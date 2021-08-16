---
description: 通知影片轉譯器視窗的篩選。
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: 'EC_NOTIFY_WINDOW (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355d4ec8b5b6bea55a2f32f01cc2f83aabeab84443b28e431e5b0d6155acc6d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820110"
---
# <a name="ec_notify_window"></a>EC \_ 通知 \_ 視窗

通知影片轉譯器視窗的篩選。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

 (**HWND**) 視窗的控制碼。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="default-action"></a>預設動作

DirectShow 會在內部使用此事件。 篩選圖形管理員不會將此事件傳遞至應用程式。 應用程式無法覆寫此事件的預設動作。

## <a name="remarks"></a>備註

當影片轉譯器連線時，它會檢查上游輸出釘選是否支援 [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) 介面。 如果是的話，轉譯器會將此事件傳送到上游篩選器。

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

 

 




