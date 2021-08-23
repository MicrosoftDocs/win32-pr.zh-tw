---
description: 預設品質控制項
ms.assetid: 91c4b8cf-3d24-4a11-b19c-b0297734e52b
title: 預設品質控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9df737855376db52a35476c0f01da4b850e3678ec20595ee82720b7b928237ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953129"
---
# <a name="default-quality-control"></a>預設品質控制項

[DirectShow 的基類](directshow-base-classes.md)會針對視頻品質控制項來執行一些預設行為。

品質訊息從轉譯器開始。 影片轉譯器的基類是 [**CBaseVideoRenderer**](cbasevideorenderer.md)，其行為如下：

1.  當影片轉譯器收到範例時，它會比較範例上的時間戳記與目前的參考時間。
2.  影片轉譯器會產生品質訊息。 在基類中，品質訊息的 **比例** 成員限制為 500 (50% ) 到 2000 (200% ) 。 超出此範圍的值可能會導致高品質的變更。
3.  根據預設，影片轉譯器會將品質訊息傳送至上游輸出 pin， (連接到其輸入 pin) 的 pin。 應用程式可以藉由呼叫 **SetSink** 方法來覆寫此行為。

接下來會發生什麼事取決於上游篩選準則。 一般來說，這是轉換篩選。 轉換篩選準則的基類是 [**CTransformFilter**](ctransformfilter.md)，它會使用 [**CTransformInputPin**](ctransforminputpin.md) 和 [**CTransformOutputPin**](ctransformoutputpin.md) 類別來執行輸入和輸出圖釘。 這些類別一起具有下列行為：

1.  [**CTransformOutputPin：： Notify**](ctransformoutputpin-notify.md)方法會呼叫 [**CTransformFilter：： AlterQuality**](ctransformfilter-alterquality.md)，也就是篩選基類上的私用方法。
2.  衍生的篩選可以覆寫 **AlterQuality** 來處理品質訊息。 根據預設， **AlterQuality** 會忽略品質訊息。
3.  如果 **AlterQuality** 未處理品質訊息，輸出圖釘會呼叫 [**CBaseInputPin：:P assnotify**](cbaseinputpin-passnotify.md)，也就是篩選器輸入釘上的私用方法。
4.  **PassNotify** 會將品質訊息傳遞至適當的位置，也就是下一個上游輸出 pin 或自訂品質管制員。

假設沒有任何轉換篩選器會處理品質訊息，訊息最後會到達來源篩選器上的輸出圖釘。 在基類中， [**CBasePin：： Notify**](cbasepin-notify.md) 會傳回 E \_ >notimpl。 特定來源篩選器處理品質訊息的方式視來源的本質而定。 某些來源（例如即時影片捕獲）無法執行有意義的品質控制項。 其他來源可以調整傳遞範例的速率。

下圖說明預設行為。

![基類中的品質控制](images/quality-control.png)

基底影片轉譯器會 **執行 IQualityControl：： Notify**，這表示您可以將品質訊息傳遞給轉譯器本身。 如果您將 **比例** 成員設定為小於1000的值，則影片轉譯器會在其轉譯的每個畫面格之間插入等待時間，實際上會減緩轉譯器。  (您可能會這麼做，以降低系統的使用方式。如需詳細資訊，請參閱 ) 的詳細資訊，請參閱 [**CBaseVideoRenderer：： ThrottleWait**](cbasevideorenderer-throttlewait.md)。 將 **比例** 成員設定為大於1000的值沒有任何作用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[品質控制管理](quality-control-management.md)
</dt> </dl>

 

 



