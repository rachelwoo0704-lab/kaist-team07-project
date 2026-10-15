# PREMORTEM.md

Team: #07 / Wine not?

Members: 김한솜, 우승현, 류대훈, 양진석

Merged on: 2026-10-04

Last updated: 2026-10-15

**현재 적용 범위 — 기존 와인 기획의 프리모텀**

교수님은 와인의 종류가 매우 많고, 우리가 구상한 서비스를 만들려면 인터넷에 흩어진 데이터를 광범위하게 모아야 하므로 데이터 수집에 시간과 에너지가 많이 들 수 있다고 피드백했습니다. 이는 기존 목록의 외부 데이터 확보와 개발 범위 위험을 재검토할 근거가 되었습니다.

2026년 10월 10일 팀 회의에서 서울시가 제공하는 실시간 공공데이터를 활용해 주제를 다시 정해 보기로 했습니다. 구체적인 서비스 주제, 대상 사용자, 사용할 데이터는 아직 확정하지 않았습니다.

아래 위험 목록과 대응 일정은 기존 와인 기획을 기준으로 작성한 기록입니다. 새 주제에 대한 개인 프리모텀 작성·취합이 완료됐다는 뜻이 아닙니다. 새 주제가 정해지면 개인별로 위험을 재검토하고, 각자의 계정으로 커밋한 내용이 모두 반영된 뒤 저장소 소유자가 종합 문서를 다시 검토·커밋해야 합니다. 이번 수정은 상담 피드백과 방향 변경 상태를 기록한 것입니다.

> \*\*Order matters, and here it is the entire method.\*\*
> Every member first writes their own list in `docs/premortem/<name>.md`, alone.
> Only then does the team fill in this file.
>
> If you brainstorm as a group first, the first risk named anchors everyone else, and the quiet member's risk, which is usually the real one, never gets written down.
>
> Write content in Korean or English.
> Keep the headings exactly as they are.

\---

## 1\. Individual lists

|Member|File|Written on|Causes listed|
|-|-|-|-|
|김한솜|`docs/premortem/Premortem_김한솜.md`|2026-10-04|6|
|우승현|`docs/premortem/Premortem_우승현.md`|2026-10-04|5|
|류대훈|`docs/premortem/Premortem_류대훈.md`|2026-10-04|6|
|양진석|`docs/premortem/Premortem_양진석.md`|2026-10-04|5|

## 2\. Read-out

Go around the table.
One cause each, in turn, until every list is exhausted.
No debating during the read-out, and nobody reads their whole list at once.
People have to feel safe saying the awkward one, so the only allowed response is writing it down.

## 3\. The merged list

Every cause from every list goes here.
Stack the repeats into one row and keep the sharpest wording, not the most diplomatic one.
Cluster by problem, never by role or department: once a cluster is called "development", half the team decides it is somebody else's problem.

Sort by how many members raised it, most first.
The repeats are your priority signal, and you get it for free.
Break ties by expected damage.

Mark a cause with **(us)** when it exists because of who is on this team, not because of the software.
At least two rows must carry that mark: skill asymmetry, time asymmetry, who will actually debug the code the artificial intelligence (AI) wrote, who has a product launch at work in November, who agrees in meetings and then goes quiet.
A premortem with no **(us)** rows is a premortem about software, not about this team.

|#|Failure cause (past tense, specific)|Problem cluster|Raised by|How many|
|-|-|-|-|-|
|1|와인 초보는 기록까지 해 가며 자기 취향을 알고 싶어 하지 않았다. 지인들은 "있으면 좋겠다"고 했지만, 실제로는 검색만 한두 번 하고 기록은 남기지 않은 채 떠났다. 와인을 자주 사지 않으니 매장에서 추천받는 편이 더 편했고, 페르소나라던 우리조차 스스로 쓰고 싶어지지 않았다. 근거는 우리 경험뿐이었고, 팀 밖 사람에게 계속 쓸 건지 묻지 않았다|소비자 수요|우승현, 류대훈, 김한솜|3|
|2|검색·후기 요약과 저널링·취향 추천을 모두 만들려다 둘 다 애매하게 끝났다. 외부 후기 수집에 시간을 쏟느라 기록 기능을 먼저 만들지 못했다. 범위를 줄이면 쓸모가 없어질까 봐 결론을 내지 않은 채 만들면서 고쳤고, 시연 날 제대로 동작한 기능은 몇 개뿐이었다.|서비스 완성도|양진석, 류대훈, 김한솜|3|
|3|(us) 조모임이 거의 열리지 않았다. 네 명 모두 직장인이라(야근, 육아) 주중 저녁은 시간이 맞지 않았고, 주말로 미룬 모임은 한두 명씩 빠져서 다시 미뤄졌다. 결국 마지막 2주에 몰아서 만들었다. 각자 실제로 쓸 수 있는 시간을 확인하지 않고 역할과 일정을 정했고, 컨설테이션 직후에는 다음 모임 각자 바쁜 시기가 왔을 때 대신할 사람이 없었다. 양진석은 회사 겨울 성수기, 우승현은 회사 프로젝트 마감, 류대훈은 11월 중순부터 연말 약속으로 빠졌고, 그 기간에 맡은 일이 멈추거나 다른 팀원에게 넘어갔다. 셋 다 그 시기가 올 걸 알았지만 팀에 미리 알리거나 대신할 사람을 정하지 않았다.날짜도 정하지 않고 헤어졌다.|일정관리|우승현, 류대훈, 양진석|3|
|4|(us) 각자 바쁜 시기가 왔을 때 대신할 사람이 없었다. 양진석은 회사 겨울 성수기, 우승현은 회사 프로젝트 마감, 류대훈은 11월 중순부터 연말 약속으로 빠졌고, 그 기간에 맡은 일이 멈추거나 다른 팀원에게 넘어갔다. 셋 다 그 시기가 올 걸 알았지만 팀에 미리 알리거나 대신할 사람을 정하지 않았다.|일정관리|양진석, 우승현, 류대훈|3|
|5|블로그·포털·SNS 후기와 가격 정보를 써도 되는지(이용약관, 저작권, 개인정보)를 개발을 시작한 뒤에야 확인했다. 실제로 쓸 수 있는 데이터가 적어 후기 요약, 가격, 구매처 안내 같은 핵심 기능이 성립하지 않았다. 처음부터 걱정했지만 대비가 충분하지 않았다.|제약|양진석, 김한솜|2|
|6|취향 분석과 추천이 작동하지 않았다. 맛을 평가할 지표를 정하지 않고 자유 서술로 기록받다 보니 취향을 정의해 와인 정보와 매칭할 수 없었고, 기록이 쌓여도 "OO한 취향이에요"라고 말해 주지 못했다. 데이터가 쌓이면, 그리고 AI가 알아서 해 줄 거라고 믿었다.\||서비스 완성도|류대훈, 우승현|2|
|7|성공과 실패의 기준이 없어 기능만 붙이다가 목적을 잃었다. "너희는 이 서비스를 왜 만든 거야?"라는 질문에 아무도 제대로 답하지 못했다. 아무도 프로젝트의 큰 방향에 책임을 지려 하지 않았고, 그럭저럭 완성하는 데만 집중했다|서비스 목적|김한솜||
|8|최종 시연 날 Vivino나 LLM 검색 같은 기존 서비스보다 나은 점이 무엇인지 설명하지 못했다. 기록 관리에 중점을 둔다는 이유로 시중 서비스와 자세히 비교하지 않았다.|소비자 수요|류대훈|1|
|9|와인 초보 대신 와인 관여도가 높은 사람이 주 사용자가 되었는데, 그들 눈에는 기록 항목과 용어가 어색하고 전문성이 없었다. 기준을 우리가 아는 수준에서 정했고, 만들기 전에 와인을 잘 아는 사람에게 보여 주지 않았다.|서비스 완성도|우승현|1|
|10|기능은 동작했지만 화면과 사용 흐름을 다듬지 못해 프로토타입 수준에 머물렀다. 기능이 기획대로 돌아가면 완성이라고 생각했고, UI/UX 기준과 사용자 테스트 일정을 따로 정하지 않았다.|서비스 완성도|양진석|1|
|11|수익 모델이 없어 서비스를 유지할 수 없었다. 완성이 우선이라 사람 손이 덜 가고 지속 가능하게 굴러가는 구조를 고려하지 않았다.\||수익모델|김한솜|1|

Add rows until every individual list is used up.

## 4\. What only one person saw

Look again at every row above that a single member raised.

|Cause|Raised by|What we decided to do about it|
|-|-|-|
|성공과 실패의 기준이 없어 기능만 붙이다가 목적을 잃었다. "너희는 이 서비스를 왜 만든 거야?"라는 질문에 아무도 제대로 답하지 못했다. 아무도 프로젝트의 큰 방향에 책임을 지려 하지 않았고, 그럭저럭 완성하는 데만 집중했다|김한솜|진행 단계마다 목적을 재정립하는 프로세스를 구축한다.|
|최종 시연 날 Vivino나 LLM 검색 같은 기존 서비스보다 나은 점이 무엇인지 설명하지 못했다. 기록 관리에 중점을 둔다는 이유로 시중 서비스와 자세히 비교하지 않았다.|류대훈|LLM과의 검색결과와 비교하여 차별화 포인트를 추가한다.|
|와인 초보 대신 와인 관여도가 높은 사람이 주 사용자가 되었는데, 그들 눈에는 기록 항목과 용어가 어색하고 전문성이 없었다. 기준을 우리가 아는 수준에서 정했고, 만들기 전에 와인을 잘 아는 사람에게 보여 주지 않았다.|우승현|전문가는 1차 타겟이 아니라 고려하지 않는다.<br />중간 또는 말기에 전문가 대상 FGD 등을 통해 검토받는다.<br />|
|기능은 동작했지만 화면과 사용 흐름을 다듬지 못해 프로토타입 수준에 머물렀다. 기능이 기획대로 돌아가면 완성이라고 생각했고, UI/UX 기준과 사용자 테스트 일정을 따로 정하지 않았다.|양진석|프로토타입 이상의 수준까지는 학기 중 목표로 삼지 않는다.|
|수익 모델이 없어 서비스를 유지할 수 없었다. 완성이 우선이라 사람 손이 덜 가고 지속 가능하게 굴러가는 구조를 고려하지 않았다.\||김한솜|수익 모델은 최종 과제에 포함하지 않는다.|

A cause only one person saw is not a weak signal.
It is usually the one the rest of the team is structurally unable to see.

## 5\. The three we act on

Pick at most three.
More than three is a list, not a plan.

The top of the merged list is where you start looking, not an automatic answer.
If a cause only one person saw is the one that would end the project, pick it.

|#|Failure cause|Early warning signal — what we would actually observe, and when|Countermeasure — the action|Owner|By when|
|-|-|-|-|-|-|
|1|와인 초보는 기록까지 해 가며 자기 취향을 알고 싶어 하지 않았다. 지인들은 "있으면 좋겠다"고 했지만, 실제로는 검색만 한두 번 하고 기록은 남기지 않은 채 떠났다. 와인을 자주 사지 않으니 매장에서 추천받는 편이 더 편했고, 페르소나라던 우리조차 스스로 쓰고 싶어하지 않았다. 근거는 우리 경험뿐이었고, 팀 밖 사람에게 계속 쓸 건지 묻지 않았다|10월 18일까지 팀 외의 와인 초보와 이야기한 사람이 한 명도 없었다.<br />인터뷰 10명 중 6명 이상이 "지금처럼 검색하거나 직원에게 묻는 걸로 충분하다"고 답한다.|와인 초보자 20명(통계적 유의미성)을 대상으로 정량적 설문조사를 진행하여 사용성 의향을 조사한다.<br />이들이 실제로 필요하다고 말한 기능을 찾아서 추가한다.|김한솜|10/18<br />(기록 확인은 11/01)|
|2|.(us) 조모임이 거의 열리지 않았다. 네 명 모두 직장인이라(야근, 육아) 주중 저녁은 시간이 맞지 않았고, 주말로 미룬 모임은 한두 명씩 빠져서 다시 미뤄졌다. 결국 마지막 2주에 몰아서 만들었다. 각자 실제로 쓸 수 있는 시간을 확인하지 않고 역할과 일정을 정했고, 컨설테이션 직후에는 다음 모임 각자 바쁜 시기가 왔을 때 대신할 사람이 없었다. 양진석은 회사 겨울 성수기, 우승현은 회사 프로젝트 마감, 류대훈은 11월 중순부터 연말 약속으로 빠졌고, 그 기간에 맡은 일이 멈추거나 다른 팀원에게 넘어갔다. 셋 다 그 시기가 올 걸 알았지만 팀에 미리 알리거나 대신할 사람을 정하지 않았다.날짜도 정하지 않고 헤어졌다.|정기 모임에 2명 이상 빠진 주가 2주 연속 나온다. <br />공유 작업 문서를 7일 동안 아무도 수정하지 않았다|미팅이 끝나기 전에 매주 고정 화상 모임 시간(30분)을 정한다.<br />10/11까지 4명 모두 10–12월의 회사 성수기, 마감, 연말 일정을 공유 캘린더에 표시하고 일정을 공유한다.|우승현|10/11|
|3|검색·후기 요약과 저널링·취향 추천을 모두 만들려다 둘 다 애매하게 끝났다. 외부 후기 수집에 시간을 쏟느라 기록 기능을 먼저 만들지 못했다. 범위를 줄이면 쓸모가 없어질까 봐 결론을 내지 않은 채 만들면서 고쳤고, 시연 날 제대로 동작한 기능은 몇 개뿐이었다|외부 데이터를 사용하는 데에 한계가 있다고 판단 되는 시점을 묵인하고 지나갔다.\||<br />후기·가격 출처(네이버 블로그, 인스타그램, 유튜브, 가격 비교 사이트)별로 이용약관을 읽고 쓸 수 있는지 표로 정리한다<br />그 결과를 보고 검색·요약과 기록 중 MVP 핵심 하나를 팀이 정하고, 뺄 기능을 정리한다.<br /><br />우리가 사용할 외부 데이터 사용의  범위를 굉장히 명확하게 정의한다.<br /><br />데이터 사용에의 한계를 발견하면 즉시 기능을 피봇한다.<br />|양진석|10/18|

Three tests every row must pass:

* **The signal is observable.** "We notice we are falling behind" is not a signal. "Two members have not opened the project in seven days" is.
* **The countermeasure is an action, not a posture.** "열심히 하기", "우선순위 관리", and "we will be careful" are intentions. "Call three potential users and write down what they say" is an action. If it has no verb, rewrite it.
* **The owner is one named person, and there is a date.** "The team" owns nothing. A countermeasure with no date is a countermeasure with no week: it never lands on anyone's calendar.

> Example of a finished row. Delete this block before you send.
>
> - \*\*Failure cause:\*\* Nobody outside the team ever used it. We demoed to ourselves for ten weeks. \*\*(us)\*\*
> - \*\*Early warning signal:\*\* On October 24, no one outside the team has touched a working screen.
> - \*\*Countermeasure:\*\* Show a clickable first screen to three people who have the problem, and write down the first thing each of them does.
> - \*\*Owner:\*\* \[one name]
> - \*\*By when:\*\* October 24

You do not need a 1-to-5 likelihood and impact matrix, and we would rather you did not add one.
It makes every risk look equally considered whether or not it was.

Everything in section 3 that is not in this table is a risk you are knowingly leaving alone for now.
That is a decision, and it is fine.

\---

## Revision log

Any change of direction needs a new row here within one week.
A premortem that analyzes a product you no longer build is worse than none, because it reads as covered.

|Date|What changed and why|
|-|-|
|2026-10-05|Draft for consultation|
|2026-10-15|교수 상담의 데이터 수집 부담 피드백과 10월 10일 팀 회의 결정을 반영. 기존 와인 기획의 위험 목록임을 명시하고, 서울시 실시간 공공데이터를 활용할 새 주제가 확정되면 개인별 재검토와 종합 갱신이 필요함을 기록함. 이번 수정은 모든 개인 커밋 이후의 최종 종합 갱신으로 표시하지 않음.|

\---

Method note: Gary Klein, "Performing a Project Premortem", Harvard Business Review, September 2007.
