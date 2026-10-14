# Premortem — 류대훈

Team: #07 and wine not?
Written on: 2026-10-04 (10-15 commit)
I wrote this before reading anyone else's list: yes

Copy this file, rename it after yourself (for example `gildong.md`), and fill it in alone.
Do this before your team meets to merge, and do not read anyone else's list first.
Write your own list before you ask any artificial intelligence (AI).
An AI list anchors you the same way a teammate's would, and an AI does not know your team, so it can only give you the list every team would get.

Write in Korean or English, whichever you think in.
Keep the headings exactly as they are.

\---

## The premise

It is December 19, 2026.
Demo Day.
Your team's project failed.
Not "went okay" — failed, visibly, in front of the class.

You are writing the explanation of why.

Write in the past tense, as fact.
This is not a hedge-your-bets risk survey.
Asserting the failure is what makes the honest answers come out, and that is the whole reason the technique works.

## My list

Four minutes.
At least five causes.
Include the uncomfortable one.
In class you wrote three in four minutes, about yourself; this one is about the project, and you have longer.

|#|What happened (past tense, specific)|When it started|Why nobody stopped it|
|-|-|-|-|
|1|최종 시연 날에 VIVINO나 LLM 검색 등 다른 서비스의 추천 서비스보다 좋은 점이 무엇인지에 대해서 설명하기 어려웠다.|서비스를 처음 만들면서 vivino와 같은 시중 서비스와의 차이점이 확연히 보이지 않았다.|우린 와인에 대해 잘 모르는 사람도 취향을 쉽고 상세히 기록할 수 있도록 관리에 중점을 두기에 시중 서비스와는 상세히 비교하지 않았다.|
|2|개인 취향에 기반한 와인 추천이 적절히 이루어지지 않았다.|샘플 데이터로 테스트 결과, 와인 맛을 평가하는 지표를 정하지 않고 개인이 자유롭게 서술하는 방식으로 서비스를 만들다보니, 이 사람의 취향을 정의하고, 와인 정보와 매칭하기가 어려웠다. |데이터가 더 누적되고, 외부에서 데이터를 더 많이 수집하면 괜찮을 거라 생각하고 진행했다.|
|3|와인 입문자들이 한두번 이용하고 이용하지 않았다. 이들은  와인에 대한 소비 빈도가 낮고, 와인 맛에서 큰 차이점을 느끼기 어려워 오프라인 추천을 받아 이용하는 게 편했다.||주변 지인들한테 이런 게 있으면 어때? 라고 묻거나 한번 써보라고 했을 때에는 반응이 좋았기에 계속 쓸건지는 확인하지 않았다.|
|4|다루는 데이터나 서비스의 범위가 예상보다 커져서 개발하기가 어려웠고, 범위를 줄이자니 이용 가치가 낮아질 것 같아 방향성에 딜레마가 생겼고 최종 시연 때 완벽히 동작하는 기능은 소수였다.|본격적으로 서비스를 개발하면서 어느정도 서비스 구현을 목표할 것 인지가 명확하지 않았다.|결론이 나지않은 채로 계속 만들여서 수정하는 방향으로 개발을 하였다.|
|5|팀원들이 다들 야근과 육아로 바쁘다보니, 과제는 우선순위에서 뒤로 밀렸다.|10월부터 조금씩 일정이 밀리고 진척도가 낮아졌다.|최종 제출까지는 시간이 충분히 남았다고 생각해서 크게 개의치 않았다.|
|6|나는 연말 약속이 많아져서 최종 제출을 앞두고 시간을 많이 쏟지 못해 적당한 선에서 끝냈다.|11월 중순부터 저녁 약속이 많아져 시간을 내기가 어려웠다. |연말이라고 잡힌 약속들을 취소하기가 어려웠다.|

Three rules:

* **Past tense, specific.** "We never got one user outside our own team", not "user acquisition may be difficult".
* **Not generic.** "Scope creep" and "the team got busy" are true of every failed project ever, so they carry no information. What specifically crept? Who specifically got busy, in which week, because of what?
* **At least two causes involve the people in this team, and at least one of those is about you.** Skill gaps, who actually understands the code the AI wrote, who has a product launch at work in November, who says "sure" in meetings and disappears. If your list is all technical, it is a safe list, not an honest one.
