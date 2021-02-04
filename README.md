# ARINBODY
 ARINBODY UE4 Project (UE4 ver 4.22)
 
 캐릭터 만들기 서비스의 클라이언트 프로젝트입니다.
 
# 구성 요소
ARINBODY
Script editor
Node.js server
Scenario editor
Speech editor 대사 편집기
Mocap DB (sqlite)

 
# 실행 가이드

## 필수 설치 플러그인 목록

- Real time import/export : https://www.unrealengine.com/marketplace/ko/product/real-time-import
- HiSQLite3 : https://www.unrealengine.com/marketplace/ko/product/hisqlite3-sqlite3-for-ue4
- LE Extended standard library : https://www.unrealengine.com/marketplace/ko/product/low-entry-extended-standard-library
- LE File manager : https://www.unrealengine.com/marketplace/ko/product/low-entry-file-manager
- LE Json : https://www.unrealengine.com/marketplace/ko/product/low-entry-json
- Mirror animation system v2 : https://www.unrealengine.com/marketplace/ko/product/mirror-animation-system


## 단축키

Q : 프로그램 종료   
D : 화면에 표시되는 로그 메시지 표시/미표시 토글   
C : Script editor와 통신하기 위한 socket 통신 연결   

## 필요 준비 파일 종류

- 대사 음성 (.wav) : 대사 편집기를 통해 생성된 wav 형식 음성 파일
- 입모양 정보 (.marks) : 캐릭터 립싱크를 위해 음성파일과 매칭되는 입모양과 타이밍 정보 파일
- MotionDB (.json) : 캐릭터 애니메이션 정보 DB로 Sqlite db파일을 json 형식으로 내보내기 한 파일
- Sound (.json) : 특스 효과 사운드 정보 DB로 Sqlite db파일을 json 형식으로 내보내기 한 파일
- 액션 스크립트 (.json) : Script editor를 통해 생성된 대사와 애니메이션들의 타이밍 정보 파일
- 시나리오 정보 (.json) : category.json 파일로 Scienario editor를 통해 생성된 사용할 시나리오, 액션 스크립트 들과 순서, 재생 모드 등의 정보 파일
- config (.json) : 대사 생성기를 통해 생성한 wav, marks 파일과 스크립트 편집툴로 생성한 actionscript를 원하는 장소에 저장 후 config 파일에 경로를 지정해야 한다.   
    {
"path_speech_wav": "E:/New/wav",  - 대사 음성 파일 저장 위치
"path_speech_marks": "E:/New/marks", - 대사 입모양 정보 파일 저장 위치
"path_actionscript": "E:/actionscripts", - actionscript 저장 위치
}
   
- usedAnimation (.json) : 스크립트 편집툴로 actionscript를 생성할때 같이 생성되는 파일로 해당 시나리오에서 사용한 애니메이션 목록 정보가 저장되어있는 파일
