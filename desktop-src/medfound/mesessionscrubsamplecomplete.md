---
description: 當媒體會話完成清除要求時引發。
ms.assetid: 1ae97022-3fb2-4c5e-9262-d5bdc2a62bee
title: 'MESessionScrubSampleComplete 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca2fdaa6ffe9693fc6a033fd0c33ff519a73dcda3a32c303844da04e6af01404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974169"
---
# <a name="mesessionscrubsamplecomplete-event"></a>MESessionScrubSampleComplete 事件

當媒體會話完成清除要求時引發。

當播放速率為零時，應用程式呼叫 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)時，就會進行清除。 每個資料流程接收完成清除要求之後，就會引發此事件。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> <dt>

[MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md)
</dt> </dl>

 

 




