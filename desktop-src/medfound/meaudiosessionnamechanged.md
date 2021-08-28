---
description: 當音訊會話顯示名稱變更時，由音訊轉譯器引發。
ms.assetid: d180b145-88e1-4f85-b001-b76140ca39d8
title: 'MEAudioSessionNameChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c890421ef2dfadf5435321966eacc7773c34c18790106887f94bfd1215e82b90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957498"
---
# <a name="meaudiosessionnamechanged-event"></a>MEAudioSessionNameChanged 事件

當音訊會話顯示名稱變更時，由音訊轉譯器引發。

媒體會話將此事件轉送到應用程式。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE                | 描述                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ 不明<br/> | [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)介面的指標。<br/> <br/> |



## <a name="remarks"></a>備註

此事件是由音訊轉譯器的資料流程接收所傳送。 當音訊轉譯器收到來自音訊會話的 [**IAudioSessionEvents：： OnDisplayNameChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ondisplaynamechanged) 事件時，就會觸發此事件。

若要取得新的顯示名稱，請呼叫 [**IMFAudioPolicy：： GetDisplayName**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFAudioPolicy：： GetDisplayName**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname)
</dt> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> <dt>

[串流音訊轉譯器](streaming-audio-renderer.md)
</dt> </dl>

 

 
