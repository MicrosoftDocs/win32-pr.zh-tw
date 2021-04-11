---
description: SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO 通知會針對檔案佇列的複製子佇列中的每個節點 SetupScanFileQueue，傳送至回呼常式。
ms.assetid: 5b22e8ba-9a18-461b-bad7-b2d76f83d7f3
title: 'SPFILENOTIFY_QUEUESCAN_SIGNERINFO 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29bf9e9c7e0ab76303d8c2fb21a0109ec60358f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944608"
---
# <a name="spfilenotify_queuescan_signerinfo-message"></a>SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO 訊息

**SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO** 通知會針對檔案佇列的複製子佇列中的每個節點 [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) ，傳送至回呼常式。 只有在呼叫 **SetupScanFileQueue** 函式來指定旗標 SPQ \_ SCAN \_ 使用 \_ 回呼 SIGNERINFO 時，才會發生這種情況 \_ 。 從 Windows XP 開始提供。


```C++
SPFILENOTIFY_QUEUESCAN_SIGNERINFO
  Param1 = (PFILEPATHS_SIGNERINFO) Filepaths;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

[**FILEPATHS \_ SIGNERINFO**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a)結構的指標。 **目標** 成員是系統上目標檔案的檔案名。 **來源** 成員是原始程式檔的預期路徑。 **Win32Error** 成員是簽署錯誤。 如果回呼常式傳回 **Win32Error**= = NO ERROR，則會傳回簽章資訊 \_ 。 **DigitalSigner** 成員是數位簽章人。 **版本** 成員為版本。 **CatalogFile** 是類別目錄檔案。

</dd> </dl>

## <a name="return-value"></a>傳回值

回呼常式應該會傳回 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

如果回呼常式未傳回 \_ 錯誤，則會繼續執行佇列掃描，如果常式傳回任何其他錯誤碼，則會傳回佇列掃描中止，且 [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) 會傳回 **FALSE**。

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

 

