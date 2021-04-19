---
description: '\_如果要複製之檔案的語言不符合現有目標檔案的語言，則會將 SPFILENOTIFY LANGMISMATCH 通知傳送至回呼常式。'
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: 'SPFILENOTIFY_LANGMISMATCH 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3d7828c90dd4dabb8e1cb73a8dcca7ae33ebd3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979384"
---
# <a name="spfilenotify_langmismatch-message"></a>SPFILENOTIFY \_ LANGMISMATCH 訊息

如果要複製之檔案的語言不符合現有目標檔案的語言，則會將 **SPFILENOTIFY \_ LANGMISMATCH** 通知傳送至回呼常式。 您可以使用 OR 運算子，搭配 [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md) 和/或 [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)，將它單獨傳送給回呼常式或結合。


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標，其中包含來源和目標檔案路徑的相關資訊。

</dd> <dt>

*Param2* 
</dt> <dd>

識別不相符的語言。 此成員具有低字組中原始程式檔的語言識別項，以及最高單字中現有目標檔案的語言識別項。

</dd> </dl>

## <a name="return-value"></a>傳回值

回呼常式應該會傳回下列其中一個值。



| 傳回碼                                                                          | Description                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**真**</dt> </dl>  | 複製檔案並覆寫現有的檔案。<br/>               |
| <dl> <dt>**假**</dt> </dl> | 略過複製操作。 請勿覆寫現有的檔案。<br/> |



 

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

 

 




