---
description: 在呼叫 IMFMediaSource：： Start 之後由媒體資料流程引發，會在資料流程中進行搜尋。 當媒體來源引發 MESourceSeeked 事件時，媒體資料流程會引發此事件。
ms.assetid: df06df16-711d-4262-b049-fb29f25934de
title: 'MEStreamSeeked 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7b66e2176b08c04b01fc487aac4b8218536b615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191903"
---
# <a name="mestreamseeked-event"></a>MEStreamSeeked 事件

在呼叫 [**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 之後由媒體資料流程引發，會在資料流程中進行搜尋。 當媒體來源引發 [MESourceSeeked](mesourceseeked.md) 事件時，媒體資料流程會引發此事件。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE           | Description                                                        |
|-------------------|--------------------------------------------------------------------|
| VT \_ I8<br/> | 新的開始時間，以 100-毫微秒單位表示。<br/> <br/> |



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

 

 




