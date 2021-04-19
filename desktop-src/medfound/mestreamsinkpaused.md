---
description: 當資料流程接收完成轉換為暫停狀態時引發。
ms.assetid: 84ab62fc-1525-433c-8af5-70659122703c
title: 'MEStreamSinkPaused 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17016285f2b88a1fc266b79f5eee45fea31f824c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984983"
---
# <a name="mestreamsinkpaused-event"></a>MEStreamSinkPaused 事件

當資料流程接收完成轉換為暫停狀態時引發。 當呼叫 [**IMFPresentationClock：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) 方法時，會在接收器的簡報時鐘上進行轉換。

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

 

 




