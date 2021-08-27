---
description: 當音訊 dession 因為使用者登出 Windows 終端機服務 (WTS) 會話而中斷連線時，由音訊捕獲來源傳送。
ms.assetid: 88B24E79-FEB8-46AF-9A6C-3FB426089584
title: 'MECaptureAudioSessionDisconnected 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567df4839776ecacb5e25992f5f8cef4795186cffc53fb8abb433418066f3c40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114168"
---
# <a name="mecaptureaudiosessiondisconnected-event"></a>MECaptureAudioSessionDisconnected 事件

當音訊 dession 因為使用者登出 Windows 終端機服務 (WTS) 會話而中斷連線時，由音訊捕獲來源傳送。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE               | 描述                           |
|-----------------------|---------------------------------------|
| VT \_ 空白 <br/> | 沒有事件資料。<br/> <br/> |



## <a name="remarks"></a>備註

此事件是由音訊捕獲來源的媒體資料流程所傳送。

當捕捉來源收到來自音訊會話的 [**IAudioSessionEvents：： OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) 事件，且中斷連線原因等於 **DisconnectReasonSessionDisconnected** 時，會傳送此事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 
