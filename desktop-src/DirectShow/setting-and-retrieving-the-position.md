---
description: 設定和取出位置
ms.assetid: 06b0e2d7-9539-41ad-a631-7e8da556feeb
title: 設定和取出位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776a32eb6193ef456d693b5a133c87d800a0b64e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687383"
---
# <a name="setting-and-retrieving-the-position"></a>設定和取出位置

篩選圖形會維護兩個位置值：目前的位置和停止位置。 這些定義如下：

-   當圖形正在執行時，目前的位置會是目前的播放位置（相對於來源的開頭）。 當圖形停止或暫停時，目前的位置是串流將開始于下一個執行命令的時間點。
-   停止位置是資料流程將結束的點。 當圖形到達停止位置時，就不會再串流處理任何資料，而篩選圖形管理員會張貼 [**EC \_ 完成**](ec-complete.md) 事件。 但圖形 (不會自動切換為已停止狀態。 如需詳細資訊，請參閱 [回應事件](responding-to-events.md)。 ) 

若要取出這些值，請呼叫 [**IMediaSeeking：： GetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpositions) 方法。 傳回的值一律相對於原始媒體來源。 依預設，值為參考時間單位。 在某些情況下，您可以變更時間單位;如需詳細資訊，請參閱 [搜尋命令的時間格式](time-formats-for-seek-commands.md)。

若要搜尋新位置或設定新的停止位置，請呼叫 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 方法，如下列範例所示：


```C++
#define ONE_SECOND 10000000
REFERENCE_TIME rtNow  = 2 * ONE_SECOND, 
               rtStop = 5 * ONE_SECOND;

hr = pSeek->SetPositions(
    &rtNow,  AM_SEEKING_AbsolutePositioning, 
    &rtStop, AM_SEEKING_AbsolutePositioning
    );
```



> [!Note]  
> 一秒是10000000的參考時間單位。 為了方便起見，此範例會將此值定義為一 \_ 秒。 如果您使用的是 DirectShow 基類程式庫，常數單位會有相同的值。

 

*RtNow* 參數會指定新的目前位置。 第二個參數是定義如何解讀 *rtNow* 的旗標。 在此範例中，AM \_ 搜尋 \_ AbsolutePositioning 旗標指出 *rtNow* 在來源中指定絕對位置。 因此，篩選圖形將會從資料流程的開頭開始搜尋兩秒鐘的位置。 *RtStop* 參數會提供停止時間。 最後一個參數指定 *rtStop* 也是絕對位置。

若要指定相對於先前位置值的位置，請使用 AM \_ 搜尋 \_ RelativePositioning 旗標。 若要讓其中一個位置值保持不變，請使用 AM \_ 搜尋 \_ NoPositioning 旗標。 在該情況下，對應的 time 參數可以是 **Null** 。 下列範例會向前搜尋10秒，但不會讓停止位置保持不變：


```C++
REFERENCE_TIME rtNow = 10 * ONE_SECOND;
hr = pSeek->SetPositions(
    &rtNow, AM_SEEKING_RelativePositioning, 
    NULL, AM_SEEKING_NoPositioning
    );
```



如果篩選圖形已停止，則影片轉譯器不會在搜尋作業之後更新影像。 對使用者而言，它會顯示為搜尋未發生。 若要更新影像，請在搜尋作業之後暫停圖形。 暫停圖形會提示影片轉譯器的新影片畫面。 您可以使用 [**IMediaControl：： StopWhenReady**](/windows/desktop/api/Control/nf-control-imediacontrol-stopwhenready) 方法，它會暫停圖形，然後將它停止。

 

 



