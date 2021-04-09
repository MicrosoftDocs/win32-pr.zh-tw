---
description: 將 MOF 檔案新增至儲存機制復原期間所編譯的檔案清單。
ms.assetid: 8901c04e-f8c1-45b0-b69d-e2ebc948f088
ms.tgt_platform: multiple
title: pragma 自動回復
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9bb1cfca44e0bc5437d05d721ffcd57203e5aa9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944932"
---
# <a name="pragma-autorecover"></a>pragma 自動回復

**Pragma 自動** 復原預處理器命令會將 MOF 檔案新增至在存放庫復原期間所編譯的檔案清單。 **自動** 回復 MOF 檔案的清單會儲存在此登錄機碼中：

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **自動回復 mof**

當作業系統啟動 WMI 時，WMI 會檢查 WMI 儲存機制的完整性。 如果存放庫損毀，WMI 就會自動重建存放庫，並在登錄中重新編譯此機碼中列出的任何 MOF 檔案。

以下說明 pragma 自動回復命令的語法：


```mof
#pragma autorecover
```



不過，使用此命令時，您必須遵守下列限制：

-   WMI 無法復原位於遠端電腦上的 MOF 檔案。

    因此，此登錄機碼中列出的 MOF 檔案必須位於本機電腦上。

-   當 WMI 復原 MOF 檔案時，您無法指定 MOF 編譯器所使用的命令列參數。

    因此，您應該將 [pragma](-pragma.md) 命令納入不需要命令列切換的 MOF 檔案中。 下列範例說明從這個登錄機碼復原 MOF 檔案時，WMI 未使用的一般命令列參數： **mofcomp.exe-N:Root \\ Test mymof. mof**

    不過，您可以使用 MOF 檔案中的 [pragma](-pragma.md) 命令來指定命名空間。

    ```mof
    #pragma namespace ("\\\\.\\Root\\test")
    ```

    

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[預處理器命令](preprocessor-commands.md)
</dt> </dl>

 

 




