---
description: 當播放速率變更時由媒體來源引發。 此事件會在 IMFRateControl：： SetRate 方法以非同步方式完成之後傳送。
ms.assetid: 68a7fe64-e28a-4c20-830c-9402e1fb57f8
title: 'MESourceRateChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2af1ca671e09fc8a236ba79b36c1610635989ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113693"
---
# <a name="mesourceratechanged-event"></a>MESourceRateChanged 事件

當播放速率變更時由媒體來源引發。 此事件會在 [**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) 方法以非同步方式完成之後傳送。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE           | Description                                   |
|-------------------|-----------------------------------------------|
| VT \_ R4<br/> | 新的播放速率。<br/> <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[執行速率控制](implementing-rate-control.md)
</dt> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> <dt>

[速率控制](rate-control.md)
</dt> <dt>

[**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)
</dt> </dl>

 

 




