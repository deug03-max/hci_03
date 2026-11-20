# 자료 지도

## 서비스
- 이름: 수덕자리
- 컨셉: 동의대학교 수덕전 2층 점심 좌석의 실시간 현황을 보여 주고, 인원에 맞는 자리를 짧게 예약해 주는 모바일 웹 서비스

## 파일 위치
| 자료 | 파일 |
|---|---|
| 서비스 기획서 | `수덕전_점심좌석_서비스_기획서.md` (편집용 원본: https://claude.ai/artifact/H8T6M2zJpqj1a9qumMWbsL) |
| 퍼소나 | `docs/research/persona-board.jpg` (페르소나 A~D 보드), `docs/research/persona-draft-patterns.png` (패턴 A, B, 미정 초안). 서비스 대표는 C, D (기획서 2절) |
| 인터뷰, 조사 | `docs/research/interview-script.hwpx` (원본), `docs/research/interview-script.md` (텍스트), `docs/research/behavior-axes.png` (행동 축별 참여자 분포) |
| 메뉴 구조 | 없음 |
| 와이어프레임 | `wireframe/` (화면 7개 `.dc.html`, 설명은 `wireframe/README.md`, 캔버스: https://claude.ai/artifact/7VqoBoFQdag8zZma8cmVa3) |
| 그 밖의 자료 | `index.html` (초기 서비스 소개 페이지), `seat-layout-editor.html` (좌석 배치도 편집기) |

## 핵심 기능 (기획서 그대로)
1. 실시간 빈자리 현황 (핵심)
2. 인원 맞춤 자리 추천 (핵심)
3. 짧은 당일 예약 (핵심)
4. 이용 예상 시간 표시·종료 10분 전 알림 (핵심)
5. 대체 장소 안내 (보조)
6. 청결 신고·정리 알림 (보조)

## 주요 사용 시나리오 (기획서 그대로)
1. 시나리오 C, 4명이 함께 먹는 경우: 현황 확인, 인원과 시간 입력 후 추천, 예약, 테이블 QR 체크인, 퇴실
2. 시나리오 D, 공강 30분 안에 끝내야 하는 경우: 수업 전 현황 확인, 자리가 없으면 대체 장소 안내, 있으면 짧게 예약 후 이동

## 화면 목록 (초안, 메뉴 구조가 없어 와이어프레임 기준으로 만듦)
| ID | 화면 이름 | 와이어프레임 파일 | 비고 |
|---|---|---|---|
| 1.0 | 학번 로그인 | `wireframe/Login.dc.html` | 캔버스 번호 0 |
| 2.0 | 좌석 현황 (홈) | `wireframe/Main.dc.html` | 캔버스 번호 1 |
| 2.1 | 자리 없음 팝업 | `wireframe/Full.dc.html` | 캔버스 번호 5, 현황 위에 뜨는 팝업 |
| 3.0 | 인원과 시간 입력, 테이블 선택 | `wireframe/Reserve.dc.html` | 캔버스 번호 2 |
| 3.1 | 예약 완료 | `wireframe/Confirm.dc.html` | 캔버스 번호 3 |
| 4.0 | 이용 중과 종료 알림 | `wireframe/InUse.dc.html` | 캔버스 번호 4 |
| 4.1 | 청결 신고 | `wireframe/Report.dc.html` | 캔버스 번호 6 |
| 4.2 | 퇴실 완료 팝업 | `wireframe/Done.dc.html` | 캔버스 번호 7, '정리해 주셔서 감사합니다' 후 2.0으로 |
| - | (빈 프레임) | `wireframe/Artboard-zhpc.dc.html` | 캔버스 Page 2, 내용 없음 |

## 비어 있는 것
- 메뉴 구조 문서가 없다. 위 화면 목록은 초안이다.
- 페르소나 보드와 행동 축 자료에는 P3, P4가 나오지만, 인터뷰 스크립트에는 P1, P2, P5~P11만 있다. 또 P8 표시가 두 번 나온다 (기획서는 응답 10건으로 셈).
- 기획서의 "대체 장소 안내" 기능과 시나리오 D 2단계에 맞는 화면이 없다. 와이어프레임 5번에서 대체 장소 목록을 뺐다.
- 로그인 화면, 테이블 다중 선택(최대 2개), 신고 사진 첨부가 와이어프레임에는 있지만 기획서 4절 기능 표에는 없다.
