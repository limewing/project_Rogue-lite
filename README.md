# project_Rogue-lite
## 처음 생각나는 대로 적은 것
- 포켓몬 불가사의던전 처럼 탑다운 형식으로 던전을 탐험하는 로그라이트  
- 플랫폼 : 모바일, PC, 스위치(서드파티 가능하다면)  
Q. 이 장르와 이 플레이 방식이 해당 플랫폼에 부합하는가?  
  
- 기본적인 공격은 매우 약하고 전투에 사용할 수 있는 액티브 스킬은 따로 존재하지 않음  
Q. 억까 가능성?(재료를 충분히 얻지 못했는데 강한적을 만남)  
  
- 던전에서 습득하게 되는 재료를 이용해 소모품을 제작하여 그것을 이용하여 전투하게 되는 방식(땅에 떨어져있거나, 몬스터를 처치하거나, 특정 아이템으로 상호작용하는 오브젝트가 있거나)  
Q.
  
- 소모품은 투척, 스크롤, 트랩, 포션으로 나뉨  
1) 먼 거리에서 공격 가능한 투척  
2) 다양한 거리를 커버 가능하지만 사용 시 마나라는 별도의 자원을 사용하는 스크롤  
3) 강력한 위력과 상태이상을 동반하지만 수동적인 트랩  
4) 플레이어를 회복하거나 일시적으로 강화시키는 포션  
Q1. 해당 분류별 밸런스를 어떻게 잡을 것인지?   
Q2. 추가적인 분류를 만들 수 없는지?  
  
- 탐험하면서 재료 뿐 아니라 그 게임동안 지속적인 피드백을 주는 유물이나 스킬을 얻을 수 있음  
Q.  
  
- 스킬은 같은 재료로 더 좋은, 혹은 더 많은 아이템을 만드는 제작법 강화를 생각중  
Q.  
  
- 유물은 플레이어의 스테이터스를 전반적으로 강화하는 것과 특정 종류의 소모품을 강화시켜줌  
Q.  
  
- 게임을 클리어하면 남은 재료들을 가지고 마을로 귀환하게 되고 그것으로 해당 지역의 새로운 재료와 제작법이 게임에 등장 할 수 있도록 해금  
Q. 남는 소모품은 어떻게 처리할까?  
  
- 던전 입장 시 
  
- 많은 재료와 귀한 재료를 소모해서 시설을 만들 수 있으며 시설에 따라 새로운 기능이 해금됨(기능 미정)  
Q.  
1) 연구소 : 퍽을 해금(재료 아이템 일정확률 추가습득, 소모품 연계, 소모품 범위증가 등등)  
Q.  
2) 공방 : 플레이어의 기본스탯을 증가시키는 장비 제작 가능(HP, 인벤토리 무게 등)  
Q.  
3) 교역소 : 특정 재료끼리 교환해주는 NPC(상인별로 취급품목 풀이 다름)  
Q.  
4) 탐험 기지 : 게임 시작시 추가적인 보급품 지급 및 가지고 갈 수 있는 아이템 추가  
Q.  
  
- 새로운 지역은 새로운 재료들과 몬스터들을 많이 볼 수 있음. 지역별 던전 특색도 존재(화산지역은 밟으면 큰 피해를 받고 화상에 걸리는 용암지대 등)  
Q1. 새로운 지역의 해금방식은 어떻게 할까?  
Q2. 해당 지역에서만 등장하는 재료를 연구를 통해 다른 지역에도 등장할 수 있게 하는 방식은 어떨까?  
Q2-1. 그렇게 한다면 해당 지역의 특색을 해치지 않으면서도 자연스럽게 재료를 얻게 하는 방식은 어떤 것이 될까?  
  
Q. 다른 사람과 함께 플레이할 수 있게 만드는건 이 장르에 어떨까? 그렇게 하고는 싶지만 모바일 플랫폼에서 그게 긍정적인 방향으로 작용할까?  
  
------------------------------------------------------------------------------------------------------------------------------------------------------  
  
필요한 기능(와이어프레임 작성 시 자세하게 생각해볼 것)  
- 랜덤 타일맵 생성(던전 생성)  
- 플레이어의 시설, 마을 창고, 장비, 조합법, 해금 지역, 클리어한 던전 등 플레이 기록 저장  
- 플레이어의 키보드 조작을 인식해 8방향으로 이동  
- 패스파인딩  
1) 마우스 클릭이나 모바일 터치 시 해당 지점으로 가장 빠른 경로로 이동, 중간에 적이나 위험한 지형지물이 시야에 들어오면 이동중지  
2) 적을 통과해서 지나갈 수 없음  
3) 적도 플레이어나 적을 통과해서 지나갈 수 없음  
- 재료, 조합법 등의 데이터베이스(Json?)  
- 습득한 조합법을 보여줄 수 있도록  
- 보유한 조합법대로 재료를 일정 갯수 차감하고 그 수에 비례해서 결과품을 인벤토리에 추가  
- 제조해둔 소모품을 임시 보관해둘 인벤토리  
- 얻는 재료들을 메모리에 할당해 저장해두고 던전 패배시 전부 삭제, 클리어시 전부 마을의 창고로 이동  
- 교역소에서 교환하는 재료가 랜덤으로 달라지고 일정 주기마다 바뀜(주기는 실제 시간 or 던전 클리어 또는 5회 연속 던전 패배)  
-  
- 연구소에서 해금하게 되는 기능에 따라 더 추가되는 기능에 따라(즉, 연구소에 퍽 무작정 추가하기 전에 구현 어떻게할지 생각해보기)  
- 어울리는 에셋...  
  
------------------------------------------------------------------------------------------------------------------------------------------------------  
  
BM은?  
1. 유료로 판매  
Q1. 모바일에는 불리하게 적용될 수도 있지 않을까?  
Q2. 유료게임은 부분유료화 게임에 비해 처음 이용자를 모으기가 굉장히 힘들 듯 한데?  
2. 유료 상품  
광고보고 유물이나 조합법 리롤 및 광고제거 유료상품?  
신 지역을 DLC로? - 이건 볼륨이 유저들을 만족시킬정도로 커야 함  
스킨? 캐릭터? - 이건 에셋쓰는이상 힘들수도 있지 않을까?  
내가 아트를 하면? - 현재로선 퀄리티가 심하게 떨어짐  
