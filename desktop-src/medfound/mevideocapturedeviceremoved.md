---
description: 由封裝裝置的 IMFMediaSource 所傳送，表示已移除裝置。
ms.assetid: 107AFF19-B444-4B62-9217-46A99AC3632C
title: 'MEVideoCaptureDeviceRemoved 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f209dc4be6e8f45639b060de1328cb04c932463f6b76355b7538b5649a69634e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013478"
---
# <a name="mevideocapturedeviceremoved-event"></a>MEVideoCaptureDeviceRemoved 事件

由封裝裝置的 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 所傳送，表示已移除裝置。

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

 

 




