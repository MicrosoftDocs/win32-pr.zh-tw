---
description: 當磁片區變更時由音訊捕獲來源傳送。
ms.assetid: 4A525D5F-9226-4277-BDB7-174BF65FE320
title: 'MECaptureAudioSessionVolumeChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a391c55e8fcebaef0f620430b12f7cdcc67364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974326"
---
# <a name="mecaptureaudiosessionvolumechanged-event"></a>MECaptureAudioSessionVolumeChanged 事件

當磁片區變更時由音訊捕獲來源傳送。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE               | Description                           |
|-----------------------|---------------------------------------|
| VT \_ 空白 <br/> | 沒有事件資料。<br/> <br/> |



## <a name="remarks"></a>備註

此事件是由音訊捕獲來源的媒體資料流程所傳送。

如果外部動作變更磁片區（例如，如果使用者透過主控台變更磁片區），音訊捕獲來源就會傳送此事件。 如果應用程式直接在來源上變更磁片區，則捕捉來源不會傳送事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




