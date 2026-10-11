# QUESTIONS.md

Team: #07 / Wine not?

Last updated: 2026-10-04

Your biggest open questions about this project.
Write this together, after the premortem merge.

At most five, most important first.
The consultation opens with question 1, so put the one you are least sure about there, not the one that is easiest to ask.

Write in Korean or English.
Keep the headings exactly as they are.

\---

## What counts as an open question

* **The answer would change what you do next.** If every possible answer leaves your next two weeks the same, it is curiosity, not an open question.
* **It is specific to this project.** "Is our idea good?" cannot be answered in 30 minutes. "We assume the person in `PROJECT.md` will enter data by hand every day, and none of us has asked one. How do we test that in a week?" can.
* **You have already tried something.** Say what you think the answer is today, even if it is a guess. A question with a guess attached gets a much better answer than a bare one.

Two good places to look for questions:

* `docs/PREMORTEM.md` — a cause of failure you could not find a countermeasure for is a question.
* `docs/PROJECT.md` — the section you argued about longest, or the one where you wrote "nobody yet".

## Our questions

### 1\. 와인 초보는 정말로 마신 와인을 기록하고, 그 기록으로 자기 취향을 알고 싶어 할까?

* **Why it matters:** 우리 서비스의 한 축인 저널링과 취향 추천은 사용자가 기록을 계속 남긴다는 가정이 있다. 초보가 검색만 한두 번 하고 기록은 남기지 않은 채 떠나는 경우 이는 의미가 없는 서비스가 된다.
* **What we think today:** 지금 근거는 우리의 경험과 의견 뿐이고 그 외 와인 초보자에게는 묻지 않았다. 팀원 중에는 맛있게 마신 와인을 나중에 기억하지 못한 경험이 있어 기록이 유용하다고 보는 사람이 있다. 반면, 팀원 스스로 쓰고 싶지 않을 수 있다는 의견도 있다. 와인을 자주 사지 않는 초보는 매장 직원 추천이 더 편할 수도 있다. 외부 문의 결과 대부분(or 10명 중 6명 이상)이 "지금처럼 검색하거나 직원에게 묻는 걸로 충분하다"고 답하면 피봇을 해야할 수 있다.
* **Who could answer it:** 팀 밖 와인 초보 10명 \~ 20명. 팀원마다 2–3명씩 10/18까지 만나보고 마지막으로 와인을 어떻게 골랐는지와 마신 와인을 기억하는지, 기록은 하는지 묻는다. 그리고 이러한 서비스가 있다면 원하는 기능이 있는지도 묻는다.

### 2\. 후기 요약, 국내 가격, 구매처 데이터를 어떤 출처와 이용 권한으로 확보할 수 있고, 그 결과에 따라 MVP의 핵심을 검색·요약과 기록 중 무엇으로 할 것인가?

* **Why it matters:** 흩어진 후기를 AI가 요약하고 국내 가격과 구매처를 보여주는 기능을 포함하기에 이 데이터를 합법적이고 안정적으로 확보하지 못하면 기능이 성립하지 않는다. 검색·요약과 기록을 모두 만들려다 둘 다 애매하게 끝날 수 있다. 
* **What we think today:** 식품의약품안전처의 수입식품 공식 API에서 제품명, 제조국, 수입업체 같은 기본 정보를 얻을 수 있다. 그러나 이 자료에는 현재 판매가격과 매장 재고 정보가 없다. 따라서 가격 정보는 사용자가 구매 장소와 가격을 직접 입력하게 하거나, 비비노나 블로그·포털·SNS의 후기와 사진은 이용 허락 없이 자동으로 수집하지 말자는 의견도 생각해볼 수 있다.
* **Who could answer it:** 출처별 이용약관(네이버 블로그, 인스타그램, 유튜브, 가격 비교 사이트)은 양진석이 10/18까지 표로 정리한다. 식품의약품안전처 API는 실제로 호출해서 결과를 확인한다. 그 밖에 교수님, 데이터 수집 경험이 있는 개발자, 국내 와인 수입사와 판매점 관계자에게 물어볼 수 있다.

### 3\. 와인 초보가 남긴 소수의 기록과 쉬운 맛 표현만으로 개인 취향을 파악하고 의미 있는 추천을 만들 수 있을까?

* **Why it matters:** 초보자는 와인 전문 용어를 모르고, 처음에는 기록 수도 적다. 그래서 AI가 부족한 정보를 근거 없이 채우거나, 일반적으로 인기 있는 와인을 개인 추천처럼 내놓을 위험이 있다. 반대로 와인을 아는 사람 눈에는 기록 항목과 용어가 어색한 경우도 나왔다. 
* **What we think today:** 자유로운 한 줄 감상이나 한두 번의 별점만으로는 믿을 만한 개인 추천을 만들기 어렵다고 본다. 초기에는 당도·산미·바디·타닌, 좋았던 점과 싫었던 점, 가격대, 마신 상황처럼 초보자도 고를 수 있는 구조화된 항목을 함께 받는다. AI는 사용자의 기록을 쉬운 말로 정리하고, 비슷한 특성의 와인을 추천하는 이유를 설명하는 역할부터 맡긴다. 추천이 실제로 적절한지는 프로토타입이 나온 뒤 검증한다. 
* **Who could answer it:** 와인을 가끔 마시지만 전문 지식은 부족한 사용자에게 기록 화면을 직접 써 보게 한다. 맛 기록 항목이나 용어에 대해서는 와인 전문가, 와인 애호가 등 와인에 대한 전문지식과 관심이 높은 사람에게 물어볼 수 있다.

\[Add up to two more.
Stop at five.]

## Where we disagree



* 초보가 기록을 남길까 : 팀원 중에는 맛있게 마신 와인을 기억하지 못한 경험이 있어 기록 기능이 유용하다고 보는 사람이 있다. 반면 우리도 스스로 사용하고 싶지 않았다는 의견이 상충한다.
* 외부 후기를 쓸 것인가 : 외부 후기는 이용하는 데 저작권 문제가 있을 수 있으므로 블로그·포털·SNS 후기를 허락 없이 자동으로 수집하지 않고,, 가격과 구매처는 사용자가 직접 입력하는 방향을 제안했다.



\---

## After the consultation

Fill this in within a week of your slot.

|#|What we heard|What we will do about it|Owner|By when|
|-|-|-|-|-|
|1|||||
|2|||||
|3|||||

## Revision log

|Date|What changed and why|
|-|-|
|2026-10-05|Draft for consultation|
|\[YYYY-MM-DD]|Revised after consultation on \[date]: \[what changed]|
