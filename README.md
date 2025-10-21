# TOUHOU Roguelike Shooting Game

---

## 🎮 프로젝트 개요
- **장르:** 로그라이크 슈팅  
- **플랫폼:** PC (Steam Demo 예정)  
- **엔진:** Unity (C#)  
- **개발 목표:**  
  - 살아 움직이는 환상향

---

## 🧱 게임 구조 / 시스템
- **GameManager / Event-driven Loop**  
  스테이지 진행 및 전체 게임 루프 제어  
- **Finite State Machine (FSM)**  
  플레이어 및 적 상태 관리
- **Object Pooling**  
  탄막, 이펙트, 드랍 등 고빈도 객체 재사용으로 메모리 최적화  
- **Procedural Generation (DFS 기반)**  
  방 연결 보장이 있는 로그라이크 맵 구조 자동 생성  
- **ScriptableObject / JSON Save**  
  무기, 적, 아이템 등 데이터 중심 설계  
- **UIManager / MVC Pattern**  
  UI 로직을 Model / View / Controller로 분리하여 유지보수성 확보  

---

## ⚔️ 전투 / 적 AI
- **FSM 기반 적 AI**
  일반 몬스터는 단순한 상태 전환 중심으로 구현  
- **Behavior Tree (보스/특수 적 전용)**  
  조건 기반 의사결정 구조를 도입해, HP 상황에 따른 행동 선택구현  
- **탄막 및 투사체 관리 (Object Pooling 기반)**  
  탄막 패턴과 이펙트를 효율적으로 재사용하여 성능 최적화  
- **무기 및 적 스펙을 ScriptableObject로 데이터화**  
  공격력, 체력, 쿨타임 등 수치를 코드 수정 없이 조정 가능

---

## 🧩 로그라이크 시스템
- DFS Graph Traversal 기반 방 구조 생성  
- Weighted Random으로 상점, 이벤트, 보스 룸 자동 배치  
- 랜덤 드랍 시스템  
- Seed 기반 플레이 다양성 확보  

---

## ⚙️ 퍼포먼스 / 최적화
- Object Pooling + GC Alloc Tracking으로 런타임 메모리 최소화  
- Sprite Atlas / Draw Call 관리로 60FPS 안정화  
- Profiler 기반 병목 구간 식별 및 최적화  

---

## 🧠 아키텍처 / 유지보수
- Component-based Architecture  
  모듈별 독립성 확보 및 재사용성 강화  
- Observer Pattern / C# Event  
  UI ↔ 전투 ↔ 시스템 간 결합도 최소화  
- Debug HUD / Logging System  
  실시간 상태 확인 및 테스트 효율 개선  
- Git Versioning (브랜치/태그 기반)  
  빌드별 변경 내역 및 릴리즈 추적 관리  

---

## 🧾 도구 및 개발 환경
- **Engine:** Unity (C#)  
- **IDE:** Visual Studio Code, ????
- **Version Control:** Git / GitHub  / <del>plasticSCM</del>
- **Documentation:** README / Notion  
- **Assets:** FMOD, BullerPro

---