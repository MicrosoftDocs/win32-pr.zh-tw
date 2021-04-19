---
description: '\_當需要新媒體或新的封包檔時，會將 SPFILENOTIFY NEEDMEDIA 通知傳送至回呼常式。'
ms.assetid: 6a7947de-1bb3-46e0-9334-405684e58e98
title: 'SPFILENOTIFY_NEEDMEDIA 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b856a95f3c2e200d1d81cfa00c05ef592c1759
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106982141"
---
# <a name="spfilenotify_needmedia-message"></a>SPFILENOTIFY \_ NEEDMEDIA 訊息

當需要新媒體或新的封包檔時，會將 **SPFILENOTIFY \_ NEEDMEDIA** 通知傳送至回呼常式。


```C++
SPFILENOTIFY_NEEDMEDIA
  Param1 = (UINT) SourceMediaInfo;
  Param2 = (UINT) NewPathInfo;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

[**來源 \_ 媒體**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)結構的指標。

</dd> <dt>

*Param2* 
</dt> <dd>

字元陣列的指標，用以儲存使用者提供的新路徑資訊。 緩衝區大小是最大路徑元素的 **TCHAR** 陣列 \_ 。 安裝應用程式所傳回的路徑資訊不應超過此大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

回呼常式應該會傳回下列其中一項。



| 傳回碼                                                                                    | Description                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ NEWPATH**</dt> </dl> | 媒體存在，而且要求的檔案可在 *Param2* 所指向的緩衝區中指定的路徑上取得。<br/>                                                                                         |
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl>    | 略過要求的檔案<br/>                                                                                                                                                                                      |
| <dl> <dt>**FILEOP \_ 中止**</dt> </dl>   | 中止佇列處理。 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)函數會傳回 **FALSE**。 GetLastError 會傳回擴充的錯誤資訊，例如， \_ 如果使用者取消，則會取消錯誤。<br/> |
| <dl> <dt>**FILEOP-DOIT R**</dt> </dl>     | 媒體可供使用。<br/>                                                                                                                                                                                      |



 

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
</dt> <dt>

[**來源 \_ 媒體**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)
</dt> </dl>

 

 




