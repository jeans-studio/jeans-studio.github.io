# Jeans Studio Blog 작성 가이드

이 가이드는 AI가 블로그 포스트를 작성할 때 참고하는 문서입니다.

---

## 1. 블로그 기본 정보

- **블로그 명**: Jeans Studio Blog
- **플랫폼**: Hexo 기반 정적 사이트 생성기
- **저자**: jeans-studio
- **언어**: 한국어 (ko)
- **URL**: https://jeans-studio.github.io
- **테마**: minimal

---

## 2. 파일 작성 위치 및 명명 규칙

### 파일 위치
- 모든 블로그 포스트는 `source/_posts/` 디렉토리에 저장

### 파일명 규칙
- 형식: `제목.md` (예: `my-first-post.md`)
- 영문 소문자 사용 권장
- 공백 대신 하이픈(-) 사용
- 한글 파일명도 가능하지만 영문 권장
- 예시:
  - ✅ `introduction-to-javascript.md`
  - ✅ `my-coding-journey.md`
  - ⚠️ `새로운-포스트.md` (한글, 가능하지만 비권장)
  - ❌ `My First Post.md` (공백 사용)

---

## 3. Front Matter 형식

모든 포스트는 YAML front matter로 시작해야 합니다.

### 필수 필드
```yaml
---
title: 포스트 제목
date: YYYY-MM-DD HH:mm:ss
tags: [태그1, 태그2, 태그3]
---
```

### 선택 필드 (필요시 추가)
```yaml
---
title: 포스트 제목
date: YYYY-MM-DD HH:mm:ss
tags: [태그1, 태그2]
categories: [카테고리1, 카테고리2]
description: 포스트에 대한 간단한 설명 (SEO용)
---
```

### 예시
```yaml
---
title: JavaScript 비동기 프로그래밍 완벽 가이드
date: 2026-03-23 14:30:00
tags: [javascript, async, programming]
categories: [개발, 프론트엔드]
description: JavaScript의 비동기 프로그래밍을 Promise와 async/await를 중심으로 설명합니다.
---
```

---

## 4. 글 작성 스타일 가이드

### 톤 & 보이스
- **친근하고 전문적인 톤** 사용
- 독자에게 말하듯이 작성 (존댓말 사용)
- 복잡한 개념은 쉽게 풀어서 설명
- 예시와 실용적인 정보 제공

### 글 구조
1. **서론 (Introduction)**
   - 주제 소개
   - 글을 읽어야 하는 이유
   - 독자가 얻을 수 있는 것

2. **본론 (Main Content)**
   - 논리적인 흐름으로 내용 전개
   - 섹션별로 명확한 제목 사용
   - 코드 예시, 이미지, 다이어그램 활용
   - 중요한 내용은 **굵게** 또는 `코드 형식`으로 강조

3. **결론 (Conclusion)**
   - 핵심 내용 요약
   - 다음 단계나 추가 학습 자료 제안
   - 독자에게 행동 유도 (CTA)

### 문단 작성
- 한 문단은 3-5문장 정도
- 너무 긴 문단은 피하기
- 적절한 줄바꿈으로 가독성 향상
- 리스트 적극 활용

---

## 5. 마크다운 사용 가이드

### 제목 (Headings)
```markdown
# H1 - 포스트 제목 (Front Matter에서 설정하므로 본문에서는 사용하지 않음)
## H2 - 주요 섹션
### H3 - 하위 섹션
#### H4 - 세부 항목
```

### 강조
```markdown
**굵게** 또는 __굵게__
*기울임* 또는 _기울임_
~~취소선~~
`인라인 코드`
```

### 리스트
```markdown
- 순서 없는 리스트
- 항목 2
  - 중첩 항목
  - 중첩 항목 2

1. 순서 있는 리스트
2. 항목 2
   1. 중첩 항목
   2. 중첩 항목 2
```

### 링크
```markdown
[링크 텍스트](https://example.com)
[참고 자료](https://example.com "툴팁 텍스트")
```

### 이미지
```markdown
![대체 텍스트](이미지 URL)
![설명](https://example.com/image.jpg "이미지 제목")
```

### 코드 블록
````markdown
```javascript
// 언어 지정 (구문 강조)
const greeting = "Hello, World!";
console.log(greeting);
```

```python
# Python 예시
def hello_world():
    print("Hello, World!")
```

```bash
# 터미널 명령어
npm install hexo
hexo generate
hexo deploy
```
````

### 인용구
```markdown
> 이것은 인용구입니다.
> 여러 줄로 작성할 수 있습니다.
```

### 테이블
```markdown
| 헤더1 | 헤더2 | 헤더3 |
|-------|-------|-------|
| 내용1 | 내용2 | 내용3 |
| 내용4 | 내용5 | 내용6 |
```

### 구분선
```markdown
---
또는
***
```

---

## 6. 카테고리 & 태그 전략

### 카테고리 (선택적)
주제의 큰 분류에 사용
- 개발
- 프론트엔드
- 백엔드
- 데이터베이스
- DevOps
- 튜토리얼
- 일상
- 리뷰

### 태그
구체적인 키워드나 기술 스택
- 프로그래밍 언어: `javascript`, `python`, `java`, `typescript`
- 프레임워크: `react`, `vue`, `nextjs`, `express`
- 주제: `tutorial`, `guide`, `tips`, `bestpractices`
- 기술: `async`, `api`, `database`, `testing`

### 권장사항
- 태그는 3-7개 정도가 적당
- 너무 일반적이거나 너무 구체적인 태그는 피하기
- 일관성 있는 태그 사용 (예: `javascript` vs `js`)

---

## 7. 이미지 처리

### 이미지 저장 위치
- 외부 URL 사용 권장 (CDN, Imgur, Cloudinary 등)
- 로컬 이미지는 `source/images/` 폴더에 저장
- 포스트별 이미지가 많을 경우: `source/images/포스트명/` 폴더 생성

### 이미지 삽입 예시
```markdown
![JavaScript Logo](https://example.com/js-logo.png)

<!-- 또는 로컬 이미지 -->
![내 이미지](/images/my-image.png)
```

---

## 8. 글 작성 프로세스

### AI가 글을 작성할 때 따를 단계:

1. **주제 분석**
   - 주제의 핵심 키워드 파악
   - 타겟 독자 설정
   - 글의 목적 정의

2. **개요 작성**
   - 제목 설정
   - 주요 섹션 구성
   - 필요한 예시/코드 계획

3. **파일 생성**
   - 적절한 파일명으로 `source/_posts/` 에 생성
   - Front matter 작성

4. **본문 작성**
   - 서론: 주제 소개 및 동기 부여
   - 본론: 논리적 흐름으로 내용 전개
   - 결론: 요약 및 다음 단계 제안

5. **검토**
   - 마크다운 형식 확인
   - 코드 블록 테스트
   - 링크 유효성 확인
   - 오타 및 문법 검토

---

## 9. 좋은 블로그 포스트의 특징

### ✅ DO (해야 할 것)
- **명확한 제목**: 내용을 정확히 반영하는 제목
- **가독성**: 적절한 줄바꿈, 섹션 분리, 리스트 활용
- **실용성**: 실제로 활용할 수 있는 정보 제공
- **예시**: 코드 예시, 스크린샷, 다이어그램 포함
- **맥락**: 배경 지식이나 사전 요구사항 명시
- **정확성**: 검증된 정보만 제공
- **완결성**: 시작부터 끝까지 완전한 내용

### ❌ DON'T (하지 말아야 할 것)
- 너무 짧거나 내용이 부실한 글
- 검증되지 않은 정보 제공
- 지나치게 전문적이거나 어려운 용어만 사용
- 코드 설명 없이 코드만 나열
- 깨진 링크나 잘못된 참조
- 맥락 없는 시작

---

## 10. 배포 명령어

글 작성 후 배포하는 방법:

```bash
# 1. 로컬에서 미리보기
hexo server

# 2. 정적 파일 생성
hexo generate

# 3. GitHub Pages에 배포
hexo deploy

# 또는 한 번에:
hexo generate && hexo deploy
# 줄여서:
hexo g -d
```

---

## 11. 예시 포스트 템플릿

```markdown
---
title: React Hooks 완벽 가이드 - useState와 useEffect 마스터하기
date: 2026-03-23 15:00:00
tags: [react, hooks, javascript, frontend]
categories: [개발, 프론트엔드]
description: React Hooks의 핵심인 useState와 useEffect를 실전 예제와 함께 완벽하게 이해합니다.
---

React 16.8에서 도입된 Hooks는 함수형 컴포넌트에서도 상태 관리와 라이프사이클 기능을 사용할 수 있게 해주는 혁신적인 기능입니다. 이 글에서는 가장 많이 사용되는 `useState`와 `useEffect`를 자세히 알아보겠습니다.

## useState - 상태 관리의 기본

`useState`는 함수형 컴포넌트에서 상태를 관리할 수 있게 해주는 Hook입니다.

### 기본 사용법

```javascript
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>현재 카운트: {count}</p>
      <button onClick={() => setCount(count + 1)}>
        증가
      </button>
    </div>
  );
}
```

### 주요 특징

- **초기값 설정**: `useState(initialValue)`
- **배열 구조분해**: `[state, setState]` 형태로 반환
- **여러 상태 관리 가능**: 여러 번 호출 가능

## useEffect - 사이드 이펙트 처리

`useEffect`는 컴포넌트에서 부수 효과(side effects)를 수행할 수 있게 해줍니다.

```javascript
import React, { useState, useEffect } from 'react';

function UserProfile({ userId }) {
  const [user, setUser] = useState(null);

  useEffect(() => {
    // API 호출
    fetch(`/api/users/${userId}`)
      .then(res => res.json())
      .then(data => setUser(data));
  }, [userId]); // userId가 변경될 때마다 실행

  if (!user) return <div>로딩 중...</div>;

  return (
    <div>
      <h2>{user.name}</h2>
      <p>{user.email}</p>
    </div>
  );
}
```

## 실전 팁

1. **의존성 배열 주의**: 필요한 모든 의존성을 포함해야 합니다
2. **클린업 함수**: 구독이나 타이머는 반드시 정리해야 합니다
3. **커스텀 Hooks**: 재사용 가능한 로직은 커스텀 Hook으로 분리하세요

## 결론

React Hooks는 함수형 프로그래밍의 장점을 살리면서도 강력한 기능을 제공합니다. `useState`와 `useEffect`를 마스터하면 대부분의 React 애플리케이션을 구축할 수 있습니다.

다음 글에서는 `useContext`, `useReducer`, `useMemo` 등 고급 Hooks를 다루겠습니다.

## 참고 자료

- [React 공식 문서 - Hooks](https://react.dev/reference/react)
- [useState API Reference](https://react.dev/reference/react/useState)
- [useEffect API Reference](https://react.dev/reference/react/useEffect)
```

---

## 12. 주제별 작성 가이드

### 튜토리얼 글
- 단계별로 명확하게 설명
- 각 단계마다 결과 확인
- 최종 완성 코드 제공

### 개념 설명 글
- 기본 개념부터 시작
- 비유나 실생활 예시 활용
- 점진적으로 난이도 상승

### 문제 해결 글
- 문제 상황 명확히 설명
- 원인 분석
- 해결 방법 단계별 제시
- 예방 방법 제안

### 비교/리뷰 글
- 공정한 시각 유지
- 장단점 명확히 제시
- 사용 사례별 추천
- 실제 경험 기반

---

## 13. SEO 최적화 팁

- **제목**: 명확하고 검색 가능한 키워드 포함 (50-60자)
- **description**: 메타 설명 작성 (150-160자)
- **태그**: 관련성 높은 키워드 사용
- **헤딩**: 계층 구조를 지키며 사용 (H2, H3, H4)
- **내부 링크**: 관련 포스트 연결
- **외부 링크**: 신뢰할 수 있는 출처 인용

---

## 14. 체크리스트

글 작성 완료 전 확인사항:

- [ ] Front matter 모든 필수 필드 작성
- [ ] 파일명이 규칙에 맞는지 확인
- [ ] 제목이 명확하고 검색 가능한지 확인
- [ ] 서론-본론-결론 구조 갖춤
- [ ] 코드 블록에 언어 지정
- [ ] 모든 링크가 올바르게 작동하는지 확인
- [ ] 이미지가 제대로 로드되는지 확인
- [ ] 맞춤법 및 문법 검사
- [ ] 태그와 카테고리 적절히 설정
- [ ] 로컬에서 `hexo server`로 미리보기

---

**이 가이드를 참고하여 일관성 있고 고품질의 블로그 포스트를 작성하세요!** 🚀
