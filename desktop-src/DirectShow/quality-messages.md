---
description: 品質訊息
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: 品質訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15224e147d363a6cf3f3a55971d35a3d6596d95f07b9897ab1f258cc7febad48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747698"
---
# <a name="quality-messages"></a>品質訊息

品質訊息是以 [**品質**](/windows/win32/api/strmif/ns-strmif-quality) 結構來定義。 此結構包含下列成員：

-   **輸入：** 由 [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) 列舉所定義;可能是 Famine，表示篩選接收太少資料或洪水，表示篩選器收到太多資料。
-   **比例：** 從基準1000開始，資料速率中所要求的調整。 例如，750表示75% 和1500表示150%。
-   **晚期：** 指出最近範例抵達的延遲時間的參考時間。 如果範例提早抵達，此值會是負數。
-   **時間戳記：** 最新樣本上的時間戳記。

例如，假設有時間戳記為240毫秒 (ms) 的範例會在280毫秒（資料流程時間）到達轉譯器。 轉譯器會建立 Famine 型別的品質訊息。 此範例遲到了40毫秒，因此 **晚期** 成員是400000。  (所有參考時間都是 100-毫微秒單位。 ) **時間戳記** 成員是2400000。

針對 **比例** 成員，轉譯器可能會使用執行中的平均值來計算值。 也許範例已準時抵達，此範例是異常。 在這種情況下，轉譯器可能只會要求小型更正。 另一方面，如果範例一直延遲，轉譯器可能會要求較大的修正。

品質控制是透過 [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) 介面處理。 它包含兩個方法。

-   [**通知**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)：傳送品質訊息。
-   [**SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink)：指定自訂品質管制員。

執行 **IQualityControl** 的物件會透過其 **通知** 方法接收品質訊息。 它可以處理訊息或將訊息傳遞至另一個物件。 如果應用程式呼叫物件的 **SetSink** 方法，則物件應該將品質控制項委派給指定的品質管制員。

 

 



