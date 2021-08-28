---
description: 針對檔案 \_ \_ 佇列的複製子佇列中的每個節點，SetupScanFileQueue 會將 SPFILENOTIFY QUEUESCAN EX 通知傳送至回呼常式。
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: 'SPFILENOTIFY_QUEUESCAN_EX 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d151a5172918e7a7dcb13e8c480aae82da0a3ec1ffb38d26db29d63143cbc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992588"
---
# <a name="spfilenotify_queuescan_ex-message"></a>SPFILENOTIFY \_ QUEUESCAN \_ EX 訊息

針對檔案佇列的複製子佇列中的每個節點， [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)會將 **SPFILENOTIFY \_ QUEUESCAN \_ EX** 通知傳送至回呼常式。 只有在呼叫 **SetupScanFileQueue** 函式來指定旗標 SPQ \_ SCAN \_ USE CALLBACKEX 時，才會發生這種情況 \_ 。


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標。 **目標** 成員是系統上目標檔案的檔案名。 **來源** 成員是原始程式檔的預期路徑。 **Win32Error** 成員是簽署錯誤。

</dd> </dl>

## <a name="return-value"></a>傳回值

回呼常式應該會傳回 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

如果回呼常式未傳回 \_ 錯誤，則會繼續執行佇列掃描。 如果常式傳回任何其他錯誤碼，則佇列掃描會中止，且 [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) 會傳回 FALSE。

> [!Note]  
> [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)函數不會處理這項通知。

 

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

[**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

