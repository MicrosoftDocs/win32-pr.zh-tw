---
description: '\_當佇列開始處理刪除、重新命名或複製子佇列中的作業時，會將 SPFILENOTIFY STARTSUBQUEUE 通知傳送至回呼函數。'
ms.assetid: 4f971549-8f79-4995-9796-1177c3a3c416
title: 'SPFILENOTIFY_STARTSUBQUEUE 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 223fb54132721601633201ff34bd239c58d85cac4324970823b6a16496dbd5d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964078"
---
# <a name="spfilenotify_startsubqueue-message"></a>SPFILENOTIFY \_ STARTSUBQUEUE 訊息

當佇列開始處理刪除、重新命名或複製子佇列中的作業時，會將 **SPFILENOTIFY \_ STARTSUBQUEUE** 通知傳送至回呼函數。


```C++
SPFILENOTIFY_STARTSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) NumOperations;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

已啟動的子佇列。 此參數可以是任何一個值 FILEOP \_ DELETE、FILEOP \_ RENAME 或 FILEOP \_ COPY。

</dd> <dt>

*Param2* 
</dt> <dd>

子佇列中的檔案複製、重新命名或刪除作業的數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果發生錯誤，回呼常式應呼叫 [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror)，並指定錯誤，然後傳回零。 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)函式會傳回 **FALSE** ，而後續對 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)的呼叫將會傳回回呼常式所設定的錯誤碼。

如果未發生任何錯誤，回呼常式應該會傳回非零值。

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

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

