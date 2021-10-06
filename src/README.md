# 과제 간단 정리 (환경 설정은 1차 과제와 거의 동일 - 빌드를 위한 설정 추가 됨)

## 1. 프로젝트 생성
* 패키지 기본정보 선택 귀찮으니, -y 옵션 줘서 default 값으로 세팅 되도록 함
```
> npm init -y
```

## 2. 패키지(모듈) 설치
* package.json 파일에 필요한 dependency 추가 후 install
```
> npm i
```

## 3. 설정
3.1 Typescript 문법 체크 및 컴파일을 위한 설정   
* tsconfig.json 파일 생성 후 설정 추가   
* 세부 설정 정보 : <https://www.typescriptlang.org/tsconfig>   

3.2 Javascript 문법 체크를 위한 설정   
* .eslintrc.js 파일 생성 후 설정 추가   
* 세부 설정 정보 : <https://eslint.org/docs/user-guide/configuring/>

3.3 VSCode EsLint 플러그인 관련 설정 적용   
* open settings(json) - sertings.json 파일 > ESLint 플러그인 관련 설정 적용   

## 4. .gitignore 파일 생성
* 링크 참조 하여 추가 : <https://github.com/github/gitignore/blob/master/Node.gitignore>

## 5. 샘플 파일의 문제 해결
* 비동기 통신을 가정하여, Promise Type 정의   
* class의 멤버 변수 및 함수의 Type 정의   
* enum 을 활용한 타입 정의   
* 기타 등등...?   

## 6. Typescript > Javascript 컴파일
* -b 옵션을 사용하여, 다른 경로/다른 파일명의 설정파일을 참조하여 컴파일도 가능함   
* 과제는 별도의 옵션 없이 컴파일   
* 컴파일 후, js 파일 확인   
```
> tsc                           # 현재 폴더 포함, 하위 폴더의 모든 ts 파일 컴파일
> tsc -b                        # 현재 디렉토리에 있는 tsconfig.json 사용   
> tsc -b src	                # src/tsconfig.json 사용   
> tsc -b foo/prd.tsconfig.json	# foo/prd.tsconfig.json 사용   
```