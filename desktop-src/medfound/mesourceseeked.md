---
description: 當媒體來源搜尋至新位置時引發。 如果來源是執行中或已暫停，而且應用程式呼叫 IMFMediaSource：： Start 的開始時間不等於目前的位置，則媒體來源會引發此事件。
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: 'MESourceSeeked 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b913089ca40895a782f3c013b752db25fe754443ae6d79b410da98e759b4b8ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941408"
---
# <a name="mesourceseeked-event"></a>MESourceSeeked 事件

當媒體來源搜尋至新位置時引發。 如果來源是執行中或已暫停，而且應用程式呼叫 [**IMFMediaSource：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 的開始時間不等於目前的位置，則媒體來源會引發此事件。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE           | 描述                                                                |
|-------------------|----------------------------------------------------------------------------|
| VT \_ I8<br/> | 新的開始位置，以 100-毫微秒單位表示。<br/> <br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Mfobjects (包含 Mfidl) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎事件](media-foundation-events.md)
</dt> </dl>

 

 




