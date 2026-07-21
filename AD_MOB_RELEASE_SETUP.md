# Infinity Zoom 광고 출시 준비

이 문서는 Infinity Zoom의 AdMob 광고를 실제 스토어 빌드에 적용할 때 필요한 공개 웹 설정과 콘솔 작업을 기록한다. 광고 단위 ID, 키스토어 비밀번호 등 비공개 값은 이 저장소에 기록하지 않는다.

## 이 저장소가 제공하는 파일

- 개인정보처리방침: [privacy-policy.html](privacy-policy.html)
- app-ads.txt 원본: [app-ads.txt](app-ads.txt)
- 공개 개인정보처리방침 URL: <https://sdlckdrl.github.io/InfinityZoomWeb/privacy-policy.html>

`privacy-policy.html`은 Google Mobile Ads SDK와 Google User Messaging Platform(UMP), 광고와 관련해 처리될 수 있는 정보, 앱 안의 개인정보 선택 진입점을 한국어와 영어로 고지한다.

## 중요한 app-ads.txt 배포 위치

이 저장소는 GitHub Pages 프로젝트 사이트이므로 `app-ads.txt`를 여기에서 배포하면 주소가 다음과 같이 된다.

```text
https://sdlckdrl.github.io/InfinityZoomWeb/app-ads.txt
```

이 주소는 **AdMob 인증용 최종 위치가 아니다.** AdMob은 개발자 웹사이트 도메인의 최상단 파일을 확인하므로 실제로는 다음 주소가 공개되어야 한다.

```text
https://sdlckdrl.github.io/app-ads.txt
```

루트 Pages 사이트는 이미 [sdlckdrl/sdlckdrl.github.io](https://github.com/sdlckdrl/sdlckdrl.github.io) 저장소로 만들었고, 실제 파일은 위의 최종 주소에서 제공한다. Google Play Console의 개발자 웹사이트도 `https://sdlckdrl.github.io/`로 지정한다.

이 저장소의 [app-ads.txt](app-ads.txt)는 원본과 변경 이력을 보관하기 위한 동기화 사본이다. 광고 네트워크를 추가하거나 AdMob의 개인화된 안내가 바뀌면 두 저장소의 파일을 함께 갱신한다.

## 현재 공개 상태

- [x] 공개 개인정보처리방침: <https://sdlckdrl.github.io/InfinityZoomWeb/privacy-policy.html>
- [x] 개발자 웹사이트: <https://sdlckdrl.github.io/>
- [x] AdMob 루트 파일: <https://sdlckdrl.github.io/app-ads.txt>

## AdMob 콘솔에서 할 일

### 1. UMP 동의 메시지 게시

1. AdMob에서 **개인정보 보호 및 메시지**를 연다.
2. 대상 지역에 맞는 동의 메시지(예: EEA/영국용 유럽 규정 메시지)를 만든다.
3. Infinity Zoom 앱을 선택하고 메시지를 검토한 뒤 게시한다.

Android 앱은 이미 UMP로 동의 상태를 확인한 다음 실제 광고를 초기화한다. 필요한 지역에서는 사용자가 앱의 **앱 정보 → 개인정보 및 광고 설정**에서 선택을 다시 열 수 있다.

### 2. app-ads.txt 확인

1. <https://sdlckdrl.github.io/app-ads.txt>에서 파일이 공개되어 있는지 확인한다.
2. AdMob의 앱 설정에서 제공하는 개인화된 app-ads.txt 안내와 파일의 `pub-4128679666064461` 값이 같은지 확인한다.
3. AdMob의 **app-ads.txt** 상태에서 크롤링 또는 확인을 요청한다.
4. 광고 네트워크를 추가하거나 AdMob 안내가 바뀌면 루트 저장소와 이 저장소의 파일을 함께 갱신한다.

## 스토어 제출 전 확인

- Google Play Console과 Galaxy Store Seller Portal에 공개 개인정보처리방침 URL을 입력한다.
- Google Play Console의 개발자 웹사이트에는 실제 최상단 `app-ads.txt`를 제공하는 도메인을 입력한다.
- Google Play 데이터 보안 선언에는 광고 SDK가 처리할 수 있는 IP 주소, 광고 상호작용, 진단 정보, 기기·광고 식별자를 현재 SDK 동작과 맞추어 반영한다.
- UMP 메시지 게시 후 실제 기기에서 필요 지역의 동의 흐름과 개인정보 설정 진입점을 확인한다.
- AdMob에서 제공하는 최신 app-ads.txt 행을 우선하며, 계정 안내가 바뀌면 이 저장소의 [app-ads.txt](app-ads.txt)도 함께 갱신한다.

## 배포 후 확인 주소

```text
개인정보처리방침: https://sdlckdrl.github.io/InfinityZoomWeb/privacy-policy.html
app-ads.txt 최종 주소: https://sdlckdrl.github.io/app-ads.txt
```
