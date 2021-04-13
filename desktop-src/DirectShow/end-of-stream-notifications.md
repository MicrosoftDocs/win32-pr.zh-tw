---
description: 資料流程結束通知
ms.assetid: cf2b13bc-5b54-4ac7-8a33-7434126fdf31
title: 資料流程結束通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53fcdfef1225aa5b93b56aeaa0d8ae9d0a8550c9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187541"
---
# <a name="end-of-stream-notifications"></a>資料流程結束通知

當來源篩選完成傳送資料時，它會在下游輸入 pin 上呼叫 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法。 下游篩選器會將呼叫傳播至下一個篩選器，依此類推。 當 **EndOfStream** 呼叫到達轉譯器時，轉譯器會將 [**EC \_ 完成**](ec-complete.md) 事件傳送至篩選圖形管理員。 如果轉譯器有多個輸入圖釘，則會 \_ 在每個輸入 pin 收到「資料流程結束」通知之後，傳遞 EC COMPLETE 事件。

篩選準則必須將 [**EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 呼叫與其他串流呼叫（例如 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)）進行序列化。  (換句話說，下游篩選準則一律必須以正確的順序接收呼叫。 ) 

在某些情況下，下游篩選器可能會在來源篩選器之前偵測到資料流程的結尾。  (例如，下游篩選可能正在剖析資料流程 ) 。在這種情況下，下游篩選器可以傳送資料流程結束通知，在這種情況下，它應該會傳回 FALSE， \_ 從 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 直到圖形停止或排清為止。 FALSE 傳回 \_ 值會通知來源篩選停止傳送資料。

### <a name="default-handling-of-ec_complete"></a>EC 完成的預設處理 \_

篩選圖形管理員預設不會將每個 EC \_ 完成事件轉寄至應用程式。 相反地，它會等到所有串流都已 \_ 完成通知 EC，然後傳送單一的 EC \_ 完成事件。 因此，應用程式會在每個資料流程完成之後接收事件。

若要判斷資料流程的數目，篩選圖形管理員會計算支援透過 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 或) [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 搜尋 (的篩選器數目，並 *具有轉譯的輸入圖釘* ，其定義為沒有對應輸出的輸入圖釘。 篩選圖形管理員會以下列兩種方式之一來判斷是否轉譯 pin：

-   Pin 的 [**IPin：： QueryInternalConnections**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryinternalconnections) 方法會在 *nPin* 參數中傳回零。
-   篩選會公開 [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) 介面，並傳回 AM \_ 篩選器 \_ \_ 的其他旗標為轉譯器 \_ 旗標 \_ 。

### <a name="end-of-stream-notifications-in-pull-mode"></a>提取模式中的資料流程結束通知

在 [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) 連接中，來源篩選不會傳送資料流程結束通知。 Instread，這是由下游篩選器（通常是剖析器篩選器）來完成。 剖析器會將 [**EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 呼叫傳送給下游。 它不會傳送一個上游給來源篩選。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[傳遞資料流程結尾](delivering-the-end-of-stream.md)
</dt> </dl>

 

 



