---
description: 計算參數值
ms.assetid: cc3c26ed-a007-4350-99be-0ebd94953689
title: 計算參數值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89dac0767d7d19bc4331e1a9ee032ec5b3eaae2e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106979706"
---
# <a name="calculating-parameter-values"></a>計算參數值

輸入緩衝區可能非常大。 在理想的情況下，當 SQL-DMO 處理緩衝區時，參數將會在整個批次的資料中完全遵循其曲線。 不過，每個一一點時間在計算這些值的方式方面都有一些。

-   最準確的方法是為每個不可部分完成的資料單位計算確切的值;例如，每個音訊範例。 這種方法是計算成本最高的方法。
-   另一種方法是將資料分割成一些固定大小的較小單位，例如100範例。 這種方法會建立「階梯-逐步執行」效果。 某些參數可能是可接受的。 在音訊效果中，它可能會建立可聽見的構件。
-   折衷的方法是使用先前的技巧，但在每個批次中，針對每個範例執行參數值的線性插補。

這些問題對於音訊處理特別重要。 音訊的一秒可能包含每個頻道48000個音訊樣本，這是很多要執行的計算，但 ear 對像是別名之類的成品很敏感。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體參數](media-parameters.md)
</dt> </dl>

 

 



