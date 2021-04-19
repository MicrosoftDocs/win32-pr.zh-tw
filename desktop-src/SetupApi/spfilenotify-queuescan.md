---
description: 針對檔案 \_ 佇列的複製子佇列中的每個節點 SetupScanFileQueue，會將 SPFILENOTIFY QUEUESCAN 通知傳送至回呼常式。 只有在呼叫 SetupScanFileQueue 函式來指定旗標 SPQ \_ SCAN 使用回呼時，才會發生這種情況 \_ \_ 。
ms.assetid: 8aacc6c0-b6fe-4b4a-bbe4-a0351baf1f30
title: 'SPFILENOTIFY_QUEUESCAN 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66202a398f7e3f4e1121782f9469d2d6f299452c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988351"
---
# <a name="spfilenotify_queuescan-message"></a>SPFILENOTIFY \_ QUEUESCAN 訊息

針對檔案佇列的複製子佇列中的每個節點 [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) ，會將 **SPFILENOTIFY \_ QUEUESCAN** 通知傳送至回呼常式。 只有在呼叫 **SetupScanFileQueue** 函式來指定旗標 SPQ \_ SCAN \_ 使用回呼時，才會發生這種情況 \_ 。


```C++
SPFILENOTIFY_QUEUESCAN
  Param1 = (UINT) TargetPath;
  Param2 = (UINT) DelayFlag;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

以 Null 終止的字串，指定目前節點中佇列之檔案的目標路徑資訊。

</dd> <dt>

*Param2* 
</dt> <dd>

如果佇列目前節點中的檔案正在使用中， *Param2* 會將值 SPQ \_ 延遲 \_ 複製。 如果檔案不在使用中，此值為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

回呼常式應該會傳回 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

如果回呼常式未傳回 \_ 錯誤，則會繼續執行佇列掃描。 如果常式傳回任何其他錯誤碼，則佇列掃描會中止，且 [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) 會傳回 **FALSE**。

> [!Note]  
> [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)函數不會處理這項通知。

 

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

[**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

