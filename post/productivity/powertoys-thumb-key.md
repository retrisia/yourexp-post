---
title: 딸깍으로 작업속도 10배 늘리기 - PowerToys 가이드
post_excerpt: Keyboard Manager 하나로 빠르고 편하게 타이핑, 작업하는 방법
featured_image: _images/keyboardmanager.png
taxonomy:
    category:
        - productivity
post_status: publish
published: October 22, 2024
author: Mingyu Choi
---

<section class="width-700 area-head-color bg-white">

<div class="callout-blue">**⌨️ 해당 글은 0.85.1 버전에서 작성되었습니다**</callout>

엄지 딸깍으로 여러분들의 작업 속도를 10배는 늘려주는 방법입니다.

Microsoft 공식 유틸리티인 PowerToys 의 Keyboard Manager 로만 진행됩니다.

이거 깔아도 여러분들 컴퓨터에 아무 문제 없습니다.

<div class="callout-blue">

**힘쎈 장난감(PowerToys) 설치가 안되어있으면 여기**

[자세한 설명](https://learn.microsoft.com/ko-kr/windows/powertoys/) / 설치 [Github](https://github.com/microsoft/PowerToys/releases), [Microsoft Store](https://aka.ms/getPowertoys)

</callout>

# Keyboard Manager

Keyboard Manager 는 단축키 리매핑, 키 리매핑 해주는 유틸리티 입니다.

![Keyboard Manager](/_images/keyboardmanager.png "Keyboard Manager")

Remap a Key(키 다시 매핑)은 키가 고장났을 때 리매핑, 게임 할 때 꼼수 용(공유키)으로 사용할 수 있는 유틸리티입니다.

하지만 평소에는 그럴 일이 없습니다.

우리는 Remap a shortcut(바로 가기 다시 매핑) 에만 집중해줍시다.

## Remap a shortcut

![Remap a shortcut](/_images/remapashortcut.png "Remap a shortcut")

이를 조금 풀어서 설명하자면 다음과 같습니다.

- **Select(선택):** 단축키를 설정하면 됩니다. Mod키(Ctrl, Alt, Shift, Win) 와 다른 키를 조합하면 됩니다.
- **To(대상):** 단축키가 사용되면 어떤 일을 할지 설정하면 됩니다.
    - **Send Key/Shortcut(키/바로 가기 보내기):** 키보드로 하는 행동입니다.
    - **Send Text(문자 메시지 보내기):** 텍스트 보내기입니다. (번역이 이상함)
    - **Run Program(프로그램 실행):** 프로그램을 실행합니다. Arguments(인수) 와 Start in(시작 위치) 를 설정할 수 있습니다.
    - **Open URI(URI 열기):** URI 를 엽니다.
- **Target app(대상 앱):** 작성하지 않으면 전체, 프로세스 이름을 설정할 수 있습니다.

## Target app

Target app(대상앱)의 프로세스 이름은 작업관리자를 켜서 찾을 수 있습니다.

![How to find a process name](/_images/howtofindaprocessname.png "How to find a process name")

안 보인다면 프로세스가 여러개 있는 것이니 프로그램의 왼쪽, 토글을 열어보시면 보입니다.

기본 이해가 되었으니 다음 단계로 넘어가 봅시다.

# Keyboard Layer

포토샵에서는 레이어 별 다른 객체를 두고 쌓는 형식으로 작업을 하게 됩니다. 키보드도 똑같다고 생각하시면 됩니다.

평소에는 일반 QWERTY 레이어, `Alt` 키를 누른 동안에 방향키 레이어가 작동한다고 상상해 봅시다. (Shift Layer 라고 부릅니다)

일단 평소에 글, 코드를 작성한다는 가정 하에 효율적인 구성 위주로 위주로 설정해봅시다.

## 이렇게 쓰면 글 수정 고트겠네 ㅋㅋ

![Bazecor: Keymap with alt arrows layer](/_images/bazecoraltarrow.png "Bazecor: Keymap with alt arrows layer")

임시로 배치하면 이런 느낌입니다. 그런데 여러분들 평소에 글 쓰면 `Home`, `End`, `Page Up`, `Page Down` 이런 거 안 쓰고 마우스로 에임 맞춰서 드래그 하는 거 알고 있습니다.

이번 기회에 한 번 써 봅시다.

## Vim: 개발자는 이런 거 씁니다.

<div class="callout-blue">**✨ 실제 Vim 키맵이 궁금하면 검색해보세요. (좀 복잡한 편)**</callout>

텍스트(문서) 편집기인 Vim의 역사와 실용성을 따지면 할 말이 많지만 가장 중요한 건 역시 키보드로 모든 텍스트 조작을 편리하게 할 수 있다는 점 입니다.

물론, 개발자도 아닌데 실제 Vim과 똑같이 만들면 오히려 손에 안 맞을 가능성이 높습니다. 하지만 Vim하고 비슷하게 만들어볼 수 있습니다.

스플릿 키보드의 QMK에서 사용되는 키맵 중 하나인 [Miryoku 레이아웃](https://github.com/manna-harbour/miryoku)으로 살펴봅시다.

<div class="callout-blue">

**QMK가 뭔가요?**

QMK(Quantum Mechanical Keyboard)는 오픈소스 키보드 펌웨어입니다. 사실상 키보드가 할 수 있는 최대한의 커스터마이징을 할 수 있습니다.

[공식 문서](https://docs.qmk.fm/)

</callout>

![Bazecor: Alt nav layer with Miryoku layout](/_images/bazecormiryoku.png "Bazecor: Alt nav layer with Miryoku layout")

Miryoku 레이아웃의 Nav 레이어 일부를 복사해봤습니다.

이제 글 쓸 때, 왼손 + 오른손의 조합으로 글을 수정하거나 입력할 때 복사, 붙여넣기, 수정을 빠르게 할 수 있습니다.

그런데 눈썰미가 좋으신 분들이라면 왼손에 `Windows`, `Alt`, `Ctrl`, `Shift` 가 순서대로 있는 것을 보셨을 겁니다.

## Home row mod: 손 안 움직이는 거에 강박 있음

풀어서 봅시다.

- Home row: 타자연습 1단계 할 때 손 올라가있는 거기입니다.
    - ASDF / JKL; <- 이거
- Mod: Modifier(수정자, Mod) 키. `Windows`, `Alt`, `Ctrl`, `Shift` 키 입니다.

키보드를 사용할 때 우리 왼손은 `Windows`, `Alt`, `Ctrl`, `Shift` 누르기 바쁩니다. 이 친구들은 Modifier(Mod) 키 라고 불리는데, 아이러니하게도 우리의 손가락은 타자 칠 때의 손가락 기본 위치인 Home row(홈 행) 에 기본으로 올라와 있습니다.

Mod 키 누르자고 손을 너무 많이 이동하는 것 같아서 어디 똑똑하신 분들이 만들어낸 게 Home row mod (홈 행에 Mod) 입니다.

참고로 키보드 펌웨어로 QMK를 쓰는 사람들은 그냥 꾹 누르면 Mod 키로 작동되게 많이 씁니다.

### 저도 QMK 쓸래요

지원되는 키보드를 구매하시거나(KeyChron 같은 기업) 직접 키보드 조립하시면 됩니다.

## 의외로 정답은 없음

다음은 위 세팅에서 `Alt`키 홀드. 즉, 손을 자판에서 옮기지 않은 상태로 텍스트를 편집할 수 있는 예시 입니다.

- **한 줄 선택:** 오른손 소지 ****`End` → 왼손 검지 `Shift` 홀드 → 오른손 검지 `Home`
- **단어 선택:** 왼손 중지 `Ctrl` , 왼손 검지 `Shift` 홀드 → 오른손 `Left` / `Right`
- **문단 순서 변경:** 한줄, 여러줄 선택 후 → 오른손 약지 `Cut` → 커서 이동 후 → 오른손 검지 `Paste`

실제 풀배열 키보드를 기준으로, 해당 행위를 하는 데에는 손의 이동을 고려해야합니다. 왼손은 `Ctrl` 과 `Shift` 를 누르기 바쁠 것이고, 오른손은 방향키와 `Home`, `End` 키 까지 손이 가거나 마우스로 드래그 해야합니다.

여기에서 여러분들이 불편함을 느끼는 것들을 수정해 가며 자신의 입맛대로 쓰면 됩니다.

다음은 제가 사용 중인 설정입니다.

![Home row mod + Vim-like layer in Keyboard Manager](/_images/homerow.png "Home row mod + Vim-like layer in Keyboard Manager")

![Bazecor: My original nav layout](/_images/bazecororiginal.png "Bazecor: My original nav layout")

속도 빠르고 수정 빠르고 작업 빨리 끝나고 아무튼 인생이 편해집니다.

## 여러분들 자주 쓰는 프로그램에 응용하기

여러분들 모두가 글이나 코드 쓰는 일을 하는 게 아니라는 건 알고 있습니다.

Excel, After Effects, Figma, Anytype 등. 여러분들이 사용하시는 프로그램 전용 단축키를 넣어서 응용해보시면 되겠습니다.

Target app(대상 앱) 설정으로 똑같은 단축키도 여러개 등록할 수 있으니 입맛대로 작성하시면 생산성 수직 상승합니다.

# Chords / Combo

그런데 키를 등록하다 보면 느끼는 점이 의외로 키가 한정되어 있는 것 같습니다.

굉장히 당연한 이야기인데, 이걸 해소할 방법이 있습니다.

![TEKKEN 7: Command input list](/_images/tekken7.png "TEKKEN 7: Command input list")

게임 하시는 분들은 철권(TEKKEN), 스트리트 파이터(Street Fighter) 생각해 봅시다.

이것처럼 커맨드를 평소에도 쓰면 재미있을 것 같지 않습니까?

![Select the keys in the shortcut: Allow chords](/_images/chords.png "Select the keys in the shortcut: Allow chords")

Select(선택) 키를 수정할 때 Allow chords(동시 누르기 허용) 옵션을 키면 다음과 같이 사용할 수 있습니다.

- 더블탭: 두 번 누르기, 예시 - `Alt + Q, Q`
- 커맨드: 순서대로 누르기, 예시 - `Alt + Q, W`
- 콤보: 같은 걸 순서만 바꿔 등록한 뒤 동시에 누르기, 예시 - `Alt + Q, W` / `Alt + W, Q`

![QW Combo example](/_images/qwcombo.png "QW Combo example")

해당 예시에서 저는 `Alt + Q W` 를 동시에 누르면 `QW Combo` 라는 텍스트가 작성됩니다.

주의할 점 이라면 A키와 B키를 동시에 콤보로 넣으면, A키 및 B키를 단일로 사용할 수 없습니다. 단일키가 우선시 되기 때문에 안됩니다.

이거 하나만 알면 여러분들은 철권하듯 작업하실 수 있습니다.

## 쉬운 가이드

- 키 2개로 4가지를 사용하고자 하는 경우 더블탭과 커맨드를 사용하면 됩니다.
    - `Alt + [Q Q / W W / Q → W / W → Q]`
- 이때 커맨드를 콤보(동시에 눌러도 동일하게 작동)로 사용해도 됩니다.
    - `Alt + [Q Q / W W / Q + W]`
- 원한다면 진짜 게임처럼 커맨드를 짜도 됩니다. (커맨드 트리)
    - `Alt + [Q → W / Q → E / Q → R]`
- 당연히 콤보를 겹쳐서 사용할 수도 있습니다.
    - `Alt + [Q + W / W + E / E + R]`

이정도면 어디 프로그램 프로게이머 해도 될 것 같습니다.

# Actions

문제는 이렇게까지 거창하게 하는데 단축키 딸깍만 하는 건 너무 웅졸한 것 같습니다.

한번 액션에 대해 알아봅시다.

## Shortcuts

![Remap a shortcut: Volume keys](/_images/volumekeys.png "Remap a shortcut: Volume keys")

잘 쓰면 여러분들 키보드에는 없는 버튼, 행동도 있습니다. (일부 키보드에는 있습니다.)

- 미디어 키: 음량 조절, 뮤트도 됩니다.
- F13 ~ F24: 게임이나 툴에 매핑해서 추가 단축키 매핑시 쓰면 좋습니다.
- 브라우징용: 몇몇 마우스 옆에 붙어있는 버튼들 입니다. Vimium 과 사용하면 좋습니다.
- 개발용, 임시 키: 목록 잘 찾아보면 아시는 분들은 알법한 키들입니다.
- Numpad 키: 텐키리스는 쓰는데, 가끔 넘버패드 필요하시면 사용하기 좋습니다.
- 이외에도 많으니까 한 번 쭉 찾아보는 것을 추천드립니다.

<div class="callout-blue">

**Vimium이 뭐임?**

키보드로만 웹서핑 하게 해주는 브라우저 익스텐션입니다.

[Github](https://github.com/philc/vimium), [Chrome Web Store](https://chromewebstore.google.com/detail/vimium/dbepggeogbaibhgnhhndojpepiihcmeb), [Add-ons for Firefox](https://addons.mozilla.org/en-US/firefox/addon/vimium-ff/), [Add-ons for Firefox (한국어)](https://addons.mozilla.org/ko/firefox/addon/vimium-ff/)

</callout>

## Run Program

뭔가 많이 안쓸 것 같은데 의외로 쓸 데가 많습니다.

즐겨찾는 프로그램 등록하는 건 하수입니다.

간단한 스크립트가 작성된 Python, PowerShell 파일 (특히 매크로) 실행 시키면 기가 막힐 것 같습니다.

시간 및 날짜 작성 매크로, 빠른 실행 CLI 런처 띄우기 등. 키보드 매핑 하나 하는 것 치곤 의외로 생각나는 아이디어가 많은 것 같습니다.

## Open URI

<div class="callout-blue">

**URI가 뭔가요?**

여러분들이 알고 있는 URL(Uniform Resource Locator)은 자원이 실제로 존재하는 위치 입니다. (google.com 같은 거)

URI(Uniform Resource Identifier)는 자원의 고유 식별자 입니다.

즉, URI는 URL 을 포함하는 더 넓은 개념이라고 생각하면 됩니다. Windows 에서 특정 설정창을 열거나, 앱을 실행하는 등을 할 수 있습니다.

[mailto:retrisia@retryond.com](mailto:retrisia@retryond.com) <- 이것도 URI 입니다. (누르면 저한테 메일 보내집니다.)

</callout>

여러분들 평소 볼륨 설정 자주 만지신다면 `ms-settings:apps-volume` 치면 바로 볼륨창 띄울 수 있습니다. (물론 `Win + G` 가 더 편함)

이것 저것 설명하다 보면 100장을 써도 안되기 때문에 검색 부탁드리겠습니다. 😐

# Your Way

모든 건 여러분의 방식대로 선택하시면 됩니다.

도움이 되셨다면 Adblock, AdGuard 꺼주시면 감사드리겠습니다.

## For Experts

내가 전문가에 손가락을 더 학습시킬 의지가 있다면 이거 쓸 게 아니라 다른 프로그램 추천드립니다.

- [Kanata](https://github.com/jtroo/kanata): QMK 처럼 매핑, 매크로 등. 키보드 매핑해주는 친구입니다.
- [KMonad](https://github.com/kmonad/kmonad): 위랑 비슷합니다.
- [AutoHotKey](https://www.autohotkey.com/): 할 수 있는 폭이 더 많습니다. GUI 메뉴도 만들 수 있습니다. 대신 최적화가 조금 구립니다.
- [QMK](https://github.com/qmk/qmk_firmware) 키보드 만들기: 무엇 하나로도 만족할 수 없으면 이것 밖엔 답이 없습니다.

## Credit

- [Microsoft PowerToys](https://learn.microsoft.com/en-us/windows/powertoys/)
- [Bazecor](https://github.com/Dygmalab/Bazecor)
- [TEKKEN 7](https://www.bandainamcoent.com/games/tekken-7)

다음에도 여러분들만의 경험을 만들어 드리겠습니다.

읽어주셔서 감사합니다.

Your Way, Your Experience.