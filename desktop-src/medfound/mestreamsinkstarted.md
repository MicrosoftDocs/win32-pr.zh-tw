---
description: 當資料流程接收完成轉換到執行中狀態時引發。
ms.assetid: 95ac658b-bec0-442d-85ef-61966b40a2f2
title: 'MEStreamSinkStarted 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407ab885da04746034b7126a8d9bb9389d2928f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978867"
---
# <a name="mestreamsinkstarted-event"></a>MEStreamSinkStarted 事件

當資料流程接收完成轉換到執行中狀態時引發。 當針對接收器的簡報時鐘呼叫 [**IMFPresentationClock：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) 方法時，會發生轉換成正在執行。 媒體接收器會透過其 [**IMFClockStateSink：： OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) 或 [**IMFClockStateSink：： OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) 方法收到通知。

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

 

 




