---
description: 當資料流程接收完成轉換至已停止狀態時引發。 在接收呈現時鐘上呼叫 IMFPresentationClock Stop 方法時，會發生轉換為已停止。
ms.assetid: 1a8c7faa-4d4a-4458-ad08-a760a15dc347
title: 'MEStreamSinkStopped 事件 (Mfobjects) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7bf6a39dca8f50fed8fdd1d0137405225624999fab42771e485174ba4f0afa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715098"
---
# <a name="mestreamsinkstopped-event"></a>MEStreamSinkStopped 事件

當資料流程接收完成轉換至已停止狀態時引發。 當對接收器的呈現時鐘呼叫 [**IMFPresentationClock：： Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) 方法時，就會發生轉換為已停止。

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

[媒體接收器](media-sinks.md)
</dt> </dl>

 

 




