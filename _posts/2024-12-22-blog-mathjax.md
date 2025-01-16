---
title: "What MathJax is"
date: 2024-12-22 22:30:45 +0900
categories: blog
tags:
    - mathjax
    - latex
---

# MathJax 소개

MathJax는 웹 페이지에서 수학식과 수학 공식을 쉽게 표시할 수 있게 해주는 JavaScript 라이브러리
LaTeX, MathML, AsciiMath와 같은 다양한 수학 마크업 언어를 지원
크로스 브라우저 호환성을 제공

# CDN 을 통해 사용하기

CDN(Content Delivery Network)을 사용하면 HTML에서 쉽게 LaTex 코드를 통해 수식을 표시할 수 있음.

다음의 코드를 `<head>` 섹션 등에 추가하면 됨.

```html
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js"></script>
```

위의 스크립트 태그는 mathjax의 버전 3이상을 CDN을 통해 로드하라는 지시를 웹브라우저에게 내림.
이 같은 방식은 외부에 존재하는 CDN 에 의존하므로 CDN의 가용성에 문제가 발생할 경우, 제대로 동작하지 않는 문제점을 가짐.
또한 CDN의 자원은 외부 자원이므로 보안상의 위험을 가지고 있음.

* 참고: [tistory 탬플릿에 추가하기](https://dsaint31.tistory.com/206)
* 참고: [vscode의 markdown에서 수식 추가하는 extension](https://ds31x.tistory.com/166)

# Download 하여 설치.

아니면 [MathJax 공식웹사이트](https://www.mathjax.org/)에서 다운로드하고, 이를 서버의 디렉토리에 업로드한 이후 해당 경로(`path`)를 다음의 스크립트에 기재하면됨.

```html
<script src="경로/to/mathjax/es5/tex-chtml.js"></script>
```
