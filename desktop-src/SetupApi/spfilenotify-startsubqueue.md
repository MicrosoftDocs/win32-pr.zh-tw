---
description: '\_當佇列開始處理刪除、重新命名或複製子佇列中的作業時，會將 SPFILENOTIFY STARTSUBQUEUE 通知傳送至回呼函數。'
ms.assetid: 4f971549-8f79-4995-9796-1177c3a3c416
title: 'SPFILENOTIFY_STARTSUBQUEUE 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e4f20440c12e7fcd1900cd9762a504a26b907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985356"
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

 

