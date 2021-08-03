---
id: 
title: 'study_csp'
desc: ''
updated: 
created: 
---

# 도메인 - 자산 보안

    - data in transit : VPN
    - 데이터 위생처리 : 왠만한 기술로 복구되지 않을 정도로 없애 버리는 것


# 도메인3 - 보안 엔지니어링 (I)

    1. 암호화 정의와 암호화의 역사
        1) 대표적인 고전암호 : 시저(Caesar), 비게네르(Vigenere), 스키타일 (Scytale) - 암호문을 적은 테이프를 둥근막대에 감으면 해독
        2) 2단계 근대 암호 : ENIGMA(Rotor Machine)
        3) Claude Shannon - 일회성 암호가 안전함을 증명 
        혼돈(confusion) - 암호문과 평문의 상관관계를 숨김(ㅛ)
        확산(diffusion) - 평문의 통계적 성질을 암호문 전반에 퍼트려 숨김 (규칙성을 가지고 **위치** 변화함)

    2. 암호 시스템의 강도와 목표
        3. 암호화 시스템의 주요 요소 (암호의 3요소)
            1. 알고리즘(수학적 함수)
            2. 암호화 키 
            3. 키의 길이
        Work Factor를 높이기 위한 노력을 기울여 안전한 암호기술을 구현하는 것이 목표 
    
    3. 암호의 종류 
        1. 대체 암호 (Substitution Cipher) : 글자를 다른 글자로 바꾸는 방법 
            [구성] substitution = confusion (구성이 달라짐 A->E, B ->F)
                - 시저암호, vigenere, rotor(근대식 ENIGMA), Hill
            [배열] Transposition = Permutation = Diffusion (글자 위치에 변화를 줌)
                - skytale
    
    3. Steganography
        1. 메세지를 숨기는 모든 기술
        2. 


# 도메인3 - 보안 엔지니어링 (II)

    1. 기본 보안 모델 개념 

        - BLP(벨-라파둘라) 기밀성 모델  - MAC 기술 사용 
            - 군사용 보안 구조의 요구사항을 충족하기 위해 설게 
            - 정보를 등급을 나누어 분류 --> MAC 
            - NRU (No Read Up)
            - NRD (No Read Down)

        - Biba 무결성 모델 - 아래로 읽을 수 없는 모델!
            - 중요한 정보들이 신뢰성이 약한 정보들과 결합하여 본래의 비밀 등급이 깨짐 
            - NRD (No Read Down)
            - NWU (No Write Up)

        - 클락-윌슨(Clark-Wilson) 모델 
            - 상용 어플리케이션의 보안 요구사항을 다룸 
            - 금융, 회계 관련 데이터
            - 직무분리(Duties are seperated)
            - 잘 형식화된 트랜잭션(Well-formed Transaction) 

        - 만리장성 모델(Brewer-Nash)
            - 고객단어 등장 -> 만리장성
            - 이익의 충돌 회피 (to avoid confilcts of interest)

        - Lipner 모델
            - 기밀성 + 무결성 모델 


    II. 정보시스템 보안 평가 모델

        - 인증 Certification
        - 인정 Accreditation - 경영진의 공식 승인


    4. CC : Common Criteria


    III. 정보시스템 보안 Capability 
        11. 호스트 방화벽 및 호스트 침입방지 시스템 
            - H-IDS (호스트 IDS)
                - 트로이목마, 백도어, 루트킷, 시스템로그, OS 감사증적 ('로그'단어가 키워드)
                - 임계치 탐지 : 빈도수 (Anomaly)
                - 프로파일 기반 : Misuse (시그니처 매핑,)
            - N-IDS (네트워크 IDS)
                - Application Protocol 분석 

    IV. Emanation (전자파 방사)
        - Side Channel Attack 의 대책 
        TEMPEST 인증 2가지 방식
        - 장비를 밀봉 Sheild
        - 방사물을 제대로 채집할 수 없도록 설계 Jamming 
        (최근 : Faraday cage)

    VI. 소프트웨어, 시스템 취약점 및 위협 
        1. 백도어 
            - 트랩도어 
            - Maintenance Hook  
            - 대응책 : 호스트 기반의 침입탐지 시스템 사용하여 백도어를 사용하는 공격자 감시 
        2. 루트킷 
            - 대응책 : 운영체제를 모두 새로 설치해야 함 
            - N-IDS, H-IDS 의 시그니처 기반으로 탐지 
        

    VII. 모바일 시스템 취약점 
        2. 모바일 기기 보안 전략 
            - 샌드박스 구현 및 white listing (허용목록) 구현  
    VIII. 임베디드 장비의 취약점 
        - 장비의 기밀성을 깨기 위한 공격. 
        - side channel attack 
    IX. 사이트 및 시설물 설계 고려사항 
        1. Facilities 보안
            - 연기탐지기 설치 위치 : Drip ceiling 위/아래, Raised floor 위/아래, 컴터있는 모든 방
        3. 시설물 보안 실행 및 운영
            1) 서버룸 - 랙에 대한 보안, 클라우드센터 보안 : Lock(잠금)이 답 
            4) HVAC : 전산실 내부 공기를 외부로 배출 (인명구조 우선)
            7) Shock Sensor : 도둑이 창문 파손하여 들어오는 케이스를 설명하는 경우에 답이됨. 

        4. CPTED (Crime Prevention through Environmental Design) 
            - CPTED의 3가지 원리
                1. 자연그러운 감시 (natural survaillance)
                2. 자연스러운 접근 통제 (natural access control)
                3. 관할영역 강화 (territorial reinforcement) - 셋 중 가장 효과적! 
                    - 사원들의 자존감과 소속감 형성 - 소유의식을 갖도록

