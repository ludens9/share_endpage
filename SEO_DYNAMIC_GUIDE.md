# 브로콜리 동적 SEO 가이드라인

## 개요
이 웹사이트는 동적으로 콘텐츠가 변경되는 사이트입니다. 각 페이지/콘텐츠에 따라 SEO 요소들을 적절히 업데이트해야 합니다.

## 동적 변경이 필요한 부분들

### 1. 페이지 URL 정보
- `<link rel="canonical" href="...">` - 현재 페이지의 실제 URL
- `<meta property="og:url" content="...">` - 소셜 미디어 공유용 URL
- `sitemap.xml` - 새로운 페이지 추가 시 업데이트

### 2. 메타 태그 (SEO 기본 요소)
- `<title>` - 콘텐츠에 맞는 제목 (예: "브로콜리 - [지역명] [이벤트명] | 1인가구 자취필수템")
- `<meta name="description">` - 콘텐츠 요약 (155자 이내)
- `<meta name="keywords">` - 콘텐츠 관련 키워드 추가

### 3. 소셜 미디어 메타 태그
- `<meta property="og:title">` - 소셜 미디어 제목
- `<meta property="og:description">` - 소셜 미디어 설명
- `<meta property="og:image">` - 콘텐츠 관련 이미지
- `<meta name="twitter:title">` - 트위터 제목
- `<meta name="twitter:description">` - 트위터 설명
- `<meta name="twitter:image">` - 트위터 이미지

### 4. HTML 콘텐츠 섹션

#### 타이틀 섹션
- **키워드 영역** (`.keyword-area`): 콘텐츠 관련 키워드들
- **메인 제목** (`.main-title`): 콘텐츠 제목
- **프로필 이미지** (`.profile`): 관련 프로필들
- **프로필 카운트** (`.profile-count`): 관련 인원 수
- **날짜** (`.date`): 콘텐츠 날짜

#### 내용 섹션
- **본문 텍스트** (`.content-text`): 실제 콘텐츠 내용
- **원본 링크** (`goToOriginal()` 함수): 원본 소스 링크

#### 사진 섹션
- **이미지 파일** (`.photo-item`): 실제 사진들
- **이미지 Alt 속성**: SEO 친화적인 설명

#### 공유 기능
- **공유 링크** (`shareLink()` 함수): 현재 페이지 URL

## 구현 예시

### 1. 메타 태그 동적 변경
```html
<!-- 예시: 한성대입구역 쿱페스타 콘텐츠 -->
<title>브로콜리 - 한성대입구역 쿱페스타 | 1인가구 자취필수템</title>
<meta name="description" content="한성대입구역 쿱페스타 정보를 브로콜리에서 확인하세요. 1인가구를 위한 당근라페 체험, 공연 등 다양한 혜택을 만나보세요.">
<meta name="keywords" content="브로콜리, 1인가구, 자취, 한성대입구역, 쿱페스타, 당근라페, 체험, 공연">
```

### 2. Open Graph 동적 변경
```html
<meta property="og:title" content="한성대입구역 쿱페스타 - 브로콜리">
<meta property="og:description" content="1인가구를 위한 당근라페 체험과 공연을 즐겨보세요!">
<meta property="og:url" content="https://brocoly.kr/events/hansung-coop-festa">
<meta property="og:image" content="https://brocoly.kr/assets/events/hansung-coop-festa.jpg">
```

### 3. HTML 콘텐츠 동적 변경
```html
<!-- 키워드 -->
<div class="keyword-area">
    <span class="keyword">문화</span>
    <span class="keyword">체험</span>
    <span class="keyword">1인가구</span>
</div>

<!-- 제목 -->
<h1 class="main-title">한성대입구역 쿱페스타 - 1인가구를 위한 당근라페 체험과 공연</h1>

<!-- 이미지 Alt 속성 -->
<img src="events/festa1.jpg" alt="한성대입구역 쿱페스타 당근라페 체험 현장">
```

## 자동화 권장사항

### 1. 템플릿 시스템
- 콘텐츠 타입별 SEO 템플릿 생성
- 동적 변수 치환 시스템 구축

### 2. 이미지 최적화
- 콘텐츠별 전용 OG 이미지 생성 (1200x630px)
- 이미지 압축 및 최적화

### 3. 사이트맵 자동 업데이트
- 새 콘텐츠 추가 시 sitemap.xml 자동 업데이트
- 검색 엔진에 sitemap 제출

### 4. 구조화된 데이터
- 콘텐츠 타입에 따른 JSON-LD 구조화 데이터 추가
- 이벤트, 기사, 지역정보 등 적절한 스키마 사용

## 주의사항

1. **제목 길이**: 60자 이내 권장
2. **설명 길이**: 155자 이내 권장
3. **키워드**: 과도한 키워드 스터핑 피하기
4. **이미지 크기**: OG 이미지는 1200x630px 권장
5. **URL 구조**: SEO 친화적인 URL 구조 유지

## 테스트 도구

- [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)
- [Twitter Card Validator](https://cards-dev.twitter.com/validator)
- [Google Rich Results Test](https://search.google.com/test/rich-results)
- [SEO Meta Tags Analyzer](https://www.seoptimer.com/meta-tag-checker)

이 가이드라인을 참고하여 각 콘텐츠에 맞는 SEO 최적화를 진행하시기 바랍니다. 