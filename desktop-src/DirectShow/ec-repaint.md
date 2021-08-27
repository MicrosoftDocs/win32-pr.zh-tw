---
description: 影片轉譯器需要重新繪製。
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: 'EC_REPAINT (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7edd498d84aaace460a10c88d5579c2f5a87bba42e1a5f393786134bbe727af3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102788"
---
# <a name="ec_repaint"></a>EC 重新 \_ 繪製

影片轉譯器需要重新繪製。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

 (**IUnknown** \*) 指標指向影片轉譯器輸入釘選的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)介面，或 **為 Null**。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="default-action"></a>預設動作

*LParam1* 參數可能會指定影片轉譯器的輸入圖釘。 如果是這樣，則篩選圖形管理員會尋找連接到該 pin 的輸出連接，並針對 [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) 介面進行查詢。 如果輸出釘選支援 **IMediaEventSink**，則篩選圖形管理員會呼叫 [**IMediaEventSink：： NOTIFY**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) 以使用 EC 重新 \_ 繪製事件代碼。 這可讓上游篩選器有機會重新傳送最後一個範例。

如果 *lParam1* 為 **Null**，或 pin 不支援 [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)，或如果 [**通知**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) 方法失敗，則篩選圖形管理員本身會處理 EC 重新 \_ 繪製事件。 其行為取決於圖形的狀態：

-   正在執行：忽略事件。  (轉譯器會接收資料流程中的下一個範例。 ) 
-   已暫停：將圖形搜尋至其目前的位置，藉此清除篩選並重新將資料排入佇列。
-   已停止：暫停並停止圖形，藉此將資料重新排入佇列。

篩選圖形管理員預設不會將此事件傳遞至應用程式。

## <a name="remarks"></a>備註

影片轉譯器會在收到 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息且沒有可顯示的資料時傳送此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[事件通知碼](event-notification-codes.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> </dl>

 

