---
description: 參數曲線
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: 參數曲線
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5130cf158271ffe3cb3da5e4e16b5fffa8a5a6994b14b9f8766fe20cdf1510ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997374"
---
# <a name="parameter-curves"></a>參數曲線

媒體參數可在一段時間後沿著曲線。 每個曲線都是由數學公式和兩個端點所描述。 每個端點都是由參考時間和曲線在該時間的值來定義。 此公式用來計算點之間的中繼值，並決定曲線的形狀。 可能的曲線如下：

-   跳
-   線性
-   Square
-   反向正方形
-   正弦函數

「跳躍」表示直接跳到結束值。 下圖顯示其他曲線。

![參數曲線](images/param-curves01.png)

數學曲線的運作方式如下。 假設某個曲線開始于時間 *t*₀，值為 *v*₀，並在時間 *t*₁的值為 *v*₁時結束。 定義曲線的兩個點是 (*t*₀、 *v*₀) 和 (*t*₁， *v*₁) 。

-   讓Δ *t* 成為曲線的總持續時間， *t*₁–*t*₀。
-   讓Δ *v* 成為開始與結束值（ *v*₁–*v*₀）之間的間隔。
-   在 *任何時候，t* ₀ **<= *t*  <=  *t*₁，let Δ *t*' = *t*–*t*₀。

![參數計算](images/param-curves02.png)

在時間 *t* 的參數值為：

*v* = f ( Δ *t*'/Δ *t* ) \* Δ *v*  +  *v*₀

其中 f (x) 是由曲線型別決定的函式：

-   線性： y = x
-   正方形： y = x ^ 2
-   反向方形： y = sqrt (x) 
-   正弦： y = \[ sin (πx –π/2) + 1 \] /2

觀察Δ *t*' < Δ *t*，所以Δ *t*'/Δ *t* 這個詞彙的範圍是從0到1。 因此，f (x) 的範圍也是從0到1，而 *v* 一律落在 *v*₀和 *v*₁之間。 無論 *v*₀ < *v*₁或反之亦然，都是如此。 換句話說，曲線 (*t*₀、 *v*₀、 *t*₁、 *v*₁) 的矩形進行系結。

針對正弦曲線， (πx –π/2 的值) 範圍從–π/2 到π/2，這表示 sin (πx –π/2) 範圍從–1到1。 然後，結果會正規化，讓 f (x) 落在 (0 – 1) 的範圍內。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體參數](media-parameters.md)
</dt> </dl>

 

 



