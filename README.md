# ARINBODY
 ARINBODY UE4 Project (UE4 ver 4.22)
 
 캐릭터 만들기 서비스의 클라이언트 프로젝트입니다.
 
# 실행 가이드

## 필수 설치 플러그인 목록

- Real time import/export : https://www.unrealengine.com/marketplace/ko/product/real-time-import
- HiSQLite3 : https://www.unrealengine.com/marketplace/ko/product/hisqlite3-sqlite3-for-ue4
- LE Extended standard library : https://www.unrealengine.com/marketplace/ko/product/low-entry-extended-standard-library
- LE File manager : https://www.unrealengine.com/marketplace/ko/product/low-entry-file-manager
- LE Json : https://www.unrealengine.com/marketplace/ko/product/low-entry-json
- Mirror animation system v2 : https://www.unrealengine.com/marketplace/ko/product/mirror-animation-system



## Data 폴더 내부 파일

### config.json
	{
		"path_speech_wav": "E:/New/wav",  - 대사 음성 파일 저장 위치
		"path_speech_marks": "E:/New/marks", - 대사 입모양 정보 파일 저장 위치
		"path_actionscript": "E:/actionscripts", - actionscript 저장 위치
	}

대사 생성기를 통해 생성한 wav, marks 파일과 스크립트 편집툴로 생성한 actionscript를 원하는 장소에 저장 후
config 파일에 경로를 지정해야 한다.

### faceExpressionList.json

캐릭터가 지을 수 있는 표정 리스트들의 블렌드 쉐잎 정보가 저장 되어있는 파일

### MotionDB.json

캐릭터의 애니메이션 목록 정보가 저장 되어있는 파일

### Sound.json

음향 효과 목록 정보가 저장 되어있는 파일

### UsedAnimation.json

스크립트 편집툴로 actionscript를 생성할때 같이 생성되는 파일로 해당 시나리오에서 사용한 애니메이션 목록 정보가 저장되어있는 파일




## 시나리오 파일 category.json

시나리오 편집 툴을 사용하여 생성한 파일 category.json을 액션스크립트가 저장되어있는 경로에 위치시켜야 함
