---
description: SPFILENOTIFY \_ NEEDNEWCABINET 通知是由 SetupIterateCabinet 傳送，以指出目前的檔案繼續在另一個封包中。
ms.assetid: 01207429-11fb-4e2c-89ba-54321992e953
title: 'SPFILENOTIFY_NEEDNEWCABINET 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3187d48b89579c329a4d0163e151824288462344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194919"
---
# <a name="spfilenotify_neednewcabinet-message"></a>SPFILENOTIFY \_ NEEDNEWCABINET 訊息

**SPFILENOTIFY \_ NEEDNEWCABINET** 通知是由 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)傳送，以指出目前的檔案繼續在另一個封包中。 您的回呼常式接著可以呼叫 [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)，或建立自己的對話方塊來提示使用者插入下一個磁片。


```C++
SPFILENOTIFY_NEEDNEWCABINET
  Param1 = (UINT) CabinetInfo;
  Param2 = (UINT) NewPath;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

封 [**包 \_ 資訊**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) 結構的指標，其中包含要解壓縮的封包和檔案的相關資訊。

</dd> <dt>

*Param2* 
</dt> <dd>

如果回呼不會傳回任何 \_ 錯誤，這個參數就是以 null 結束的字串指標。 如果字串不是空的，它會指定封包的新路徑。

</dd> </dl>

## <a name="return-value"></a>傳回值

您的常式應該會傳回下列其中一個值。



| 傳回碼                                                                                 | Description                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**沒有 \_ 錯誤**</dt> </dl>    | 未發生任何錯誤，請繼續處理封包。<br/>                                                                                                                                                                        |
| <dl> <dt>**錯誤 \_* XXX * * *</dt> </dl> | 發生指定的類型時發生錯誤。 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)函式會傳回 **FALSE**，而指定的錯誤碼會由對 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)的呼叫傳回。<br/> |



 

> [!Note]  
> 沒有預設的封包回呼常式;因此，您必須提供回呼常式來處理 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)所傳送的通知。

 

## <a name="remarks"></a>備註

如果回呼常式未傳回任何 \_ 錯誤， [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) 會檢查 *Param2* 所指向的緩衝區。 如果緩衝區不是空的，則它會包含新的來源路徑。 如果緩衝區是空的，則會假設來源路徑不會變更。

如果需要插入新媒體，您的回呼函式應該確保封包在傳回之前可以存取，呼叫 [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) 函式。

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

[**封包 \_ 資訊**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a)
</dt> <dt>

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

