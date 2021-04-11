---
description: 如果檔案 \_ 刪除作業期間發生錯誤，則會將 SPFILENOTIFY DELETEERROR 通知傳送至回呼常式。
ms.assetid: b98b62f0-0b59-430e-966d-c1447026b696
title: 'SPFILENOTIFY_DELETEERROR 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035b61120bd1343b43c9b6f6d74246eab33cb430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027488"
---
# <a name="spfilenotify_deleteerror-message"></a>SPFILENOTIFY \_ DELETEERROR 訊息

如果檔案刪除作業期間發生錯誤，則會將 **SPFILENOTIFY \_ DELETEERROR** 通知傳送至回呼常式。


```C++
SPFILENOTIFY_DELETEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標。

</dd> <dt>

*Param2* 
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="return-value"></a>傳回值

回呼常式應該會傳回下列其中一個值。



| 傳回碼                                                                                  | Description                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ 中止**</dt> </dl> | 應取消佇列處理。 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 會傳回零，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回擴充的錯誤資訊，例如 \_ ，如果使用者取消) 或錯誤 \_ 記憶體不足，則會傳回錯誤 (\_ \_ 。<br/> |
| <dl> <dt>**FILEOP \_ 重試**</dt> </dl> | 使用者正在嘗試刪除操作。<br/>                                                                                                                                                                                                                 |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>  | 使用者即將略過檔案刪除操作。<br/>                                                                                                                                                                                                                    |



 

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

 

