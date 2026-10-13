# hrd-form-gy
스마트홈

main_controller/ (RPi에서 실행되는 코드)
main_controller/
├── main.py              # 전체 프로그램 실행
├── config.py            # RS232 포트, MQTT 주소, DB 경로
├── protocol.py          # JSON 메시지 규격·검증
├── serial_manager.py    # Arduino와 RS232 통신
├── mqtt_manager.py      # 앱/HMI와 MQTT 통신
├── command_manager.py   # 명령·ACK·타임아웃 관리
├── state_manager.py     # 장치 상태·연결 상태 관리
├── db_manager.py        # DB 담당이 제공한 규격으로 저장·조회
├── requirements.txt     # 필요한 Python 패키지
├── scheduler.py ← 추가: 스케줄(타이머) 관리
├── automation_manager.py ← 추가: 자동제어 룰(온도 기반 등)
├── sensor_manager.py ← 추가: 온도/센서 수집(Arduino로부터 또는 로컬)
├── control_logic.py ← 추가: 자동/원격 간 우선순위 및 실행 정책
├── api_server.py ← 선택(REST 필요 시): 스케줄/룰 CRUD
├── main.py
└── migrations/ ← DB 변경 스크립트(스키마 업그레이드)
