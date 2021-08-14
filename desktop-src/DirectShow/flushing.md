---
description: 沖洗
ms.assetid: 868218c4-3e1a-4da0-89fa-30a9848da0e8
title: 沖洗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e70f610a68b2ca81afff736b3e7402d80e5d5675e429d1715ebebf5b640a362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401742"
---
# <a name="flushing"></a>沖洗

當篩選圖形正在執行時，任意數量的資料都可以透過圖形來移動。 其中有些可能會在佇列中等候傳遞。 有時候，篩選圖形需要儘快移除此暫止的資料，並將它取代為新的資料。 例如，在搜尋命令之後，來源篩選會從來源中的新位置產生樣本。 為了將延遲降到最低，下游篩選應捨棄在 seek 命令之前建立的任何範例。 捨棄範例的進程稱為排清 *。* 當事件改變一般的資料流程時，可讓圖形更具回應性。

提取模型會以稍微不同于推送模型的方式來處理排清。 本文一開始會描述推送模型;然後，它會描述提取模型中的差異。

清除會以兩個階段進行。

-   首先，來源篩選準則會在下游篩選器的輸入 pin 上呼叫 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 。 下游篩選器會開始拒絕上游的範例。 它也會捨棄所持有的任何範例，並將下游的 **BeginFlush** 呼叫傳送至下一個篩選準則。
-   當來源篩選器準備好要傳送新的資料時，它會在輸入 pin 上呼叫 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 。 這會對下游篩選器發出可接收新範例的信號。 下游篩選器會將 **EndFlush** 呼叫傳送至下一個篩選準則。

在 **BeginFlush** 方法中，輸入 pin 會執行下列動作：

1.  在下游輸入 pin 上呼叫 **BeginFlush** 。
2.  拒絕任何其他串流資料的呼叫，包括 **接收** 和 **EndOfStream**。
3.  從篩選器配置器解除封鎖等候範例的任何上游篩選。 某些篩選準則會取消認可其配置器的用途。
4.  離開任何區塊串流的等候。 例如，轉譯器篩選會在暫停時封鎖。 它們也會在等候于正確資料流程時間轉譯樣本時封鎖。 篩選準則必須解除封鎖，才能傳遞和拒絕佇列上游的範例。 此步驟可確保所有上游篩選器最後都會解除封鎖。

在 **EndFlush** 方法中，輸入 pin 會執行下列動作：

1.  等候所有已排入佇列的樣本被捨棄。
2.  釋放任何緩衝的資料。 此步驟有時可以在 **BeginFlush** 方法中執行。 但是， **BeginFlush** 不會與資料流程處理執行緒同步處理。 篩選準則不能在呼叫 **BeginFlush** 和 **EndFlush** 呼叫之間處理或緩衝任何其他資料。
3.  清除任何暫止 \_ 的 EC 完成通知。
4.  呼叫 **EndFlush** 下游。

此時，篩選可以再次接受範例。 所有範例保證會比排清更新。

在提取模型中，剖析器篩選器會起始清除，而不是來源篩選。 它不只會在下游篩選器上呼叫 **IPin：： BeginFlush** 和 **IPin：： EndFlush** ，也會在來源篩選的 *輸出* 釘選上呼叫 [**IAsyncReader：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-beginflush)和 [**IAsyncReader：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-endflush) 。 如果來源篩選具有暫止的讀取要求，則會捨棄這些要求。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[清除資料](flushing-data.md)
</dt> </dl>

 

 



