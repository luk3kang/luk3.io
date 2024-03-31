---
title: 비트코인 시세 가져오기
toc: true
---

# 비트코인 시세 가져오기

바이낸스에서 제공하는 API를 사용해서 비트코인 시세(BTC/USDT)를 가져 옵니다.

## Binance에서 최신 데이터 가져오기

```js echo
const res = await fetch('https://api.binance.com/api/v3/ticker/24hr?symbol=BTCUSDT');
const data = await res.json();
```

```js
data
```

## 비교하기

현재 가격은 약 \$${Math.floor(data.lastPrice)}이네요.
2010년 $0.30와 비교한다면 ${(new Date()).getFullYear()}년에는 ${Math.round(data.lastPrice / 0.3).toLocaleString('en-us')}배나 오른 것입니다.