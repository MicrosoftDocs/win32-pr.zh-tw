---
description: 從呈現媒體資料的媒體接收器發出事件的信號。
ms.assetid: bb7db7c9-c39f-4bf4-9412-42525c4f2ea3
title: 'MERendererEvent 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c52e15bfbe97743e8af10a79cf3ef1d94626a877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191910"
---
# <a name="merendererevent-event"></a>MERendererEvent 事件

從呈現媒體資料的媒體接收器發出事件的信號。

[增強型影片](enhanced-video-renderer.md)轉譯器 (EVR) 會在收到來自 EVR 展示者的使用者事件時傳送此事件。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE           | Description                        |
|-------------------|------------------------------------|
| VT \_ I4<br/> | 事件代碼。<br/> <br/> |



## <a name="remarks"></a>備註

如果展示者以 EC 使用者或更高範圍的事件代碼來呼叫 EVR 的 **IMediaEventSink：： Notify** 方法 \_ ，則 EVR 會傳送此事件。 事件資料是傳遞給 **通知** 方法的事件程式碼。

*EventParam1* 和 *EventParam2* 在 **IMediaEventSink：： Notify**) 方法中 (的原始事件參數會被忽略，因此展示者應該將這些值設定為 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




