# Regular Expression

Created: 2020년 8월 10일 오후 1:54
Type: Lecture
url: https://regexone.com/

# Lesson 1 : An Introduction, and The ABCs - `abc...` Letters

**정규 표현식**은 코드, 로그 파일, 스프래드시트 그리고 심지어 문서에서부터 정보를 추출할때 매우 효율적입니다. 일반적인 언어  뒤엔 많은 이론들이 있지만, 앞으로 나올 내용과 예제에서 정규 표현식의 실용적인 사용을 최대한 빠르게 익힐 수 있을것입니다.

정규표현식을 사용할때 가장 먼저 인지해야 할 점은 **모든 것은 본질적으로 문자(Character)** 이고, 특정한 문자의 순서에 맞는 패턴을 사용하고있다는 것입니다 (string으로 알려져있는 것들도요.). 대부분의 패턴들은 문자, 숫자, 구두점 및 %#$@! 와 같은 너의 키보드에 있는 기타 기호들을 포함하는 일반적인 ASCII를 사용하지만, 유니코드 문자는 국제적인 텍스트 형식에 맞추는데도 사용합니다.

아래에는 몇줄의 문자들이 있습니다. 너가 아래에 있는 입력창에 입력할때 각 줄에 일치하는 문자를 나타내는 하이라이트가 어떻게 변하는지 확인하세요. 다음 수업을 계속하려면, 너는 새로운 문법과  각각의 수업에서 주어진 라인들을 모두 매치하게 하는 패턴을 작성하는 개념을 사용할 줄 알아야합니다.

아래 주어진 3개의 열에 맞는 패턴을 어서 작성 해 보세요. **아마 쉬울껍니다.**

![Regular%20Expression%20c7f578c159664245907b307f955ff88a/Untitled.png](Regular%20Expression%20c7f578c159664245907b307f955ff88a/Untitled.png)

---

# Lesson 1.5 : The 123s - `123...` Digits / `\d` Any Digit / `\D` Any Non-digit character

문자(Character)들은 일반적인 알파뱃을 포함합니다. 숫자 역시 그렇습니다. 사실 0~9 숫자들도 또한 그냥 문자들입니다. 만약 너가 [ASCII table](https://en.wikipedia.org/wiki/ASCII#ASCII_printable_characters)을 본다면 숫자들이 연속적으로 목록에 있는 것을 볼 수 있을것입니다.

다양한 수업을 통해 특정 유형의 문자(Character) 에 맞춰 사용할 수 있는 정규표현식에 사용되는 특수 메타케릭터를 다수 소개할껍니다. 이번 시간에서는, 문자 **\d** 가 **0~9인 어떠한 숫자**가 있는 위치에 사용되어질 수 있다는 것입니다. 앞에 있는 슬래쉬는 단순한 문자 **d** 와 구별시켜주고 이게 메타케릭터라는것을 나타냅니다.

아래에 숫자를 포함하는 몇개의 문장이 있습니다. 아래에 있는 문자열에 있는 모든 숫자가 일치하는 패턴을 적어보는 것을 시도해보고, 너의 패턴이 단순히 첫 시작 문자가 아닌 **문자열 내 어디든 일치하는 것**을 주목하세요. 나중에 나올 수업에서 우린 이걸 어떻게 컨트롤 할껀지에 대해 배울 것입니다.

![Regular%20Expression%20c7f578c159664245907b307f955ff88a/Untitled%201.png](Regular%20Expression%20c7f578c159664245907b307f955ff88a/Untitled%201.png)

---

# Lesson2: The Dot - `.` any character / `./` Period

카드게임에서 조커는 와일드카드이면서 댁에 있는 카드 중 어떠한 것들로 나타낼 수 있습니다. 정규표현식을 사용하면 패턴이나 구조(예를 들면 전화번호나 주소와 같이)를 공유한다는 사실 외에 정확한 내용을 모르는 택스트 조각과 일치하는 경우가 많습니다.

비슷하게, .(점) 메타케릭터가 와일드카드의 개념을 가지고 있습니다. 그리고 이건 어떠한 한개의 문자와 매칭할 수 있습니다. (글자, 숫자, 공백, 이외 전부). 당신은 기존 마침표와의 일치를 무시한다는 것을 알 수 있습니다. 따라서 마침표를 정확하게 일치시키기 위해선, 슬래시 \. 를 사용하여 기존 마침표와 구별해야 합니다.

아래에 같은 길이이지만 다양한 문자를 가지는 문자열들이 있습니다. 먼저 3개의 문자열을 매칭할 수 있지만 마지막 문자열은 아닌(스킵될 수 있는)  하나의 패턴을 작성 해 보세요. 당신은 몇몇 문장에서 그 범위에 맞추기 위해 . 메타케릭터를 사용하지 말아야 할 수 있습니다.

![Regular%20Expression%20c7f578c159664245907b307f955ff88a/Untitled%202.png](Regular%20Expression%20c7f578c159664245907b307f955ff88a/Untitled%202.png)

> *3개의 문자들을 맞추기 위해선 `...\.` 를 사용할 수 있고, 마침표를 일치시키기 위해 최종 와일드카드 메타 케릭터를 탈출시킬 수 있습니다.*

---

# Lesson 3: Matching specific characters - `[abc]` Only a, b or c

저번 수업시간에서 배운 점(.) 메타케릭터는 꽤나 강력하지만 때떄로 **너무 과하게 강력해**. 예를 들어서 우리가 휴대폰 번호를 맞춘다고 했을 때, 우리는 "(+ab)-cdef-ghij" 와 같은 문자가 유효한 숫자인지 확인하고 싶어하지 않아해!

**대괄호** 안에 정의하는 정규 표현식을 사용하여 **특정한 문자를 매칭**하기 위한 방법이 있어. 예를 들어, *[abc]* 라는 패턴은 오직 **하나의** a, b, c 문자에만 부합하고 다른것과는 부합하지 않아.

아래 여러줄에서, 처음에 오는 3개의 문자열만 매칭하고 마지막 3개의 문자열은 매칭하지 않길 원해. 우리가 만약 .(점) 을 쓴다면 마지막 3개의 문자열이 매칭되는것을 피할 수 없지만, 위의 표기법을 사용하여 일치시킬 문자를 구체적으로 정의할 수 있어.

![Regular%20Expression%20c7f578c159664245907b307f955ff88a/Untitled%203.png](Regular%20Expression%20c7f578c159664245907b307f955ff88a/Untitled%203.png)

> *다른 줄에있는 것들은 매칭하지 않고, 'can', 'man' 그리고 'fan'만 맞추기위해선 정규표현식 [cmf]an 을 사용할 수 있어, 너가 다음 수업에서 볼 수 있듯이 반대로 [^drp]an 이런 정규표현식을 사용한다면 앞 3문자 'd','r','p'로 시작하지 않고 an으로 끝나는 문자를 찾을 수 있어. (역주)위 답이 [cmf]an 말고도 [^drp]an 도 가능하다는 이야기입니다.*

---

# Lesson 4: Excluding specific characters - `[^abc]` Not a, b or c

몇몇 상황에선, 우리는 같이 포함되지 않길 원하는 특정된 문자들이 있다는것을 알고있어. 예를 들면, 휴대전화에서 지역 코드 650은 포함 안되는 휴대폰 번호들을 찾고싶어하는 상황이야.

이런걸 나타내기 위해선, 우리는 **대괄호** 와 **^ (hat)** 을 사용하는 **특정 문자들을 제외**하는 표현을 사용할 수 있어. 예를 들면 패턴 **[^abc]**는 문자 a, b, c를 **제외한 한 문자**를 매칭해.

아래에 있는 문자열들을 가지고, 살아있는 동물들만 매칭하는 패턴을 한번 작성해봐. (hog, dog... 하지만 bog는 빼구). 이 유형의 대부분 패턴은 실제로 동일한 동전의 양면이기 때문에 지난 강의의 기술을 사용하여 작성 될 수 있다는 것을 명심해. 두가지 선택을 가짐으로서, 너만의 팬턴을 작성할 때 어떤게 더 쉽고 잘 이해 할 수 있는지 정할 수 있어.

![Regular%20Expression%20c7f578c159664245907b307f955ff88a/Untitled%204.png](Regular%20Expression%20c7f578c159664245907b307f955ff88a/Untitled%204.png)

> *가장 간단한 해결방법은 'og' 로 끝나고 'bog'만 매칭하지 않는 '[^b]og` 표현이야. 반대로 이전 단원에서 배운것을 사용하면 '[hd]og'를 사용할 수 있지. 이건 'hog'와 'dog'를 매칭하고 'bog'는 매칭하지 않아. 이게 조금더 제한적인 표현이라는 것을 알아둬. 왜냐하면 이건 매칭될 수 있는 문자열이 제한되니깐.*

---