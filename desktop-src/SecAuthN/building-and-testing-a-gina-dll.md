---
description: 所有的函式、原型、結構和常數都定義于 Winwlx .h 標頭檔中。
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: 建立和測試 GINA DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31df8597ca9ad78b8c94efb5610e3c899f7834cb14c9112b15a410c72705a0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883528"
---
# <a name="building-and-testing-a-gina-dll"></a>建立和測試 GINA DLL

所有的函式、原型、結構和常數都定義于 Winwlx .h 標頭檔中。

> [!Note]  
> Windows Vista 會忽略 GINA dll。

 

若要測試 [*GINA*](/windows/desktop/SecGloss/g-gly) DLL，請從已檢查版本的作業系統使用 Winlogon.exe，這可透過 Microsoft Windows 驅動程式開發工具組 (DDK) 取得。 已檢查的 [*Winlogon*](/windows/desktop/SecGloss/w-gly) 版本支援偵錯工具 gina，如下所示：

-   您可以使用下列語法，在 Win.ini 中建立區段，以指定 Winlogon 調試選項。

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    如果 **指定，則** 記錄檔應該包含將用來記錄偵錯工具資訊之檔案的完整名稱。 若檔案不存在，會建立該檔案。

    **DebugFlags** 選項會指定要寫入記錄檔或偵錯工具的哪些類型的偵錯工具。 **DebugFlags** 可包含下列一或多個旗標。

    

    | 調試旗標 | 描述                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | CoolSwitch     | CTRL + ALT + SHIFT + TAB 鍵組合會導致 Winlogon 中的 debug break。                                                                                               |
    | 錯誤          | 列印錯誤。                                                                                                                                                              |
    | Init           | 列印初始化和進度訊息。                                                                                                                                |
    | Notify         | 列印通知套件訊息。                                                                                                                                       |
    | SAS            |  (SAS) 通知，列印 [*安全注意順序*](/windows/desktop/SecGloss/s-gly) 的相關資訊。 |
    | 狀態          | 當 Winlogon 變更狀態時列印訊息。                                                                                                                                |
    | 逾時        | 在設定時間限制或達到時間限制時列印訊息。                                                                                                        |
    | 追蹤          | 列印詳細資訊追蹤資訊。                                                                                                                                           |
    | 警告           | 列印警告。                                                                                                                                                            |

    

     

-   若要在偵錯工具中啟動已檢查的 Winlogon 版本，請在登錄中新增下列專案：

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows NT
                CurrentVersion
                   Image File Execution Options
                      winlogon.exe
                         Debugger = ntsd -d<dl>
    <dt>

                     Data type
</dt>
    <dd>                     REG_SZ</dd>
    </dl>
    ```

> [!NOTE]
> 您必須使用 Windows 符號偵錯工具 (NTSD) 來偵測 Winlogon。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[載入和執行 GINA DLL](loading-and-running-a-gina-dll.md)
</dt> <dt>

[GINA 匯出函數](authentication-functions.md)
</dt> <dt>

[GINA 結構](authentication-structures.md)
</dt> <dt>

[終端機服務 GINA 函式](terminal-services-gina-functions.md)
</dt> </dl>

 

 
