---
description: 當使用大小可變大小的資料結構來傳送 TAPI 和應用程式之間的資訊時，應用程式會負責配置所需的記憶體。
ms.assetid: f1e2e864-fa10-4058-ba56-faa0ba7363a1
title: 大小可變大小的資料結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182e349079abbce93f533b1b6cd299ab7e0e883d71e9b845dfdaf52bf0275ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760193"
---
# <a name="variably-sized-data-structures"></a>大小可變大小的資料結構

當使用大小可變大小的資料結構來傳送 TAPI 和應用程式之間的資訊時，應用程式會負責配置所需的記憶體。 配置的記憶體數量至少必須夠大，才能用於資料結構的固定部分，而且是由應用程式在資料結構的 **dwTotalSize** 成員中設定。 **DwUsedSize** 和 **dwNeededSize** 成員是由 TAPI 填入。 如果 **dwTotalSize** 小於固定部分的大小，則會傳回 LINEERR/PHONEERR \_ STRUCTURETOOSMALL。 如果函數傳回成功，則會填入固定部分中的所有欄位。 **DwUsedSize** 和 **dwNeededSize** 成員可以進行比較，以判斷是否已填入所有變數部分，以及需要多少空間來填滿它們。

如果 **dwNeededSize** 等於 **dwUsedSize**，則會填入所有固定和變數部分。 如果 **dwNeededSize** 大於 **dwUsedSize**，某些變數部分可能已經填入，但已填滿的大小可變大小欄位就剛好未定義。 沒有任何變數部分會被截斷，而且因為空間不足而被截斷的變數部分，則會將兩個對應的「位移」和「大小」部分設為零來表示。 如果這些都不是零 (且) 未傳回錯誤，則會指出有效、nontruncated 的變數部分資料的位移和大小。

應用程式一律會配置並指出結構的 **dwNeededSize** 位元組，並再次呼叫 "Get" 函式，直到函式傳回 Success 且 **dwNeededSize** 等於 **dwUsedSize**，藉以保證會填入所有變數部分。 這應該會在第二次嘗試時發生，但競爭情形會導致呼叫之間的變數部分大小變更，這應該是很罕見的情況。

> [!Note]  
> 大小可變大小結構中的所有文字字串（無論編碼方式）都應該根據一般 C 字串處理慣例，以 **Null** 終止。

 

 

 



