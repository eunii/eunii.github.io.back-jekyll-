---
title: "깃허브 블로그 만들기-콜렉션(Collection)만들기"
categories:
  - blog
---

## 1. /_config.yml파일 수정하기

```
collections:
  trip:
    output: true
    permalink: /:collection/:path/
```    
위의 내용 추가

```
defaults:
  # _trip
  - scope:
      path: ""
      type: trip
    values:
      layout: single
      author_profile: false
      share: true
      related: true
```
위의 내용 추가


## 2. _pages/trip-archive.md 파일 만들기

```
---
title: 여행
layout: collection
permalink: /trip/
collection: trip
entries_layout: grid
classes: wide

---
```
## 3._/trip/post1.md 파일 만들기

```
---
title: "Trip1"
excerpt: "첫번째 여행글 입니다.."
header:
  image: /assets/images/별그림.png
  #teaser: assets/images/unsplash-gallery-image-1-th.jpg
sidebar:
  - title: "Role"
    image: /assets/images/별그림.png
    image_alt: "logo"
    text: "Designer, Front-End Developer"
  - title: "Responsibilities"
    text: "Reuters try PR stupid commenters should isn't a business model"
gallery:
  - url: /assets/images/별그림.png
    image_path: /assets/images/별그림.png
    alt: "placeholder image 1"
  - url: /assets/images/unsplash-gallery-image-2.jpg
    image_path: /assets/images/별그림.png
    alt: "placeholder image 2"
  - url: /assets/images/unsplash-gallery-image-3.jpg
    image_path: /assets/images/별그림.png
    alt: "placeholder image 3"
categories: [아시아, 한국, korea]
tags: [hot, summer]

---

이사진은 별그림 입니다
{% include gallery caption="This is a sample gallery to go along with this case study." %}

이건 마지막 글입니다.
ude gallery caption="This is a sample gallery to go along with this case study." %}


```
## 4. 완성

![캡쳐](/assets/images/trip1.JPG)

![캡쳐](/assets/images/trip2.JPG)

## 참고:https://jekyllrb-ko.github.io/docs/collections/
