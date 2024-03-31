---
theme: dashboard
title: 비트코인 시세 가져오기
toc: false
---

## Binance에서 최신 데이터 가져오기

바이낸스에서 제공하는 API를 사용해서 비트코인 시세(BTC/USDT)를 가져 옵니다.

```js echo
const res = await fetch('https://api.binance.com/api/v3/ticker/24hr?symbol=BTCUSDT');
const data = await res.json();
```

```js
data
```
<div>
  가격: ${data.lastPrice}USDT (% ${data.priceChangePercent})
</div>