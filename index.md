---
layout: page
title: Monix
---

Asynchronous Programming for Scala and [Scala.js](http://www.scala-js.org/).

{% include github-stars.html %}

### Monix 한글문서

번역: <terdong@gmail.com>

- 이 사이트는 제가 공부용으로 개설했습니다. 혹시 문제가 생길 시 메일주세요.(This website has been opened for study purposes. but please email me if it has any problems.)
- 번역이 많이 미숙합니다. 번역이 잘못된 부분이 있다면 메일 주시면 감사하겠습니다.([원본 사이트](https://monix.io))
- 주요 프로그래밍 명사나 단어들은 원어 그대로 사용했습니다.
- 중간에 제 첨언이 들어간 부분도 있습니다.(*이텔릭으로 구분*)

## Overview

Monix는 비동기적 구조, 이벤트 기반 프로그래밍을 위한 고효율 Scala / Scala.js 라이브러리입니다.

Monix는 [ReactiveX](http://reactivex.io/)의 기능을 보다 잘 구현 한 것으로 시작하여 강력한 
첫 시작은 잘 만들어진 로 부터 시작되었습니다.

Monix는 더 강력한 함수형 프로그래밍 영향과 back-pressure(배압)를 위해 처음부터 다시 디자인되고, 스칼라 표준 라이브러리와 깔끔하게 상호 작용하도록 만들어졌으며, [Reactive Streams](http://www.reactive-streams.org/) 프로토콜과는 격이다르게 호환이 되는 상태로 [ReactiveX](http://reactivex.io/)를 적절히 구현하기 위해 시작되었습니다.

<a href="https://typelevel.org/"><img src="{{ site.baseurl }}public/images/typelevel.png" width="150" style="float:right;" align="right" /></a>

[Typelevel project](http://typelevel.org/projects/)인 Monix는 자랑스럽게도 스칼라에서 순수하고, 타입형이며, 함수형 프로그래밍의 좋은 예입니다. 반면에 성능면에서도 전혀 꿀리지 않습니다.

두드러지는 점:

- 필요한 모든 지원들과 더불어 강력한 `Observable`, `Iterant`, `Task` and `Coeval`의 데이터 타입들을 보여줌
- 필요한 모듈만 사용가능
- JVM과 [Scala.js](http://scala-js.org) 양쪽에서 구동되고, 진정한 비동기성을 위해 설계됨
- 진짜 좋은 테스트 적용범위, 코드 퀄리티 그리고 API 문서

### Presentations

{% include presentations.html %}

### Download and Usage

The packages are published on Maven Central.

- 3.x release (latest): `{{ site.version3x }}` 
  ([download source archive]({{ site.github.repo }}/archive/v{{ site.version3x }}.zip))
- 2.x release (older): `{{ site.version2x }}` 
  ([download source archive]({{ site.github.repo }}/archive/v{{ site.version2x }}.zip))

In SBT for the latest 3.x release that integrates with 
[Typelevel Cats](https://typelevel.org/cats/) out of the box
(use the `%%%` for Scala.js):

```scala
libraryDependencies += "io.monix" %% "monix" % "{{ site.version3x }}"
```

Or for the older `2.x` release:

```scala
libraryDependencies += "io.monix" %% "monix" % "{{ site.version2x }}"
```

Monix is modular by design, so you can have an à la carte experience, 
the project being divided in multiple sub-projects.

See [Usage in SBT and Maven](/docs/3x/intro/usage.html) for more details.

### Documentation

Documentation and tutorials:

- [3.x series (latest)](/docs/3x/)
- [2.x series (previous)](/docs/2x/)

API ScalaDoc: 

- [3.x]({{ site.api3x }})
- [2.x]({{ site.api2x }})
- [1.x]({{ site.api1x }})

Relevant links to dependencies:

- [Cats](https://typelevel.org/cats/)
- [Cats Effect](https://typelevel.org/cats-effect/)

## Latest News

<ol class="news-summary">
  {% for post in site.posts limit: 5 %}
  <li>
    <time itemprop="dateCreated"
      datetime="{{ post.date | date: "%Y-%m-%d" }}">
      {{ post.date | date_to_string }} »
    </time>
    <a href="{{ post.url }}">{{ post.title }}</a>
  </li>
  {% endfor %}
</ol>

## Acknowledgements

<img src="{{ site.baseurl }}public/images/logos/yklogo.png"
align="right" /> YourKit supports the Monix project with its
full-featured Java Profiler.  YourKit, LLC is the creator
[YourKit Java Profiler](http://www.yourkit.com/java/profiler/index.jsp)
and
[YourKit .NET Profiler](http://www.yourkit.com/.net/profiler/index.jsp),
innovative and intelligent tools for profiling Java and .NET
applications.

<img src="{{ site.baseurl }}public/images/logos/logo-eloquentix@2x.png" align="right" width="130" />
Development of Monix has been initiated by
[Eloquentix](http://eloquentix.com/) engineers, with
Monix being introduced at E.ON Connecting Energies, powering the next
generation energy grid solutions.

## License

```text
Copyright (c) 2014-{{ site.time | date: '%Y' }} by The Monix Project Developers.
See the project homepage at: https://monix.io

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```