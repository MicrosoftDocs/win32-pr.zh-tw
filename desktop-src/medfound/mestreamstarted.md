---
description: 當來源啟動但未搜尋時，由媒體資料流程引發。 當媒體來源引發 MESourceStarted 事件時，媒體資料流程會引發此事件。
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: 'MEStreamStarted 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a385516a6f0f973dd5bd0453d6c9751a0f7411a8ea43cb6acb936d8601c5272
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113938"
---
# <a name="mestreamstarted-event"></a>MEStreamStarted 事件

當來源啟動但未搜尋時，由媒體資料流程引發。 當媒體來源引發 [MESourceStarted](mesourcestarted.md) 事件時，媒體資料流程會引發此事件。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/>                                                                          |
| VT \_ I8<br/>    | 相對於樣本上時間戳記的開始時間，以 100-毫微秒單位為單位。<br/> <br/> |



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

 

 




