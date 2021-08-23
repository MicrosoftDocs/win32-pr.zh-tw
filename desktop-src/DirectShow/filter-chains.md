---
description: 篩選鏈
ms.assetid: c17b3b58-65ab-4e83-91f2-54a995f22ddf
title: 篩選鏈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4650c49dd796ff3aa7ddecbd21076a4e217def9bfb6504149fdb740c2810b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685474"
---
# <a name="filter-chains"></a>篩選鏈

*篩選鏈* 是符合下列條件的一系列篩選準則：

-   鏈中的每個篩選器最多隻會有一個連接的輸入 pin 和一個連線的輸出 pin。
-   您可以跨越鏈中的每個篩選器，而不需要在鏈外遍歷篩選。

例如，在下圖中，篩選 A-B、C – D 和 F – G – H 是篩選鏈。 F – G – H (F – G 和 G – H) 中的每個 subchain 也是篩選鏈。 篩選鏈可以由單一篩選準則組成，因此篩選 A、B、C、D、F、G 和 H 也是不同的篩選鏈。 篩選 E 有兩個輸入連接，因此包含篩選 E 的任何篩選準則順序都不是篩選鏈。

![篩選鏈 (範例 1) ](images/filter-chain1.png)

[**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)介面提供下列方法來控制篩選鏈：



| 標籤 | 值 |
|---------------------------------------------------------------|---------------------------------|
| [**IFilterChain::StartChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-startchain)   | 啟動鏈。                 |
| [**IFilterChain::StopChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-stopchain)     | 停止鏈。                  |
| [**IFilterChain：:P auseChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-pausechain)   | 暫停鏈。                 |
| [**IFilterChain::RemoveChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-removechain) | 從圖形中移除鏈。 |



 

沒有任何特定的方法可以新增鏈。 若要加入鏈，請使用 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 方法插入新的篩選準則。 然後藉由呼叫 [**IGraphBuilder：：連線**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)、 [**IGraphBuilder：： Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)或類似的方法來連接篩選。

當圖形正在執行時，篩選鏈可以在執行和停止之間切換。 當圖形暫停時，它可以在暫停和停止之間切換。 這些是唯一可以使用篩選鏈進行的狀態轉換。

## <a name="filter-chain-guidelines"></a>篩選鏈指導方針

當您使用 **IFilterChain** 方法時，請務必確定圖形中的篩選準則可以支援篩選連結作業。 否則，您可能會造成鎖死或圖形錯誤。 連線到鏈的篩選準則必須在鏈變更狀態之後正確運作。

使用 **IFilterChain** 的最佳方式是使用一組專為連結而設計的篩選。 使用下列指導方針，以確保您的篩選準則對篩選鏈作業是安全的。 這些點會參考下圖。

![篩選鏈 (範例 2) ](images/filter-chain2.png)

-   在篩選鏈的狀態變更之前，所有在篩選鏈界限的資料處理呼叫都必須完成。 此規則適用于 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)、 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)和 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)方法。 鏈中的篩選準則必須從鏈外部篩選器所提出的這些方法呼叫傳回。鏈外的篩選準則必須從鏈內的篩選準則所進行的呼叫傳回。

例如，在上圖中，篩選 B 必須從篩選 A 完成任何資料處理呼叫，而篩選 E 必須從篩選 D 完成任何呼叫。如果釘選公開 [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) 和 [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) 介面，您可以藉由呼叫 [**IPinFlowControl：： Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) 和 [**IGraphConfig：:P ushthroughdata**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-pushthroughdata) 方法（如 [動態重新連接](dynamic-reconnection.md)中所述），將資料推送到圖形。 篩選器可能也支援用來推送資料的私用方法。

-   上游篩選準則必須預期鏈的狀態才會變更。 例如，在上圖中，假設鏈已停止，但篩選 A 呼叫 **IMemInputPin：： Receive**。 呼叫失敗，而篩選 A 的回應是停止串流。 當應用程式重新開機鏈時，不會有任何作用，因為篩選 A 已不再串流資料。
-   下游篩選器也必須預期鏈的狀態才會變更。 如果沒有，下游篩選器可能會在等候從未抵達的範例時封鎖。 例如，多工器 (MUX) 篩選器通常需要其所有輸入插針的資料。 停止某個輸入 pin 的資料流程程，可能會封鎖其他串流進行處理。 這可能會導致圖形鎖死。
-   每個從鏈外的篩選連線到鏈內篩選器的連接，都應該有自己的配置器，而不是由其他連接所共用。 當鏈變更狀態或從圖形中移除時，配置器可能會已取消認可。 如果其他連接使用相同的配置器，則無法再處理範例。
-   除非連接到鏈的篩選支援動態中斷連線，否則請勿移除鏈。 一般而言，連接的篩選準則會支援 **IPinConnection** 或 **IPinFlowControl** 介面，但可能會改為支援私用介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[動態 Graph 大樓](dynamic-graph-building.md)
</dt> </dl>

 

 



