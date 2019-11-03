# Ubuntu install

- Ubuntu 버전: ubuntu-16.04.6-server-amd64
  - iso: http://releases.ubuntu.com/16.04.6/ubuntu-16.04.6-desktop-amd64.iso
  
 
## Ubuntu 한글 패키지 설치하기

- 터미널 실행: `ctrl + alt + t`
- 한글 패키지 설지: `sudo apt-get install fcitx-hangul`
- 우측 상단의 설정 버튼 클릭 후 `System Settings` 클릭
- `Language Support` 클릭 후 아래 순서대로 클릭
  - install > password 입력 후 Authenticate
  - **이때 Keyboard input method system을 IBus가 아닌 fcitx로 변경**
  - 재부팅 `sudo reboot`

## 한영 전환 설정

- 우측 상단의 설정 버튼 클릭 후 `System Settings` 클릭
- keyboard 클릭 
- Shortcuts Tab 클릭 후 Typing 클릭
- `Switch to Next source, Switch to Previous sourc, Compose Key, Alternative Characters Key`를 모두 `Disabled`로 선택
  - **Disabled로 선택하기 위해서는 backspace를 누르면 된다.**
- Compose Key는 Diabled를 길게 눌러 `Right Alt`를 선택
- Switch to next source는 한/영키를 눌러 `Multikey`를 선택
  - **반드시 Compose Key 설정이 먼저되어야 Multikey를 선택할 수 있다.** 
   
<hr>

- System Settings 윈도우를 닫고 상단 메뉴바 오른쪽 상단의 키보드 표시가 된 것이 fcitx인데,
  - fcitx아이콘을 눌러서 `Configure Current Input Method`를 클릭한다.
- `Only Show Current Language를 Uncheck!`(체크 풀어주고)
  - Keyboard-English(US)가 있다면 `+를 눌러 Hangul을 추가`한다. `(Korean이 아닌 Hangul이여야 한다.)`
  - Hangul이 추가된것을 확인할 수 있다.
  
- `Global Config tab`에서 
  - Trigger Input Method는 한/영키를 눌러 `Multikey`로 설정(왼쪽 오른쪽 모두)한다. 
  - Extra key for trigger input method는 `Disabled`로 설정한다. 
  - (macOS에서는 command key이므로 대신 shift+space를 선택한다.)
  - Share State Among Window는 All로 선택한다.
  
- 재부팅한다. `sudo reboot`

## 테스트 
- 한글/영어가 **한/영키**로 전환 되는지 확인한다. 
