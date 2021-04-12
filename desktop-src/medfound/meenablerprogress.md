---
description: 通知內容啟用物件的進度。 公開 IMFContentEnabler 介面的物件可以引發這個事件，以通知應用程式有關內容執行程式執行動作的進度。
ms.assetid: ec14ba9b-cfb6-4e32-870e-2436e11c308b
title: 'MEEnablerProgress 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58303835113408a7fe09436967286d5ff988acdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191915"
---
# <a name="meenablerprogress-event"></a>MEEnablerProgress 事件

通知內容啟用物件的進度。 公開 [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) 介面的物件可能會引發此事件，以通知應用程式有關內容啟用程式動作的進度。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE               | Description                                                               |
|-----------------------|---------------------------------------------------------------------------|
| VT \_ LPWSTR<br/> | 描述進度的寬字元字串。<br/> <br/> |



## <a name="remarks"></a>備註

若要接收此事件，請查詢 [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)介面的 [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)介面。 然後呼叫 [**IMFMediaEventGenerator：： BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)，如「 [媒體事件](media-event-generators.md)產生器」主題所述。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[媒體事件產生器](media-event-generators.md)
</dt> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




