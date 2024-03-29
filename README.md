# 온라인 대전이 가능한 동물장기

![1_pre](https://user-images.githubusercontent.com/83110819/131839150-504af6b2-fa7a-47af-b9ec-71915831d827.png)

> 실제 존재하는 게임인 “동물장기”를 PC 환경에서 온라인 대전이 가능하게 만든 프로젝트.  
여러 사람이 온라인 상에서 게임방을 만들고 그 게임방에서 두 사람이 보드게임을 하고 플레이어가 아닌 다른 사람이 게임을 관전하는 것도 가능한 자바기반 GUI 프로그램.


## 설명 & 시연 영상
설명 & 시연 영상 : <https://www.youtube.com/watch?v=HqBfmYT2lIA>


## 실행 방법
1. server.jar 을 먼저 실행시켜서 서버포트를 입력합니다.
2. client.jar 을 실행시킨 다음 서버의 아이피(예 127.0.0.1)을 입력하고, 1번에서 입력한 서버 포트를 입력합니다.
3. client.jar 을 여러개 실행시킬때도 2번과 같은 방법으로 실행시키면 됩니다.


## 동물 장기 게임 규칙
* 각 말들은 말에 표시된 방향으로만 이동이 가능하다.
* 상대방의 말을 잡은 경우, 해당 말을 포로로 잡게 되며 포로로 잡은 말은 다음 턴부터 자신의 말로 사용 가능하다.
* 게임 판에 포로로 잡은 말을 내려놓는 행동도 턴을 소모하는 것이며 이미 말이 놓여진 곳에는 말을 내려놓을 수 없다.
* 병아리는 상대 진영에 들어가면 닭으로 변한다.
* 상대방의 닭을 잡아 자신의 말로 사용할 경우에는 병아리로 사용해야 한다.
* 상대방의 사자(왕)를 잡으면 해당 플레이어의 승리로 종료된다.
* 자신의 사자(왕)가 상대방의 진영에 들어가 자신의 턴이 다시 돌아올 때까지 한 턴을 버틸 경우 해당 플레이어의 승리로 게임이 종료된다.

_동물 장기 규칙에서 포로말을 상대방 진영에 놓을 수 있다는 것과 무승부 조건을 제외하면 십이장기 규칙과 완전히 같아집니다._


## 클라이언트, 서버 기능
* 관전 기능 : 같은 방에 있는 두 플레이어의 경기를 관전할 수 있다. (관전을 하기 위해서는 게임이 시작되기 전에 방에 입장을 해야한다.)
* 클라이언트 명령어
  - `#skin` : 채팅창에 #skin을 입력하면 장기 말의 이미지를 바꿔준다
  - `#G` : 방 제목 끝에 #G를 추가하면 상대방 진영에 포로 말을 내려놓을 수 없다 (십이장기 규칙)

* 서버 명령어
  - `#notice <메시지>` : 현재 접속중인 모든 유저에게 메시지를 보냄
  - `#send <유저 닉네임> <메시지>` : 특정 한 유저에게 메시지를 보냄
  - `#user` : 현재 접속중인 유저 목록을 보여줌
  - `#kill <유저 닉네임>` : 특정 한 유저의 접속을 강제로 끊음
