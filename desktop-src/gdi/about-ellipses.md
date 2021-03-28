---
description: 橢圓形是由兩個固定點（ (f1 和 f2）所定義的封閉曲線，) 讓距離 (d1 + d2 ) 從曲線上任何點到兩個固定點的總和是常數。
ms.assetid: c4aab4cf-9575-4817-b51f-aed4e3c27d2f
title: 關於橢圓形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c6b2774da9886e25d3e1dcca7c701b034e7b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565674"
---
# <a name="about-ellipses"></a>關於橢圓形

橢圓形是由兩個固定點（ (f1 和 f2）所定義的封閉曲線，) 讓距離 (d1 + d2 ) 從曲線上任何點到兩個固定點的總和是常數。 下圖顯示使用 [**橢圓形**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) 函數繪製的橢圓形。

![顯示橢圓形、兩個固定點、兩個距離和周框矩形的圖例](images/csfsh-01.png)

呼叫 [**橢圓形**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)時，應用程式會提供橢圓周框矩形左上角和右下角的座標。 周 *框* 是完全圍繞橢圓形的最小矩形。 當系統繪製橢圓形時，如果未設定任何世界轉換，則會排除右邊和右下方。 因此，針對任何測量 x 單位寬度 x y 單位偏高的矩形，相關聯的橢圓形會依 y1 單位來測量 x1 單位寬。 如果應用程式藉由呼叫 [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) 或 [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) 函式來設定世界轉換，系統就會包含右邊和右下方。

 

 



