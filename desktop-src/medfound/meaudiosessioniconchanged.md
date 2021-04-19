---
description: 當音訊會話圖示變更時，由音訊轉譯器引發。
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: 'MEAudioSessionIconChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7a12a4e82585c270206d595d32ba82c4e9e594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971044"
---
# <a name="meaudiosessioniconchanged-event"></a>MEAudioSessionIconChanged 事件

當音訊會話圖示變更時，由音訊轉譯器引發。

媒體會話將此事件轉送到應用程式。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE                | Description                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ 空白<br/>   | 沒有事件資料。<br/> <br/>                                                     |
| VT \_ 不明<br/> | [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)介面的指標。<br/> <br/> |



## <a name="remarks"></a>備註

此事件是由音訊轉譯器的資料流程接收所傳送。 當音訊轉譯器收到來自音訊會話的 [**IAudioSessionEvents：： OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) 事件時，就會觸發此事件。

若要取得新的圖示，請呼叫 [**IMFAudioPolicy：： GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFAudioPolicy::GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> <dt>

[串流音訊轉譯器](streaming-audio-renderer.md)
</dt> </dl>

 

 
