---
description: 由封裝裝置的 IMFMediaSource 所傳送，以指出裝置已被佔用。
ms.assetid: 85EE663C-94B7-47EA-ABBA-A8371342EEB2
title: 'MEVideoCaptureDevicePreempted 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78246d6560344735167fc6efd45ba0481095534977c67dac11a76ffae0947d1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061161"
---
# <a name="mevideocapturedevicepreempted-event"></a>MEVideoCaptureDevicePreempted 事件

由封裝裝置的 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 所傳送，以指出裝置已被佔用。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE               | 描述                           |
|-----------------------|---------------------------------------|
| VT \_ 空白 <br/> | 沒有事件資料。<br/> <br/> |



## <a name="remarks"></a>備註

此事件是由封裝裝置的 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 所傳送。

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

 

 




