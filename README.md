# gift-kit-assets — 선물연가 홈페이지 이미지

홈페이지(`gift-kit-homepage-unified`)가 부르는 **구성품 사진과 키트 이미지**입니다.
GitHub Pages 로 서비스합니다 → `https://joseonlab.github.io/gift-kit-assets/`

## 왜 따로 두는가

- 구성품 사진을 공급사 주소로 그대로 불러 쓰면 **외부사이트 노출 금지**에 걸려
  배포한 뒤 사진이 사라집니다.
- 8010 이 만든 세트 이미지는 홈페이지 저장소에서 `.gitignore` 라 배포에 실리지
  않습니다. 여기에 두면 함께 나갑니다.
- 이미지가 홈페이지 저장소에 없으니 clone 과 배포가 가볍습니다.

## 무엇이 있나

```
components/{상품코드}.webp        기프트연가 구성품
brand/{H|K|L}{상품코드}.webp      헤리터(H)·코토나(K)·레스쁘리(L) 구성품
images/kits/{주소조각}/hero.webp   8010 이 만든 세트 이미지
images/kits/{주소조각}/detail-NN.webp   상세컷 조각
```

## 만드는 법

원본은 `E:\선물연가` 에 키트별로 있습니다. 여기 것은 **화면용 사본**입니다.

```
python gift-kit-automation/build_assets_site.py
```

- 폭 1600px webp 로 줄입니다 (화면에서 가장 크게 서는 곳이 860px)
- 이미 있는 파일은 건너뜁니다

## ⛔ 담지 않는 것

브랜드 **상세컷 4,060장(3.3GB)** 은 담지 않습니다. 구성품이 아니고 Pages 한도
(1GB)를 넘습니다. 그쪽은 브랜드 사이트에서 그대로 불러 씁니다.
