---
description: 當資料流程接收完成轉換至已停止狀態時引發。 在接收呈現時鐘上呼叫 IMFPresentationClock Stop 方法時，會發生轉換為已停止。
ms.assetid: 1a8c7faa-4d4a-4458-ad08-a760a15dc347
title: 'MEStreamSinkStopped 事件 (Mfobjects) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e35313ab3d43c950184a82e403fa6ad0eb5b4ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027068"
---
# <a name="mestreamsinkstopped-event"></a>MEStreamSinkStopped 事件

當資料流程接收完成轉換至已停止狀態時引發。 當對接收器的呈現時鐘呼叫 [**IMFPresentationClock：： Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) 方法時，就會發生轉換為已停止。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



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

[媒體接收器](media-sinks.md)
</dt> </dl>

 

 




