# Regular Expression

Created: 2020년 8월 10일 오후 1:54
Type: Lecture
url: https://regexone.com/

# Lesson 1 : 개요와 ABC

**정규 표현식**은 코드, 로그 파일, 스프래드시트 그리고 심지어 문서에서부터 정보를 추출할때 매우 효율적입니다. 일반적인 언어  뒤엔 많은 이론들이 있지만, 앞으로 나올 내용과 예제에서 정규 표현식의 실용적인 사용을 최대한 빠르게 익힐 수 있을것입니다.

정규표현식을 사용할때 가장 먼저 인지해야 할 점은 **모든 것은 본질적으로 문자(Character)** 이고, 특정한 문자의 순서에 맞는 패턴을 사용하고있다는 것입니다 (string으로 알려져있는 것들도요.). 대부분의 패턴들은 문자, 숫자, 구두점 및 %#$@! 와 같은 너의 키보드에 있는 기타 기호들을 포함하는 일반적인 ASCII를 사용하지만, 유니코드 문자는 국제적인 텍스트 형식에 맞추는데도 사용합니다.

아래에는 몇줄의 문자들이 있습니다. 너가 아래에 있는 입력창에 입력할때 각 줄에 일치하는 문자를 나타내는 하이라이트가 어떻게 변하는지 확인하세요. 다음 수업을 계속하려면, 너는 새로운 문법과  각각의 수업에서 주어진 라인들을 모두 매치하게 하는 패턴을 작성하는 개념을 사용할 줄 알아야합니다.

아래 주어진 3개의 열에 맞는 패턴을 어서 작성 해 보세요. **아마 쉬울껍니다.**

![Regular%20Expression%20c7f578c159664245907b307f955ff88a/Untitled.png](Regular%20Expression%20c7f578c159664245907b307f955ff88a/Untitled.png)

---

# Lesson 1.5 : The 123s

문자(Character)들은 일반적인 알파뱃을 포함합니다. 숫자 역시 그렇습니다. 사실 0~9 숫자들도 또한 그냥 문자들입니다. 만약 너가 [ASCII table](https://en.wikipedia.org/wiki/ASCII#ASCII_printable_characters)을 본다면 숫자들이 연속적으로 목록에 있는 것을 볼 수 있을것입니다.

다양한 수업을 통해 특정 유형의 문자(Character) 에 맞춰 사용할 수 있는 정규표현식에 사용되는 특수 메타케릭터를 다수 소개할껍니다. 이번 시간에서는, 문자 **\d** 가 **0~9인 어떠한 숫자**가 있는 위치에 사용되어질 수 있다는 것입니다. 앞에 있는 슬래쉬는 단순한 문자 **d** 와 구별시켜주고 이게 메타케릭터라는것을 나타냅니다.

아래에 숫자를 포함하는 몇개의 문장이 있습니다. 아래에 있는 문자열에 있는 모든 숫자가 일치하는 패턴을 적어보는 것을 시도해보고, 너의 패턴이 단순히 첫 시작 문자가 아닌 **문자열 내 어디든 일치하는 것**을 주목하세요. 나중에 나올 수업에서 우린 이걸 어떻게 컨트롤 할껀지에 대해 배울 것입니다.

![Regular%20Expression%20c7f578c159664245907b307f955ff88a/Untitled%201.png](Regular%20Expression%20c7f578c159664245907b307f955ff88a/Untitled%201.png)

---

# Lesson2: The Dot

카드게임에서 조커는 와일드카드이면서 댁에 있는 카드 중 어떠한 것들로 나타낼 수 있습니다. 정규표현식을 사용하면 패턴이나 구조(예를 들면 전화번호나 주소와 같이)를 공유한다는 사실 외에 정확한 내용을 모르는 택스트 조각과 일치하는 경우가 많습니다.

비슷하게, .(점) 메타케릭터가 와일드카드의 개념을 가지고 있습니다. 그리고 이건 어떠한 한개의 문자와 매칭할 수 있습니다. (글자, 숫자, 공백, 이외 전부). 당신은 기존 마침표와의 일치를 무시한다는 것을 알 수 있습니다. 따라서 마침표를 정확하게 일치시키기 위해선, 슬래시 \. 를 사용하여 기존 마침표와 구별해야 합니다.

아래에 같은 길이이지만 다양한 문자를 가지는 문자열들이 있습니다. 먼저 3개의 문자열을 매칭할 수 있지만 마지막 문자열은 아닌(스킵될 수 있는)  하나의 패턴을 작성 해 보세요. 당신은 몇몇 문장에서 그 범위에 맞추기 위해 . 메타케릭터를 사용하지 말아야 할 수 있습니다.

![Regular%20Expression%20c7f578c159664245907b307f955ff88a/Untitled%202.png](Regular%20Expression%20c7f578c159664245907b307f955ff88a/Untitled%202.png)

> *3개의 문자들을 맞추기 위해선 `...\.` 를 사용할 수 있고, 마침표를 일치시키기 위해 최종 와일드카드 메타 케릭터를 탈출시킬 수 있습니다.*

---
