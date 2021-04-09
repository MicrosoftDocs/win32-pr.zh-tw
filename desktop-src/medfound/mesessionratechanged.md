---
description: 當播放速率變更時由媒體會話引發。 此事件會在 IMFRateControl：： SetRate 方法以非同步方式完成之後傳送。
ms.assetid: 6bef923f-4083-46e1-9a2e-49a6825467ec
title: 'MESessionRateChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4cbbd8254dfb988c94cf2016164726d578d8906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848538"
---
# <a name="mesessionratechanged-event"></a>MESessionRateChanged 事件

當播放速率變更時由媒體會話引發。 此事件會在 [**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) 方法以非同步方式完成之後傳送。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE           | Description                                                                                     |
|-------------------|-------------------------------------------------------------------------------------------------|
| VT \_ R4<br/> | 新的播放速率，以正常播放速率的比率表示。<br/> <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




