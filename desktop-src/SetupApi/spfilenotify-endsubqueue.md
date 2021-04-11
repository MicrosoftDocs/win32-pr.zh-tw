---
description: '\_當佇列完成刪除、重新命名或複製子佇列中的所有作業時，會將 SPFILENOTIFY ENDSUBQUEUE 通知傳送至回呼函數。'
ms.assetid: 76bd027a-0f00-46e3-b502-0c97827308a8
title: 'SPFILENOTIFY_ENDSUBQUEUE 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7eadc7546487b308313b7cb31088a22420e27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027486"
---
# <a name="spfilenotify_endsubqueue-message"></a>SPFILENOTIFY \_ ENDSUBQUEUE 訊息

當佇列完成刪除、重新命名或複製子佇列中的所有作業時，會將 **SPFILENOTIFY \_ ENDSUBQUEUE** 通知傳送至回呼函數。


```C++
SPFILENOTIFY_ENDSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

已完成的子佇列。 這個參數可以是下列其中一個值 FILEOP \_ DELETE、FILEOP \_ RENAME 或 FILEOP \_ COPY。

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
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Setupapi.log。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[概觀](overview.md)
</dt> <dt>

[通知](notifications.md)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




