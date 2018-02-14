# 버전 매니저

Node.js 의 버전 매니저.

여러 버전의 Node.js 를 설치하고 사용할 수 있게 해준다.

## NVM

[https://github.com/creationix/nvm](https://github.com/creationix/nvm)

### 설치방법

```bash
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash
```

### 명령어

```bash
$ nvm install node           // 최신버전의 Node.js 설치
$ nvm install v8.9.0         // 특정 버전의 Node.js 설치
$ nvm uninstall v8.9.0       // 특정 버전의 Node.js 삭제

$ nvm ls                     // 설치된 Node.js 버전 확인
$ nvm ls-remote              // 설치 가능한 Node.js 버전 확인

$ nvm use v8.9.0             // 특정 버전의 Node.js 사용
$ nvm alias default v8.9.0   // 기본으로 사용할 Node.js 버전 지정
```

### .nvmrc

프로젝트 에 사용될 Node.js 버전을 지정할 수 있다.

Node.js 버전이 입력된 이 파일을 생성하면, 다른 사용자들도 아래 명령어 입력시 동일한 버전의 Node.js 를 사용할 수 있다.

```bash
$ nvm use                    // .nvmrc 에 지정된 버전의 Node.js 사용
```

# 패키지 매니저

패키지를 사용하는 과정에서 발생하는 여러 복잡한 상황 \(다운로드, 설치, 빌드, 업그레이드, 의존성관리 등\) 을 처리하기 위한 도움이 되는 소프트웨어

## npm

[https://www.npmjs.com](https://www.npmjs.com)

가장 많이 보편적으로 사용되고 있는 패키지 매니저.

현재는 Node.js 설치시 같이 설치가 된다.

## Yarn

[https://yarnpkg.com](https://yarnpkg.com)

페이스북에서 만든 패키지 매니저.

npm 의 여러 단점들을 보완하여 만들어졌다.

