---
description: Shell API 提供可用來管理網路印表機的功能。 如果檔案具有與其相關聯的列印動詞，您可以使用 ShellExecuteEx 命令來列印。
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: 管理印表機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e9625fbe17c0dd350a10c0c71dcd5332fb9154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973349"
---
# <a name="managing-printers"></a>管理印表機

Shell API 提供可用來管理網路印表機的功能。 如果檔案具有與其相關聯的 **列印** 動詞，您可以使用 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 命令來列印。

-   [印表機管理](#printer-management)
-   [使用 ShellExecuteEx 列印檔案](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a>印表機管理

您可以使用 [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) 功能管理系統上的印表機。 此函數可讓您：

-   安裝印表機。
-   開啟 [印表機]。
-   取得印表機屬性。
-   建立印表機連結。
-   列印測試頁。

## <a name="printing-files-with-shellexecuteex"></a>使用 ShellExecuteEx 列印檔案

如果檔案類型具有與其相關聯的列印命令，您可以使用 **print** 作為動詞來呼叫 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)來列印檔案。 這個命令通常與用於 **open** 動詞的命令相同，加上旗標來指示應用程式列印檔案。 比方說，Microsoft WordPad 可以列印 .txt 檔。 .Txt 檔案的 **open** 動詞將對應至類似下列的命令：


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



當您使用 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 來列印 .txt 檔案時，WordPad 會開啟檔案、列印檔案，然後關閉，將控制權傳回給應用程式。 下列範例函式會採用完整路徑，並使用 **ShellExecuteEx** 來列印它，並使用與其副檔名相關聯的列印命令。


```C++
#include <shlobj.h>

HINSTANCE PrintFile(LPCTSTR pszFileName)
{
    SHELLEXECUTEINFO ShExecInfo;
    HINSTANCE hInst;

    // Fill the SHELLEXECUTEINFO array.

    ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
    ShExecInfo.fMask = NULL;
    ShExecInfo.hwnd = NULL;
    ShExecInfo.lpVerb = "print";
    ShExecInfo.lpFile = pszFileName;  // a fully qualified path
    ShExecInfo.lpParameters = NULL;
    ShExecInfo.lpDirectory = NULL;    
    ShExecInfo.nShow = SW_MAXIMIZE;
    ShExecInfo.hInstApp = NULL;

    hInst = ShellExecuteEx(&ShExecInfo);
    
    return hInst;
}
```



 

 



