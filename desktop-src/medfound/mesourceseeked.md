---
description: 當媒體來源搜尋至新位置時引發。 如果來源是執行中或已暫停，而且應用程式呼叫 IMFMediaSource：： Start 的開始時間不等於目前的位置，則媒體來源會引發此事件。
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: 'MESourceSeeked 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589e6619b4b4147da65a327681ad4ed2eace89c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983325"
---
# <a name="mesourceseeked-event"></a>MESourceSeeked 事件

當媒體來源搜尋至新位置時引發。 如果來源是執行中或已暫停，而且應用程式呼叫 [**IMFMediaSource：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 的開始時間不等於目前的位置，則媒體來源會引發此事件。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE           | Description                                                                |
|-------------------|----------------------------------------------------------------------------|
| VT \_ I8<br/> | 新的開始位置，以 100-毫微秒單位表示。<br/> <br/> |



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

 

 




