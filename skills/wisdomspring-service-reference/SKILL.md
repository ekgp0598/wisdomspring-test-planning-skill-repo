---
name: wisdomspring-service-reference
description: >
  WisdomSpring 서비스 레퍼런스 스킬. 서비스 개요, 화면기획서, 디자인 이미지, 어드민 정책, QA 가이드를 번들로 제공한다.
  트리거: (1) "위즈덤스프링 서비스 설명해줘" (2) "WisdomSpring 테스트 케이스/시나리오 만들어줘"
  (3) 화면 ID(HM-001, FD-001, PR-410 등)와 함께 QA 요청 (4) "어드민 정책 확인해줘"
  (5) "위즈덤스프링 화면 구조 알려줘" (6) 서비스 온보딩, 정책 비교, 리스크 분석 요청.
  입력: 화면 ID, 기능명, 정책 질문, 또는 자유 질문.
  출력: 한국어 QA 보고서, 테스트 시나리오, 서비스 설명, 정책 비교 결과.
user-invocable: true
argument-hint: "[화면ID 또는 질문]"
---

# WisdomSpring Service Reference

## Overview

Use this skill to turn bundled WisdomSpring artifacts into a practical QA plan and execution report. Build only the minimum context needed, test with explicit assumptions, and leave a clear Korean record of scenarios, results, defects, and open questions.

If the user is new to WisdomSpring, do not jump straight into test cases. First explain the service, the major screens, the user journey, and the visual tone using the bundled newcomer and design references.

## Inline Knowledge Base

아래 데이터는 스킬 로딩 시 즉시 참조한다. 별도 파일 읽기 없이 바로 답변에 사용한다.

### IA Map

| Mobile | Web | Depth | Name | Type |
| --- | --- | --- | --- | --- |
| `M-IN-001` | | 1 | 인트로 | page |
| `M-HM-001` | `W-HM-001` | 1 | 홈(발견) | page |
| `M-HM-030` | `W-HM-030` | 1 | 상단 메뉴 | drawer / side drawer |
| `M-HM-B002` | `W-HM-P002` | 2 | 테마 전체보기 | bottom sheet / popup |
| `M-HM-010` | `W-HM-010` | 2 | 테마 상세 | page |
| `M-HM-020` | `W-HM-020` | 3 | 학습화면-영상 | page |
| `M-HM-021` | `W-HM-021` | 3 | 학습화면-아티클 | page |
| `M-HM-B022` | `W-HM-P022` | 4 | 전체회차 | bottom sheet / popup |
| `M-HM-B023` | | 4 | 노트 | bottom sheet |
| | `W-HM-P024` | 4 | 노트 댓글 | popup |
| `M-SH-010` | `W-SH-010` | 2 | 검색결과 | popup / layer |
| `M-FD-001` | `W-FD-001` | 1 | 질문피드 | page |
| `M-FD-B030` | `W-FD-M030` | 2 | 답변쓰기 | modal |
| `M-FD-010` | `W-FD-010` | 2 | 답변 상세 | page |
| `M-FD-020` | `W-FD-020` | 3 | 오늘의 콘텐츠 | content |
| `M-PR-001` | `W-PR-001` | 1 | 프로필 | content |
| `M-PR-P110` | `W-PR-P110` | 3 | 프로필 설정 | popup |
| `M-PR-120` | `W-PR-120` | 4 | 생각기록-오늘의 질문 | tab |
| `M-PR-121` | `W-PR-121` | 4 | 노트 | tab |
| `M-PR-122` | `W-PR-122` | 4 | 댓글 | tab |
| `M-PR-130` | `W-PR-130` | 3 | 관심콘텐츠 | tab |
| `M-PR-140` | `W-PR-140` | 3 | 팔로워 / 팔로잉 | tab |
| `M-PR-210` | `W-PR-210` | 2 | 회원정보(설정) | page |
| `M-PR-310` | `W-PR-310` | 2 | 결제관리 | page |
| `M-PR-410` | `W-PR-410` | 2 | 멤버십 정보 | page |
| `M-PR-420` | `W-PR-420` | 2 | 멤버십 가입 | page |
| `M-PR-421` | `W-PR-421` | 4 | 결제정보 입력 및 가입 | page |
| `M-PR-422` | `W-PR-422` | 5 | 상품 결제 | page |
| `M-PR-P423` | `W-PR-P423` | 5 | NHN KCP 결제 | popup |
| `M-IN-010` | `W-IN-010` | 1 | 로그인 | page |
| `M-IN-011` | `W-IN-011` | 2 | 아이디 찾기 | page |
| `M-IN-012` | `W-IN-012` | 3 | 비밀번호 찾기 | page |
| `M-IN-020` | `W-IN-020` | 1 | 회원가입 | page |
| `M-CS-010` | `W-CS-010` | 1 | About(멤버십 소개) | page |
| `M-CS-011` | `W-CS-011` | 2 | 1개월 무료 체험권 | page |
| `M-CS-020` | `W-CS-020` | 1 | 공지사항 | page |
| `M-CS-050` | `W-CS-050` | 1 | 자주묻는질문(FAQ) | page |

- `HM` = 홈·테마·학습, `FD` = 질문피드·답변, `PR` = 프로필·멤버십·결제, `IN` = 인트로·로그인·회원가입, `CS` = About·공지·FAQ
- `M-` = 모바일, `W-` = 웹. 공통 ID(예: `HM-001`)는 양 플랫폼 동일 기능.

### Screen Index

| Shared ID | 화면명 | Reference file |
| --- | --- | --- |
| `HM-001` | 홈 메인(발견) | `screen-plans/HM-001 메인(발견).md` |
| `HM-010` | 테마 상세 | `screen-plans/HM-010 테마 상세 페이지.md` |
| `HM-020` | 학습화면-영상 | `screen-plans/HM-020 학습화면-영상.md` |
| `HM-021` | 학습화면-아티클 | `screen-plans/HM-021 학습화면-아티클.md` |
| `HM-030` | 상단 메뉴 | `screen-plans/HM-030 상단 메뉴.md` |
| `HM-P022` | 전체 회차 팝업 | `screen-plans/HM-P022 전체 회차 팝업-바텀시트.md` |
| `FD-001` | 질문피드 | `screen-plans/FD-001 질문피드.md` |
| `FD-010` | 답변 상세 | `screen-plans/FD-010 답변 상세.md` |
| `FD-B030`/`FD-M030` | 답변 작성 | `screen-plans/FD-B030 FD-M030 답변 작성.md` |
| `PR-001`/`PR-120` | 프로필 생각기록 | `screen-plans/PR-001 PR-120 프로필의 생각기록-오늘의 질문.md` |
| `PR-121` | 프로필 노트 | `screen-plans/PR-121 프로필-노트.md` |
| `PR-122` | 프로필 댓글 | `screen-plans/PR-122 프로필-댓글.md` |
| `PR-130` | 관심콘텐츠 | `screen-plans/PR-130 프로필-관심콘텐츠.md` |
| `PR-140` | 팔로워/팔로잉 | `screen-plans/PR-140 프로필-팔로워.md` |
| `PR-410` | 멤버십 정보 | `screen-plans/PR-410 멤버십 정보.md` |
| `IN-001` | 인트로 첫 화면 | `screen-plans/M-IN-001 인트로 첫 화면.md` |
| `M-HM-B023` | 모바일 노트 바텀시트 | `screen-plans/M-HM-B023 노트 바텀시트.md` |
| `W-HM-P024` | 웹 노트 댓글 팝업 | `screen-plans/W-HM-P024 노트 댓글 PC(WEB).md` |

### Source Loading Rules

질문 유형에 따라 아래 순서로 필요한 파일만 읽는다. 위 IA Map과 Screen Index는 이미 인라인이므로 다시 읽지 않는다.

1. 화면 ID가 주어지면 → Screen Index에서 매칭되는 `screen-plans/*.md` 1개만 읽는다.
2. 정책·스케줄·노출·수정삭제 관련이면 → `references/admin-policy-summary.md`
3. 어드민 목록·상세 필드·등록 플로우·제약 조건이면 → `references/admin-planning-spec.md`
4. 디자인·레이아웃 시각 확인이면 → `references/design-image-index.md` + `references/design-images/`
5. 화면 구조·계층·섹션 구성 설명이면 → `references/visual-structure-by-area.md`
6. 비주얼 톤·분위기 질문이면 → `references/visual-design-summary.md`
7. 서비스 입문 설명이면 → `references/service-primer.md`
8. 커버리지 계획이면 → `references/test-areas.md`
9. QA 보고서 형식이면 → `references/report-template.md`
10. 기대결과 패턴이면 → `references/expected-results.md`
11. 위 자료로 부족하면 → 사용자에게 스크린샷이나 추가 자료 요청

영역 약어로 들어오면 이렇게 매핑한다: home/발견 → `HM-*`, 질문/답변 → `FD-*`, 프로필/멤버십 → `PR-*`, 인트로/로그인 → `IN-*`, 공지/FAQ → `CS-*`

## Workflow

## Response Style Rules

Always follow these answer-style constraints when responding to the user:

- Do not expose reference markdown file names, file paths, or bundled resource names in the answer.
- Do not say which document you read. Give the answer directly.
- Do not include sections such as `근거`, `참고 문서`, `참조 파일`, `레퍼런스`, or `출처` if they would reveal markdown file names or internal resource names.
- If the user asks why or on what basis, explain the reasoning in plain product language without citing file names.
- Never output lists of `.md` files to justify the answer.
- You may mention screen IDs, but when you do, always write the screen ID and the screen name together.
- Do not use the term `spec gap` in user-facing answers.
- If the artifacts are incomplete or conflicting, resolve it internally and answer with the best-supported conclusion, a cautious assumption, or a neutral confirmation request without naming the gap category.
- Prefer direct product answers over meta-explanations about references or source material.

### 1. Fix the scope first

Classify the request into one of these modes before reading many files:

- smoke: verify major user journeys quickly
- feature: test one screen, one flow, or one requirement change
- regression: cover impacted areas around a release or policy change
- exploratory: inspect unclear behavior and surface risks
- admin-policy: compare admin rules with front behavior

If the user names screen IDs such as `HM-001`, `FD-001`, or `PR-410`, use those as the primary scope. If the user is vague, start with the baseline areas in `references/test-areas.md`.

### 2. Build context from inline knowledge first

IA Map, Screen Index, Source Loading Rules는 이미 이 문서에 인라인되어 있다. 별도 파일을 읽지 않고 바로 사용한다.

추가 파일은 Source Loading Rules에 따라 필요한 것만 읽는다. `screen-plans` 폴더를 통째로 읽지 않는다.

### 2-1. Newcomer onboarding mode

When the user appears unfamiliar with WisdomSpring, answer in this order before deeper QA work:

1. what the service is
2. who it is for
3. the main user journey
4. the major screens and content types
5. the visual and interaction tone
6. the membership and admin-policy implications

Source Loading Rules 7번(service-primer.md)과 6번(visual-design-summary.md)을 읽는다. 화면 구조 질문이면 5번(visual-structure-by-area.md)도 읽는다.

### 2-2. Admin deep-reference mode

When the user asks about admin planning or wants field-level admin behavior, read in this order:

1. `references/admin-policy-summary.md`
2. `references/admin-planning-spec.md`

Use the summary file for policy judgment and the planning-spec file for list columns, detail fields, registration rules, search filters, modal flow, hidden-delete distinction, and edit-delete lock details.

### 3. Derive test scenarios

For each scoped area, produce scenarios in this order:

1. happy path
2. boundary and validation
3. state transition
4. permission or visibility
5. platform difference
6. policy sync between admin and front

Write each case with:

- id
- objective
- preconditions
- steps
- expected result bundle
- priority

Do not collapse the expected result into a single sentence unless the flow is trivial. By default, structure the expected result bundle with these lenses:

- 정상 결과: expected success outcome
- 예외 결과: blocked or rejected outcome when preconditions are missing or invalid
- 상태 변화: UI, CTA, count, badge, route, modal, or visibility changes after the action
- 데이터 반영: whether submitted, edited, deleted, hidden, or scheduled data is reflected correctly
- 플랫폼 차이: web and mobile differences when both exist

When requirements are incomplete, do not invent behavior. Use the best-supported conclusion, or state a cautious assumption without exposing internal gap terminology.

### 4. Execute and log carefully

When actually testing, record:

- actual result
- pass or fail
- evidence path or screenshot reference
- suspected cause if inferable
- whether the issue is reproducible

When a test case contains multiple expected-result branches, log which branch was exercised and which branches remain unverified.

Separate findings internally into:

- bug: behavior conflicts with explicit artifact or stable expectation
- spec gap: artifact is ambiguous or conflicting
- setup issue: account, data, environment, or permission problem blocks execution

Do not expose the `spec gap` label to the user. Convert it into a neutral explanation, a confirmation item, or an assumption note.

### 5. Report in Korean

Default output order:

1. scope and assumptions
2. test scenarios or executed cases
3. findings ordered by severity
4. open questions
5. next recommended checks

Use concise Korean that a planner, designer, developer, or QA can all read quickly.
Do not append internal reference citations or markdown file lists to any section.

## Expected Result Rule

Default to richer expected results. Prefer this format when the user asks for test cases:

- `정상`: expected success path
- `예외`: invalid input, empty data, locked state, permission denial, or missing membership handling
- `상태변화`: button label, toast, badge, count, route, modal, or visibility changes
- `플랫폼`: mobile-web behavior differences

If the flow has admin dependencies, also include:

- `정책 연동`: scheduled open, duplicate-date restriction, edit-delete lock, hidden-delete distinction

If the flow has user-state dependencies, also include:

- `사용자 상태별`: logged-in or logged-out, subscribed or unsubscribed, own content or others' content

## Prompt Examples

If the user needs starter prompts, onboarding guidance, or shareable examples, use `references/example-prompts.md`. Prefer examples that include the skill name, the scope, the platform, and the expected output.

## Coverage Rules

Unless the user narrows the request, prioritize these WisdomSpring areas:

- 홈 또는 발견
- 질문피드와 답변 작성 또는 답변 상세
- 테마 상세와 학습화면
- 프로필, 노트, 댓글, 팔로우
- 멤버십 상태와 결제 관리
- 인트로, 공지사항, FAQ

Always call out web and mobile differences when both artifacts exist.

## Working Rules

- Prefer bundled WisdomSpring artifacts over generic QA theory.
- Do not expose file names to the user.
- Use screen IDs exactly as written in the artifacts, and pair each screen ID with its screen name in user-facing answers.
- If the user asks for evidence or rationale, summarize the relevant rule or behavior directly instead of citing internal markdown resources.
- State assumptions when environment access, test accounts, or payment conditions are unknown.
- If you cannot run the service, still return a document-based test plan and risk list.
- If artifacts conflict, reconcile them internally and answer with the most defensible conclusion or a short confirmation note without referencing source file names or the term `spec gap`.
- This skill is packaged to be shareable; prefer bundled references over machine-specific absolute paths.
- If the user asks what the service looks or feels like, follow Source Loading Rules 6번.
- If the user asks for screen structure or layout explanation, follow Source Loading Rules 4번+5번+6번.
- If the user asks about admin list structure or management behavior, follow Source Loading Rules 2번+3번.
