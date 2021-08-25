---
description: 發出嚴重錯誤的信號。 任何媒體基礎元件都可以隨時傳送此事件。 呼叫 IMFMediaEvent：： GetStatus，以取得失敗作業的錯誤碼。
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: 'MEError 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd012bf7fbb7f21f37201a67f5c203f5981be6aa16795e2a3c37d16ea268f67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941468"
---
# <a name="meerror-event"></a>MEError 事件

發出嚴重錯誤的信號。 任何媒體基礎元件都可以隨時傳送此事件。 呼叫 [**IMFMediaEvent：： GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) ，以取得失敗作業的錯誤碼。

## <a name="event-values"></a>事件值

從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。



| VARTYPE              | 描述                           |
|----------------------|---------------------------------------|
| VT \_ 空白<br/> | 沒有事件資料。<br/> <br/> |



## <a name="remarks"></a>備註

此事件只應用於非預期的錯誤。 請勿傳送此事件來表示非同步方法失敗。 如果非同步方法失敗，則會在該方法的正常事件中傳回錯誤碼。

如果串流期間發生可復原的錯誤，請傳送 [MENonFatalError](menonfatalerror.md) 事件。

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

 

 




