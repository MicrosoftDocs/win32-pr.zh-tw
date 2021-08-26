---
description: 音訊轉譯器在音訊裝置的預設音訊格式變更時引發。 音訊轉譯器現在無效。
ms.assetid: eeef764a-f6d2-4f6e-9af3-acd5fd7bc55c
title: 'MEAudioSessionFormatChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab0464aa4bd98ec0143838762ac3fcc3efd88e03528b1d5732e2d5423a711640
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013868"
---
# <a name="meaudiosessionformatchanged-event"></a>MEAudioSessionFormatChanged 事件

音訊轉譯器在音訊裝置的預設音訊格式變更時引發。 音訊轉譯器現在無效。

媒體會話將此事件轉送到應用程式。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE                | 描述                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ 空白<br/>   | 沒有事件資料。<br/> <br/>                                                     |
| VT \_ 不明<br/> | [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)介面的指標。<br/> <br/> |



## <a name="remarks"></a>備註

此事件是由音訊轉譯器的資料流程接收所傳送。 當音訊轉譯器收到來自使用者模式音訊會話的 [**IAudioSessionEvents：： OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) 事件，而中斷連線原因等於 **DisconnectReasonFormatChanged** 時，就會觸發此事件。

[**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)指標（如果設定的話）並不實用，因為音訊資料流程不再有效。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> <dt>

[串流音訊轉譯器](streaming-audio-renderer.md)
</dt> </dl>

 

 
