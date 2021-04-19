---
description: 由封裝裝置的 IMFMediaSource 所傳送，表示已移除裝置。
ms.assetid: 107AFF19-B444-4B62-9217-46A99AC3632C
title: 'MEVideoCaptureDeviceRemoved 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e3276f53f86bdce78825b94828577eab9e40954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992486"
---
# <a name="mevideocapturedeviceremoved-event"></a>MEVideoCaptureDeviceRemoved 事件

由封裝裝置的 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 所傳送，表示已移除裝置。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE               | Description                           |
|-----------------------|---------------------------------------|
| VT \_ 空白 <br/> | 沒有事件資料。<br/> <br/> |



## <a name="remarks"></a>備註

此事件是由封裝裝置的 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 所傳送。

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

 

 




