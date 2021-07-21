# [UE4] SnowAdventure

## 스노우 어드벤처⛄ | 블루프린트를 이용한 Unreal Toy Game

### 한국전파진흥협회(RAPA) XR콘텐츠 개발 화목금 분반

#### Team 최씨정권

---

## 구현 목록

### 타이틀

* Start / Exit Widget

게임에 들어가기 전 레벨 셋팅<br>
버튼 UI / 이벤트 / Sound 출력<br>
간단한 위젯 애니메이션<br>

### 플레이어

* Cinematic Sequence

카메라 무빙<br>
레벨이 시작되기 전 플레이어의 모습을 Cinematic Sequence를 활용하여 몰입도 형성<br>
씬이 끝나갈 때 확대되는 버튼을 통해 인게임 진입<br>

* Move

W, A, S, D 키를 이용하여 움직임<br>
3인칭 카메라 셋팅

* Attack

마우스 왼쪽 버튼으로 일반공격<br>
스노우볼 투척<br>
(일반공격의 경우 데미지 -10)<br><br><br>

마우스 오른쪽 버튼으로 특수공격<br>
범위 마법 공격<br>
(특수공격의 경우 데미지 -5)<br><br><br>

적을 죽였을 때 Kill Count 구현<br><br>

* HP / MP / Inventory

HP와 MP Bar / Inventory 구현<br>
HP는 단풍잎 아이템을 통해서 회복<br>
MP는 시간이 지나면 자동으로 조금씩 회복<br>
습득한 단풍잎은 Inventory에 표시하고 F키를 통해 사용 가능<br>

* Dialogue

돈을 습득했을 시 Count 하여 표시

* Warning Event

HP 잔량이 얼마 남지 않았을 때 경고음<br>
화면을 붉게 표시하여 위험 알림<br>

* Win / Dead Event

몬스터를 5마리 죽였을 경우 Game Win<br>
HP 게이지가 모두 소진되었을 경우 Game End<br>

---

### 몬스터 1 / 몬스터 2

* Move

플레이어 추적<br>

* Attack

#### 몬스터 1

Bullet을 term을 두고 계속 생성<br>
Bullet도 플레이어 추적<br>
1 Bullet 당 플레이어에게 주는 데미지는 -10 <br>

#### 몬스터 2

Bullet을 term없이 빠르고 끊임 없이 생성<br>
호선을 그리며 플레이어 추적<br>
1 Bullet 당 플레이어에게 주는 데미지는 -10 <br>

* 아이템 드롭

#### 돈

모든 몬스터가 죽었을 시 항상 스폰<br>
플레이어가 습득한 후 Count 하고 Destroy

#### 물약

모든 몬스터가 죽었을 시 랜덤으로 스폰<br>
플레이어가 습득한 후 인벤토리에 표시하고 Destroy
