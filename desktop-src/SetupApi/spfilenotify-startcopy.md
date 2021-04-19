---
description: '\_當佇列啟動檔案複製作業時，會將 SPFILENOTIFY STARTCOPY 通知傳送至回呼函數。'
ms.assetid: 01a7d9d4-b548-4e72-b1c9-7116e67c023b
title: 'SPFILENOTIFY_STARTCOPY 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6693938a2f67530e7e3c906c5105d2c98a915a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990371"
---
# <a name="spfilenotify_startcopy-message"></a>SPFILENOTIFY \_ STARTCOPY 訊息

當佇列啟動檔案複製作業時，會將 **SPFILENOTIFY \_ STARTCOPY** 通知傳送至回呼函數。


```C++
SPFILENOTIFY_STARTCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標。

</dd> <dt>

*Param2* 
</dt> <dd>

一律具有值 FILEOP \_ COPY。

</dd> </dl>

## <a name="return-value"></a>傳回值

回呼常式應該會傳回下列其中一個值。



| 傳回碼                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ 中止**</dt> </dl> | 中止佇列認可進程。 回呼常式應呼叫 [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) 來指出終止的原因。 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)函式會傳回 **FALSE** ，而後續的 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)呼叫會傳回回呼常式在呼叫 **SetLastError** 期間所設定的錯誤碼。<br/> |
| <dl> <dt>**FILEOP \_ DOIT R**</dt> </dl>  | 執行檔案複製作業。<br/>                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>  | 略過目前的複製操作。<br/>                                                                                                                                                                                                                                                                                                                                                          |



 

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

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

