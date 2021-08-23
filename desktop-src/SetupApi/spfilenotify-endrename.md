---
description: '\_當佇列完成重新命名作業時，會將 SPFILENOTIFY ENDRENAME 通知傳送至回呼常式。 即使使用者取消或發生錯誤，也會傳送此通知。'
ms.assetid: 8d5a8d17-de4f-4100-aa72-dfefeb8d4db9
title: 'SPFILENOTIFY_ENDRENAME 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f34ad30cc103e8a13277d3383bad8c2e46409eaabe6f957ace27aebc9759990
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683118"
---
# <a name="spfilenotify_endrename-message"></a>SPFILENOTIFY \_ ENDRENAME 訊息

當佇列完成重新命名作業時，會將 **SPFILENOTIFY \_ ENDRENAME** 通知傳送至回呼常式。 即使使用者取消或發生錯誤，也會傳送此通知。


```C++
SPFILENOTIFY_ENDRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標。 **FILEPATHS** 結構的 **Win32Error** 成員指出複製作業的結果。

</dd> <dt>

*Param2* 
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Setupapi.log。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[概觀](overview.md)
</dt> <dt>

[通知](notifications.md)
</dt> <dt>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




