---
description: 當檔案作業因為檔案正在 \_ 使用中而延遲時，SetupInstallFileEx 或 SetupCommitFileQueue 會將 SPFILENOTIFY FILEOPDELAYED 通知傳送至回呼常式。 下次重新開機系統時，就會處理此作業。
ms.assetid: a0b38e2b-2390-49e5-b288-77c31636e696
title: 'SPFILENOTIFY_FILEOPDELAYED 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38975506ff998ec09c4549ec95d9ddb620466cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848828"
---
# <a name="spfilenotify_fileopdelayed-message"></a>SPFILENOTIFY \_ FILEOPDELAYED 訊息

當檔案作業因為檔案正在使用中而延遲時， [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)或 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)會將 **SPFILENOTIFY \_ FILEOPDELAYED** 通知傳送至回呼常式。 下次重新開機系統時，就會處理此作業。


```C++
SPFILENOTIFY_FILEOPDELAYED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標。

如果延遲的作業是檔案複製作業， [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) 結構會包含下列資訊。



| FILEPATHS 成員 | 值                                |
|------------------|--------------------------------------|
| **Win32Error**   | 沒有 \_ 錯誤                            |
| **旗標**        | FILEOP \_ 複製                         |
| **來源**       | 暫存檔案的完整路徑。     |
| **Target**       | 實際目標檔案的完整路徑。 |



 

當系統重新開機時，此暫存檔案將會複製到目標目錄。 安裝函式會自動產生暫存檔案的路徑。

如果延遲的作業是檔案刪除作業， [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) 結構會包含下列資訊。



| FILEPATHS 成員 | 值                                |
|------------------|--------------------------------------|
| **Win32Error**   | 沒有 \_ 錯誤                            |
| **旗標**        | FILEOP \_ 刪除                       |
| **來源**       | NULL                                 |
| **Target**       | 要刪除之檔案的完整路徑。 |



 

</dd> <dt>

*Param2* 
</dt> <dd>

未使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

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

[**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




