---
title: "Test Rouge"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - Rouge
  - Minimal Mistake
  - Code
---

Rouge는 code highlighting을 위해, Minimal Mistakes에서 사용하고 있음.

<!--more-->

## Remote Theme 에서 사용하기.

Minimal Mistakes 테마에서 remote theme starter로 시작한 경우엔, `_config.yml` 에 아예 `rouge`에 대한 설정이 없다.

때문에 `rouge`에 대한 설정을 `_config.yml`에 추가해야만 함.

다음은 `_config.yml`에서 `# Build settings` 부분에 `highlighter: rouge`를 추가한 것을 보여줌.  
(또한 `plugins` 에서 `rouge`를 추가.)

```yml
# Build settings
remote_theme: mmistakes/minimal-mistakes
markdown: kramdown
kramdown:
  syntax_highlighter: rouge
  syntax_highlighter_opts:
    block:
      line_numbers: true

# ...

# Plugins (previously gems:)
plugins:
  - jekyll-paginate
  - jekyll-sitemap
  - jekyll-gist
  - jekyll-feed
  - jemoji
  - jekyll-include-cache
  - rouge
```

또한 `Gemfile` 에서 `rouge`를 추가해야함.

아래는 `Gemfile` 로서 맨 아래 라인에 `gem rouge`가 기재됨.

```rudy
source "https://rubygems.org"

# 테마를 사용하기 위한 플러그인
gem "jekyll-remote-theme"

# 테마의 의존성 (예를 들어, Minimal Mistakes 테마를 사용하는 경우)
gem "rouge" # 코드 하이라이팅을 위한
gem "jekyll-paginate" # 페이지네이션을 위한
gem "jekyll-sitemap" # 사이트 맵 생성
gem "jekyll-gist" # GitHub Gist를 삽입하기 위한
gem "jekyll-feed" # RSS 피드 생성
gem "jemoji" # emoji 지원

# 기타 Jekyll 플러그인
group :jekyll_plugins do
  gem "jekyll-include-cache"
end

# Windows 환경에서 사용되는 경우
# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem "tzinfo-data", platforms: [:mingw, :mswin, :x64_mingw, :jruby]

# 성능 최적화를 위한
gem "wdm", "~> 0.1.0" if Gem.win_platform?
```

이후 코드는 backtick을 세개 연달아 놓고 ` ``` `코드를 기재하고 다시 세개 연달아 있는 backtick으로 기재하면 다음과 같이 보임.

```markdown

  ```python
  import numpy as np

  def test_func(a):
      n = np.array(a)
      return n
  ```

```

