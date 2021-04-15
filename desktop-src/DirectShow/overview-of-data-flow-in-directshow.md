---
description: DirectShow 中的資料流程總覽
ms.assetid: a1b30592-5106-44f5-8ee0-577573670167
title: DirectShow 中的資料流程總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5a34444991d6cba62026935f5ec2d7aa4eba77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467826"
---
# <a name="overview-of-data-flow-in-directshow"></a>DirectShow 中的資料流程總覽

本節將全面探討資料流程在 DirectShow 中的運作方式。 您可以在檔的其他章節中找到詳細資料。

資料會保留在緩衝區中，這只是位元組的陣列。 每個緩衝區都是由稱為 *媒體範例* 的 COM 物件所包裝，它會執行 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面。 範例是由另一種類型的物件所建立，稱為配置器，它會執行 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面。 因為有兩個以上的 pin 連線可能共用相同的配置器，所以系統會為每個 pin 連接指派配置器。 下圖說明此程式。

![緩衝區、範例和配置器](images/dataflow.png)

每個配置器都會建立媒體範例的集區，並為每個範例配置緩衝區。 每當篩選需要填滿資料的緩衝區時，就會呼叫 [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)向配置器要求範例。 如果配置器具有目前未由其他篩選使用的任何範例， **GetBuffer** 方法會立即傳回範例的指標。 如果配置器的所有範例都在使用中，方法會封鎖，直到範例變成可用為止。 當方法傳回範例時，篩選會將資料放入緩衝區、在範例上設定適當的旗標 (通常包括時間戳記) ，並傳遞範例下游。

當轉譯器篩選器收到範例時，它會檢查時間戳記並保存到範例上，直到篩選圖形的參考時鐘指出應該呈現資料為止。 在篩選轉譯資料之後，它會釋放範例。 此範例不會回到配置器的範例集區，直到樣本的參考計數為零，這表示每個篩選都已釋放範例。 下圖說明此程式。

![以解碼等候可用媒體範例](images/dataflow2.png)

上游篩選器可能會在轉譯器之前執行，也就是，它可能會比轉譯器取用緩衝區更快地填滿緩衝區。 即使是這樣，範例也不會提早轉譯，因為轉譯器會保存每個範例，直到其呈現時間為止。 此外，上游篩選不會不慎覆寫緩衝區，因為 **GetSample** 只會傳回未使用的範例。 上游篩選器可以預先執行的數量取決於配置器集區中的樣本數。

上圖只會顯示一個配置器，但每個串流通常會有數個配置器。 因此，當轉譯器釋放範例時，它可能會有串聯效果。 下圖顯示在等候轉譯器釋放範例時，某個解碼器持有壓縮影片框架的情況。 剖析器篩選器也會等候解碼器釋放範例。

![等候範例的兩個篩選](images/dataflow3.png)

當轉譯器釋放其範例時，會傳回 **GetBuffer** 的解碼器暫止呼叫。 然後，您可以將壓縮的影片框架解碼並釋出它所保留的範例，藉此解除封鎖剖析器的暫止 **GetBuffer** 呼叫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[篩選圖形中的資料流程](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



