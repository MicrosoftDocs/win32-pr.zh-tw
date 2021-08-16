---
description: 當音訊會話由獨佔模式連接佔用時，由音訊轉譯器引發。 音訊轉譯器現在無效。
ms.assetid: f89acfe4-14a7-4051-a816-e5e0ba8db80a
title: 'MEAudioSessionExclusiveModeOverride 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6344a5d073e9dc29777e6cb181c77bcae79da8602b830ade86646459e4d0bea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114218"
---
# <a name="meaudiosessionexclusivemodeoverride-event"></a>MEAudioSessionExclusiveModeOverride 事件

當音訊會話由獨佔模式連接佔用時，由音訊轉譯器引發。 音訊轉譯器現在無效。

媒體會話將此事件轉送到應用程式。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE                | Description                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ 空白<br/>   | 沒有事件資料。<br/> <br/>                                                     |
| VT \_ 不明<br/> | [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)介面的指標。<br/> <br/> |



## <a name="remarks"></a>備註

此事件是由音訊轉譯器的資料流程接收所傳送。 當音訊轉譯器從音訊會話接收 [**IAudioSessionEvents：： OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) 事件，而中斷連線原因等於 DisconnectReasonExclusiveModeOverride 時，就會觸發此事件。

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

 

 
