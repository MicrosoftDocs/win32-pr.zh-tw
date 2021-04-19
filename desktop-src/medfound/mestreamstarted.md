---
description: 當來源啟動但未搜尋時，由媒體資料流程引發。 當媒體來源引發 MESourceStarted 事件時，媒體資料流程會引發此事件。
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: 'MEStreamStarted 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479726c1295b4497080b2e15abdde1558f0d4888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977820"
---
# <a name="mestreamstarted-event"></a>MEStreamStarted 事件

當來源啟動但未搜尋時，由媒體資料流程引發。 當媒體來源引發 [MESourceStarted](mesourcestarted.md) 事件時，媒體資料流程會引發此事件。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | Description                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/>                                                                          |
| VT \_ I8<br/>    | 相對於樣本上時間戳記的開始時間，以 100-毫微秒單位為單位。<br/> <br/> |



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

 

 




