---
description: '\_當佇列啟動檔案刪除作業時，會將 SPFILENOTIFY STARTDELETE 通知傳送至回呼函數。'
ms.assetid: 244714ad-dde7-4b5a-b3f3-78aa4cc901f5
title: 'SPFILENOTIFY_STARTDELETE 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e17edd2bdbf58be72d4c7b8d6841663787c4fb0074e5eefe322c51dab0f9a3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964294"
---
# <a name="spfilenotify_startdelete-message"></a>SPFILENOTIFY \_ STARTDELETE 訊息

當佇列啟動檔案刪除作業時，會將 **SPFILENOTIFY \_ STARTDELETE** 通知傳送至回呼函數。


```C++
SPFILENOTIFY_STARTDELETE
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

一律將值 FILEOP \_ 刪除。

</dd> </dl>

## <a name="return-value"></a>傳回值

回呼常式應該會傳回下列其中一個值。



| 傳回碼                                                                                  | 描述                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ 中止**</dt> </dl> | 中止佇列認可。 回呼常式應呼叫 [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) 來指示中止的原因。 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 會傳回 **FALSE** ，而後續的 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 呼叫會傳回回呼常式在呼叫 **SetLastError** 期間所設定的錯誤碼。<br/> |
| <dl> <dt>**FILEOP \_ DOIT R**</dt> </dl>  | 執行檔案複製作業。<br/>                                                                                                                                                                                                                                                                                                                                  |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>  | 略過目前的複製操作。<br/>                                                                                                                                                                                                                                                                                                                                  |



 

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

 

