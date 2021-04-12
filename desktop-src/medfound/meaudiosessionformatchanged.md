---
description: 音訊轉譯器在音訊裝置的預設音訊格式變更時引發。 音訊轉譯器現在無效。
ms.assetid: eeef764a-f6d2-4f6e-9af3-acd5fd7bc55c
title: 'MEAudioSessionFormatChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1faddc73622c65d1eb32e0d723f576b9410d978b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848267"
---
# <a name="meaudiosessionformatchanged-event"></a>MEAudioSessionFormatChanged 事件

音訊轉譯器在音訊裝置的預設音訊格式變更時引發。 音訊轉譯器現在無效。

媒體會話將此事件轉送到應用程式。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE                | Description                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ 空白<br/>   | 沒有事件資料。<br/> <br/>                                                     |
| VT \_ 不明<br/> | [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)介面的指標。<br/> <br/> |



## <a name="remarks"></a>備註

此事件是由音訊轉譯器的資料流程接收所傳送。 當音訊轉譯器收到來自使用者模式音訊會話的 [**IAudioSessionEvents：： OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) 事件，而中斷連線原因等於 **DisconnectReasonFormatChanged** 時，就會觸發此事件。

[**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)指標（如果設定的話）並不實用，因為音訊資料流程不再有效。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> <dt>

[串流音訊轉譯器](streaming-audio-renderer.md)
</dt> </dl>

 

 
