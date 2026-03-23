# Expected Results Guide

Use this guide when a plain one-line expected result would hide meaningful branches.

## Core rule

Do not write only:

- `정상적으로 이동한다`
- `버튼이 노출된다`
- `저장된다`

Instead, expand expected results into observable branches.

## Default expected-result bundle

### 1. 정상

Describe the success path in concrete observable terms:

- which UI appears
- which screen or layer opens
- which labels or values change
- what data becomes visible

Example:

- 정상: `답변하기` 선택 시 모바일은 `M-FD-B030` 바텀시트, 웹은 `W-FD-M030` 모달이 열린다.

### 2. 예외

Describe what should happen when input, account state, membership state, or data state blocks the action.

Examples:

- 예외: 오늘의 질문 데이터가 없으면 질문 카드 영역은 숨김 또는 빈 상태로 처리되고, 깨진 CTA는 노출되지 않는다.
- 예외: 이미 오픈된 과거 질문은 수정 또는 삭제가 차단되어야 한다.

### 3. 상태변화

Describe post-action changes, not just the immediate response.

Examples:

- 상태변화: 답변 작성 완료 후 CTA 문구가 `답변하기`에서 `답변 보기`로 바뀐다.
- 상태변화: 좋아요 선택 후 아이콘이 filled 상태로 바뀌고 카운트가 1 증가한다.

### 4. 데이터 반영

Describe how the saved, edited, deleted, hidden, or scheduled data should be reflected.

Examples:

- 데이터 반영: 삭제 처리된 노트는 프로필 노트 목록과 admin 노트 목록에서 더 이상 노출되지 않는다.
- 데이터 반영: 예약 오픈일이 오늘 이후인 테마는 프런트에서 `COMING SOON` 상태로 보인다.

### 5. 플랫폼 차이

When web and mobile differ, state both explicitly.

Examples:

- 플랫폼 차이: 모바일은 바텀시트, 웹은 팝업으로 열린다.
- 플랫폼 차이: 웹은 최대 2줄, 모바일은 최대 3줄까지 문장을 노출한다.

### 6. 정책 연동

When admin-policy behavior matters, include the rule that must be reflected.

Examples:

- 정책 연동: 동일 날짜에는 오늘의 질문을 중복 등록할 수 없어야 한다.
- 정책 연동: 과거 오픈 완료 질문은 수정 및 삭제가 불가해야 한다.

## Shortcut by scenario type

- navigation case: 정상 + 상태변화 + 플랫폼 차이
- validation case: 예외 + 상태변화
- membership case: 정상 + 예외 + 사용자 상태별
- admin-sync case: 정책 연동 + 데이터 반영
- list-rendering case: 정상 + 예외 + 플랫폼 차이

## Good output example

Bad:

- 기대결과: 테마 상세로 이동한다.

Better:

- 정상: 선택한 테마 카드에 해당하는 `HM-010` 테마 상세 화면으로 이동한다.
- 예외: 오픈 전 테마인 경우 상세 진입은 가능하더라도 `COMING SOON` 상태가 유지되어야 한다.
- 상태변화: 홈 화면에서 선택한 테마 컨텍스트가 상세 화면 상단 타이틀과 썸네일에 반영된다.
- 플랫폼 차이: 모바일과 웹 모두 테마 상세로 이동하지만 전체보기 진입 방식은 모바일 바텀시트, 웹 팝업으로 다를 수 있다.

## Minimum bar

If the user asks for test cases, aim for at least two branches in each expected result:

- one success branch
- one exception or state-change branch
