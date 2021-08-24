---
description: 當我使用尖峰限制的 VBR 時，從編解碼器物件取出的平均位元速率會大於尖峰位元速率。
ms.assetid: 5fc344f8-4492-4878-802a-94606c5f33e0
title: 當我使用尖峰限制的 VBR 時，從編解碼器物件取出的平均位元速率會大於尖峰位元速率。 這有何可能？
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa27e1a03c12f854486c65d7959c66f6592da4c3fea84936ee671a911f7fa46d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011948"
---
# <a name="when-i-use-peak-constrained-vbr-the-average-bit-rate-retrieved-from-the-codec-object-is-larger-than-the-peak-bit-rate-how-is-that-possible"></a>當我使用尖峰限制的 VBR 時，從編解碼器物件取出的平均位元速率會大於尖峰位元速率。 這有何可能？

平均位元速率和尖峰位速率之間的關聯性通常會被誤解。 尖峰位速率會描述尖峰緩衝區視窗所指定的一段時間內的緩衝區條件約束。 雙通過 VBR (不受限制或尖峰限制的平均位元速率) 是檔案持續時間內每秒的平均位數。

如同有漏洞值區 [緩衝區模型](the-leaky-bucket-buffer-model.md)中所述，在一段時間內使用的實際位速率（等於緩衝區視窗）可以接近位元速率兩倍。 這是因為緩衝區定義為等於緩衝區視窗 (的位元速率乘以位元組數（以秒) 為單位），所以會以固定的速率清空。

例如，在 56 Kbps 串流的1秒內，編碼器會建立總計 59 Kb 的範例。 因此，56 Kb 的資料會在該秒內從緩衝區中移除，並將 3 Kb 保留在緩衝區中。 如果資料流程的緩衝區視窗為三秒，因此緩衝區大小總計為 168 Kb，則需要將近40秒來填滿緩衝區。 資料流程的平均位元速率 (如果其持續時間小於填滿緩衝區所花費的時間) 為 59 Kbps，即使位元速率設定為 56 Kbps 也一樣。

相同的現象也適用于尖峰位速率條件約束。 針對簡短內容，編解碼器物件在編碼完成後所計算的平均位速率可能會大於尖峰位元速率。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[常見問題集](frequentlyaskedquestions.md)
</dt> </dl>

 

 



