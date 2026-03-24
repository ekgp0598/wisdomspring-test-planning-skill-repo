# Visual Structure By Area

Use this file when the user asks how WisdomSpring screens are visually structured, how mobile and web differ, what major UI blocks exist on a screen, or how the design organizes information.

This file is based on the bundled images under `references/design-images/`. It is more structural and screen-specific than `visual-design-summary.md`.

## 1. Shared visual grammar

### 1.1 Core composition pattern

Across most WisdomSpring screens, the visual structure follows this sequence:

1. quiet header or top bar
2. one dominant summary block near the top
3. one or more content cards or rails below
4. lighter secondary exploration blocks near the bottom

This gives the product a reading-first rhythm rather than a dashboard-first rhythm.

### 1.2 Layout principles

- Mobile uses a single vertical column with long feed continuity.
- Web keeps the same order of information, but introduces wide centered containers and more whitespace between blocks.
- Large surfaces are usually white or pale warm gray.
- High-emphasis content sits inside muted green, olive, or soft beige cards.
- Rounded rectangles are the default container shape for both cards and controls.

### 1.3 Repeating UI primitives

- top navigation with minimal chrome
- pill tabs or segmented filters
- large hero card or status card
- horizontal content rails
- stacked feed cards
- accordion-like expandable groups
- low-noise CTA buttons
- small status badges such as `NEW`

### 1.4 Visual emphasis rules

- Green carries primary action, active state, membership state, and selected tab emphasis.
- White space is used aggressively to separate blocks instead of heavy borders.
- The most important block usually appears first and is visually larger than the rest.
- Secondary controls are often text-light, icon-light, and intentionally subdued.

## 2. Home and discover

Representative images:

- `M-HM-001 메인(발견).png`
- `W-HM-001 메인(발견).png`
- `M-HM-B002 테마 전체보기.png`

### 2.1 Information hierarchy

The home screen is structured as an editorial landing page:

1. today's question banner
2. large theme card carousel
3. continue-watching rail
4. today's quote block
5. multiple curation rails
6. all-theme exploration cards

The sequence is intentionally emotional first, then navigational.

### 2.2 Mobile structure

- The mobile version behaves like a continuous discovery feed.
- The top question area is compact and text-led.
- The first major visual anchor is the theme card.
- Subsequent sections are broken into small vertical blocks with short titles and horizontal cards.
- Exploration cards at the bottom become simpler and flatter than the upper content rails.

### 2.3 Web structure

- The web version expands the same sections into wide rails.
- Theme cards dominate the top and behave like a hero carousel.
- Lower sections are arranged as horizontally aligned card rows with more breathing room.
- Quotes and curation sections sit inside soft content bands, giving the page an editorial-magazine feel.

### 2.4 Design implications

- The home screen depends on section order for meaning.
- If one rail collapses spacing or card height, the page loses rhythm quickly.
- Badge placement and card alignment matter more here than dense data accuracy.

## 3. Question and answer

Representative images:

- `M-FD-001-질문피드.png`
- `W-FD-001 web-질문.png`
- `M-FD-B030 질문피드_작성.png`
- `W-FD-M030 답변쓰기 질문피드_작성.png`
- `M-FD-010 오늘의 질문 _ 나.png`
- `M-FD-010 오늘의 질문 _타인.png`
- `W-FD-010 답변상세 댓글달기.png`

### 3.1 Page structure

The question area is designed as a reflective community feed:

1. current question block at the top
2. answer composer entry or CTA
3. long vertical answer feed
4. inserted related content card
5. detailed answer view with comment interaction

### 3.2 Visual character

- Answer cards are long, lightly bordered or softly filled blocks.
- Green-tinted cards distinguish authored content from neutral background.
- The question itself remains visually pinned and persistent.
- Controls such as like, comment, and follow are present, but visually understated.

### 3.3 Mobile structure

- Mobile emphasizes vertical continuity and continuous reading.
- Cards stack tightly and preserve a feed rhythm.
- The current question remains visible as a strong upper anchor.
- Composition modals or bottom sheets feel native to the feed rather than separate workflows.

### 3.4 Web structure

- Web keeps a single dominant column rather than turning into a dashboard.
- The result still feels like a reading wall, not a table.
- Feed width stays constrained to maintain legibility and reflective tone.

### 3.5 Answer detail structure

- Answer detail prioritizes the answer body first.
- Interaction counts and comments are secondary.
- The comment area visually extends the answer instead of competing with it.

## 4. Theme detail and learning

Representative images:

- `M-HM-010 테마상세.png`
- `W-HM-010 테마상세.png`
- `M-HM-020 학습화면.png`
- `W-HM-020 학습화면=영상.png`
- `M-HM-021 아티클.png`
- `W-HM-021 아티클.png`
- `M-HM-B022 전체회차.png`
- `W-HM-P022 전체회차.png`
- `M-HM-B023 댓글작성.png`
- `W-HM-P023 댓글작성1.png`

### 4.1 Theme detail layout

Theme detail uses a curated-path structure:

1. theme identity block
2. progress or continue-watching block
3. stacked subtheme groups
4. expandable content rows
5. lower related-theme exploration

The user is guided downward through the theme as if reading a curated syllabus.

### 4.2 Mobile theme detail

- Mobile compresses the theme hero into a tall introductory block.
- Progress and CTA remain close to the top.
- Subtheme groups feel accordion-like and clearly chunked.
- Lower exploration remains available without overpowering the theme sequence.

### 4.3 Web theme detail

- Web gives the hero more width and makes progress visually easier to scan.
- Accordion groups breathe more and feel like curated content chapters.
- Card groups remain centered and avoid dense multi-column complexity.

### 4.4 Video learning structure

Video learning screens follow this order:

1. dominant media player
2. compact metadata and action row
3. adjacent or lower episode navigation
4. note area
5. recommended content
6. theme exploration

The player is the anchor, but the surrounding blocks still preserve the same calm editorial tone.

### 4.5 Article learning structure

- Article learning replaces the media-heavy top with a structured reading header.
- The article title and summary act as the visual entry point.
- The body becomes the main surface, with supporting interactions below.
- The page remains visually consistent with video learning even without a player.

### 4.6 Note and comment overlays

- Mobile note interactions are layered as bottom sheets.
- Web note interactions become popup overlays or inline sections.
- The design keeps comments attached to the learning context instead of turning them into a separate social product.

## 5. Profile, records, and follow structure

Representative images:

- `M-PR-120 프로필_생각기록.png`
- `W-PR-120 프로필_생각기록.png`
- `M-PR-121-프로필_노트.png`
- `W-PR-121-프로필_노트.png`
- `M-PR-122-프로필_댓글.png`
- `W-PR-122 프로필_댓글.png`
- `M-PR-140 프로필_팔로우_팔로워.png`
- `W-PR-140 프로필_팔로우_팔로워.png`

### 5.1 Profile page hierarchy

Profile and record pages follow this sequence:

1. identity header card
2. counts and tab summary
3. selected archive list
4. item-level actions such as edit, delete, or follow

The emotional center is the user's accumulated thinking, not the user's avatar alone.

### 5.2 Record screens

- Question history is presented as a chronological archive.
- Date grouping helps the page feel like a reading log or journal.
- The card styling is restrained so the written content remains central.

### 5.3 Follow and relationship screens

- Follow screens keep the same profile context at the top.
- Relationship lists are simple, card-light rows with soft action buttons.
- The design treats follow as a low-noise utility, not a social growth mechanic.

## 6. Membership and billing

Representative images:

- `M-PR-310_멤버십 정보_결제 관리o.png`
- `W-PR-310_멤버십 정보_결제 관리o.png`
- `M-PR-410_멤버십 정보_구독중.png`
- `W-PR-410_멤버십 정보_구독중.png`
- `M-PR-410_멤버십 정보_현황(사용정지).png`
- `W-PR-410_멤버십 정보_현황(사용정지).png`
- `M-PR-421_멤버십 가입.png`
- `W-PR-421_멤버십 가입.png`

### 6.1 Membership information structure

Membership pages are intentionally sparse:

1. large status hero card
2. concise subscription info block
3. small supporting notice text
4. payment-management link or next-step CTA

### 6.2 Visual tone

- The upper hero card carries most of the state meaning.
- Subscription period and fee are readable at a glance.
- The rest of the page is minimal and trust-oriented.
- Even failure or suspended states are communicated with restraint instead of alarm-heavy UI.

### 6.3 Mobile and web difference

- Mobile keeps the hero card tall and stacked.
- Web spreads the same information horizontally while preserving emptiness around the card.
- Neither version introduces extra billing complexity into the layout.

## 7. Intro and support

Representative images:

- `M-IN-001 인트로 첫 화면.png`
- `M-CS-020-_공지사항.png`
- `W-CS-020-_공지사항.png`
- `M-CS-030_FAQ.png`
- `W-CS-030_FAQ.png`

### 7.1 Intro structure

- The intro uses a full-bleed emotional background image.
- The current question and sample answer sit inside translucent cards.
- CTA buttons are large and stacked near the bottom.
- The screen is much more atmospheric than the rest of the service.

### 7.2 FAQ and support structure

- FAQ screens are flatter and more utility-driven than the core learning experience.
- Category tabs appear near the top.
- Questions are stacked in accordion rows.
- The answer area expands inline and keeps the layout clean.

## 8. Mobile versus web summary

### 8.1 Mobile

- one-column continuous reading flow
- stronger use of stacking and sheets
- more feed-like continuity
- more compact titles and cards

### 8.2 Web

- centered wide containers
- more whitespace between sections
- wider card rails and clearer grouping
- same emotional tone without changing the core information order

## 9. How the skill should use this file

- Use this file when the user asks for design structure, visual hierarchy, layout explanation, or mobile-web structural comparison.
- Use `visual-design-summary.md` for tone and mood.
- Use `screen-plans/*.md` for interaction and behavior rules.
- Use `design-image-index.md` to locate representative image files by area or screen ID.
- When text artifacts and images conflict, explain the difference as `design-reference gap` rather than silently choosing one.
