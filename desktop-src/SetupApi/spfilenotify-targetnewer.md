---
description: '\_如果要複製的檔案已排入較新的 sp \_ 複製 \_ ，或是 sp \_ copy \_ 強制 \_ 指定較新的旗標，且目標目錄中已有較新版本的檔案，則會將 SPFILENOTIFY TARGETNEWER 通知傳送至回呼常式。'
ms.assetid: 93bcd610-f75d-4900-841c-f67946af5c4a
title: 'SPFILENOTIFY_TARGETNEWER 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c432515a5ce0e9a1eddb8ea6e92f7376c318b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993199"
---
# <a name="spfilenotify_targetnewer-message"></a>SPFILENOTIFY \_ TARGETNEWER 訊息

如果 **要 \_** 複製的檔案已排入較新的 sp \_ 複製 \_ ，或是 sp \_ copy \_ 強制 \_ 指定較新的旗標，且目標目錄中已有較新版本的檔案，則會將 SPFILENOTIFY TARGETNEWER 通知傳送至回呼常式。 它可以單獨傳送給回呼常式，或與 [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) 和/或 [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md)一起 or 運算。


```C++
SPFILENOTIFY_TARGETNEWER
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標，其中包含來源和目標檔案之路徑的相關資訊。

</dd> <dt>

*Param2* 
</dt> <dd>

除非使用 OR 運算子搭配 [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md)來合併此通知，否則不會使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

回呼常式應該會傳回下列其中一個值。



| 傳回碼                                                                          | Description                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**真**</dt> </dl>  | 覆寫目標目錄中的檔案。<br/> |
| <dl> <dt>**假**</dt> </dl> | 略過目前的複製操作。<br/>            |



 

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
</dt> <dt>

[**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




