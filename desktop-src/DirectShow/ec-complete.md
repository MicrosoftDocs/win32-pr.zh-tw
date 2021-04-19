---
description: 已轉譯特定資料流程中的所有資料。
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: 'EC_COMPLETE (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cd6d548a56173b9c6ea83426ddab3fa8556e312
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987134"
---
# <a name="ec_complete"></a>EC \_ 完成

已轉譯特定資料流程中的所有資料。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

 (**HRESULT**) 完成時的資料流程狀態。 如果播放期間未發生任何錯誤，則值為 S \_ OK。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

 (**IUnknown** \*) 零或轉譯器的 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)介面指標。

</dd> </dl>

## <a name="default-action"></a>預設動作

篩選圖形管理員預設不會將此事件轉寄至應用程式。 不過，在圖形報表中的所有串流都 **\_ 完成** 後，篩選圖形管理員會將不同的 **EC \_ 完成** 事件張貼至應用程式。

如果此事件的預設動作已停用，則應用程式會從轉譯器接收所有的 **EC \_ 完成** 事件。

## <a name="remarks"></a>備註

轉譯器篩選器會在收到資料流程結尾通知時傳送此事件。  (結束資料流程會透過 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法發出信號。 ) 篩選器會為每個資料流程只傳送一個 **EC \_ 完成** 事件。 篩選準則必須先處理任何擱置中的範例，才能傳送事件。 停止轉譯器會重設已快取的任何資料流程結束狀態。

如果已暫停轉譯器，則在呼叫 [**IMediaFilter：： Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run)方法之前，不會將 **EC \_ 完成** 傳送。 此外，它會繼續為每個轉換從 pause 傳送的 **EC \_ 完成** 事件傳送到執行，直到篩選器停止或清除為止。

篩選準則會將 *lParam2* 參數設定為 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) 指標。 如果預設動作已啟用，則篩選圖形管理員會將此參數設定為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[事件通知碼](event-notification-codes.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> <dt>

[替代影片轉譯器](alternative-video-renderers.md)
</dt> </dl>

 

 




