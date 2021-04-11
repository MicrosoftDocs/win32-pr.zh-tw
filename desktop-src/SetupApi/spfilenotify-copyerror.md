---
description: 如果檔案 \_ 複製作業期間發生錯誤，則會將 SPFILENOTIFY COPYERROR 通知傳送至回呼常式。
ms.assetid: d6096954-c6a5-44d4-a358-c1320c50730a
title: 'SPFILENOTIFY_COPYERROR 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cd44daabd6a4aed5e61a716bab3df44f35fc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849599"
---
# <a name="spfilenotify_copyerror-message"></a>SPFILENOTIFY \_ COPYERROR 訊息

如果檔案複製作業期間發生錯誤，則會將 **SPFILENOTIFY \_ COPYERROR** 通知傳送至回呼常式。


```C++
SPFILENOTIFY_COPYERROR
  Param1 = (UINT_PTR) FilePathInfo;
  Param2 = (UINT_PTR) ReturnBuffer;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標。

</dd> <dt>

*Param2* 
</dt> <dd>

緩衝區大小上限路徑字元的指標，可 \_ 儲存使用者指定的新路徑資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

回呼應該會傳回下列其中一個值。



| 傳回碼                                                                                    | Description                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ 中止**</dt> </dl>   | 應取消佇列處理。 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 會傳回零，而 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 會傳回擴充的錯誤資訊，例如 \_ ，如果使用者取消) 或錯誤 \_ 記憶體不足，則會傳回錯誤 (\_ \_ 。<br/> |
| <dl> <dt>**FILEOP \_ NEWPATH**</dt> </dl> | 使用回呼函式放在 *Param2* 參數所指向之緩衝區中的路徑，以重試複製作業。 回呼常式應確定路徑不會溢位最大路徑元素之 TCHAR 陣列的緩衝區大小 \_ 。<br/>                |
| <dl> <dt>**FILEOP \_ 重試**</dt> </dl>   | 使用者正在嘗試複製操作。<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>    | 使用者即將略過檔案複製作業。<br/>                                                                                                                                                                                                                      |



 

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

 

