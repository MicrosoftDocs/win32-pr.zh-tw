---
description: 當音訊會話的音量或靜音狀態變更時，串流音訊轉譯器會 (SAR) 傳送。
ms.assetid: 63c37bd2-0289-407a-92f1-169eb5d2e02e
title: 'MEAudioSessionVolumeChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429edd8a26ed7f4ca1e764c7fbea1c6930c4871c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991833"
---
# <a name="meaudiosessionvolumechanged-event"></a>MEAudioSessionVolumeChanged 事件

當音訊會話的音量或靜音狀態變更時，串流音訊轉譯器會 (SAR) 傳送。

媒體會話將此事件轉送到應用程式。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE                | Description                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ 空白<br/>   | 沒有事件資料。<br/> <br/>                                                     |
| VT \_ 不明<br/> | [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)介面的指標。<br/> <br/> |



## <a name="remarks"></a>備註

此事件是由 SAR 的資料流程接收所引發。 當 SAR 從音訊會話收到 [**IAudioSessionEvents：： OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) 事件時，就會觸發此事件。 若要取得新的磁片區層級和靜音狀態，請呼叫 [**IMFSimpleAudioVolume：： GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) 和 [**IMFSimpleAudioVolume：： GetMute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute)。

如果外部動作變更磁片區，則會傳送此事件（例如，如果使用者透過系統磁片區控制程式變更磁片區 (SndVol) 。 如果應用程式直接在 SAR 上變更磁片區，則 SAR 不會傳送事件。

此外，當通道磁片區變更時，也不會傳送此事件 ([**IAudioSessionEvents：： OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)) 。

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

 

 
