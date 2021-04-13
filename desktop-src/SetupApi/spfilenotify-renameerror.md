---
description: 如果在檔案 \_ 重新命名作業期間發生錯誤，則會將 SPFILENOTIFY RENAMEERROR 通知傳送至回呼常式。
ms.assetid: b7016cbe-2987-477f-958b-52b7a31c54c2
title: 'SPFILENOTIFY_RENAMEERROR 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a45658153980d7cfd5cb99b76fb344fcdb4bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319875"
---
# <a name="spfilenotify_renameerror-message"></a>SPFILENOTIFY \_ RENAMEERROR 訊息

如果在檔案重新命名作業期間發生錯誤，則會將 **SPFILENOTIFY \_ RENAMEERROR** 通知傳送至回呼常式。


```C++
SPFILENOTIFY_RENAMEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標。 **FILEPATHS** 結構的 **Win32Error** 成員會指定在重新命名作業期間發生的錯誤。

</dd> <dt>

*Param2* 
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="return-value"></a>傳回值

回呼常式應該會傳回下列其中一項。



| 傳回碼                                                                                  | Description                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ 重試**</dt> </dl> | 使用者選擇再次嘗試重新命名操作。<br/>                                                                                                                                                                                                  |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>  | 使用者選擇略過檔案重新命名作業。<br/>                                                                                                                                                                                                      |
| <dl> <dt>**FILEOP \_ 中止**</dt> </dl> | 停止佇列認可。 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 會傳回 **FALSE**。 [](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) \_ 如果使用者取消) 或錯誤 \_ 記憶體不足，GetLastError 會傳回擴充的錯誤資訊，例如錯誤取消 (\_ \_ 。<br/> |



 

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

 

