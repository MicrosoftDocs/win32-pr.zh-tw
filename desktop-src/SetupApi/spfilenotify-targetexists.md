---
description: '\_如果要複製的檔案是以 SP 複製 NOOVERWRITE 旗標排入佇列 \_ \_ ，而該檔案已存在於目標目錄中，則會將 SPFILENOTIFY TARGETEXISTS 通知傳送至回呼常式。'
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: 'SPFILENOTIFY_TARGETEXISTS 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d0c1a1ffba520789113b0dc78246657a4fe324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386252"
---
# <a name="spfilenotify_targetexists-message"></a>SPFILENOTIFY \_ TARGETEXISTS 訊息

如果要複製的檔案是以 SP 複製 NOOVERWRITE 旗標排入佇列，而該檔案已存在於目標目錄中，則會將 **SPFILENOTIFY \_ TARGETEXISTS** 通知傳送至回呼常式 \_ \_ 。 您可以使用 OR 運算子，搭配 [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) 和/或 [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md) 通知，將它單獨傳送給回呼常式或合併使用。


```C++
SPFILENOTIFY_TARGETEXISTS
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

除非使用 OR 運算子結合了 [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) 通知，否則不會使用此參數。

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

 

 




