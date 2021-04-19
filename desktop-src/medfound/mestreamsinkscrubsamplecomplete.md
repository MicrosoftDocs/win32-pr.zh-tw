---
description: 當資料流程接收完成清除要求時引發。
ms.assetid: 451c7e09-868e-4c05-b970-d222b97223f2
title: 'MEStreamSinkScrubSampleComplete 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81f29d478635d5a9ba7e7c5356c49ebd8da216f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983880"
---
# <a name="mestreamsinkscrubsamplecomplete-event"></a>MEStreamSinkScrubSampleComplete 事件

當資料流程接收完成清除要求時引發。

當播放速率為零，且表示時鐘以指定的 srubbing 時間啟動時，就會進行清除。 如果媒體接收器支援清除，則每當呼叫 [**IMFClockStateSink：： OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) 方法，而播放速率為零時，每個資料流程上的每個資料流程都會引發此事件。

如果串流在清除時轉譯資料，它會在資料轉譯時立即傳送事件。 如果資料流程未轉譯資料，它會在呼叫 [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) 之後立即傳送事件。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="attributes"></a>屬性

此事件會定義下列屬性。



| 屬性                                                                              | 描述                                                                                                                                                   |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ 事件 \_ SCRUBSAMPLE \_ 時間**](mf-event-scrubsample-time-attribute.md)<br/> | 轉譯資料的呈現時間。 如果媒體接收器未在清除時轉譯資料，則不會設定此屬性。<br/> <br/> |



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
</dt> <dt>

[MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md)
</dt> </dl>

 

 




