---
description: '\_當佇列承諾程式啟動時，會將 SPFILENOTIFY STARTQUEUE 通知傳送至回呼常式。'
ms.assetid: 682c2ce0-0c82-402c-a487-db5f2c377f3f
title: 'SPFILENOTIFY_STARTQUEUE 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40d4fedde850d975edd697423339c686fe697911b9bef2fdc252baffda0158f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073208"
---
# <a name="spfilenotify_startqueue-message"></a>SPFILENOTIFY \_ STARTQUEUE 訊息

當佇列承諾程式啟動時，會將 **SPFILENOTIFY \_ STARTQUEUE** 通知傳送至回呼常式。


```C++
SPFILENOTIFY_STARTQUEUE
  Param1 = (UINT) OwnerWindow;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

要擁有回呼常式產生之對話方塊的視窗控制碼。

</dd> <dt>

*Param2* 
</dt> <dd>

未使用的。

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

 

