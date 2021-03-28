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
# <a name="managing-printers"></a><span data-ttu-id="26c19-104">管理印表機</span><span class="sxs-lookup"><span data-stu-id="26c19-104">Managing Printers</span></span>

<span data-ttu-id="26c19-105">Shell API 提供可用來管理網路印表機的功能。</span><span class="sxs-lookup"><span data-stu-id="26c19-105">The Shell API provides functions that you can use to manage networked printers.</span></span> <span data-ttu-id="26c19-106">如果檔案具有與其相關聯的 **列印** 動詞，您可以使用 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 命令來列印。</span><span class="sxs-lookup"><span data-stu-id="26c19-106">If a file has the **print** verb associated with it, you can use the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) command to print it.</span></span>

-   [<span data-ttu-id="26c19-107">印表機管理</span><span class="sxs-lookup"><span data-stu-id="26c19-107">Printer Management</span></span>](#printer-management)
-   [<span data-ttu-id="26c19-108">使用 ShellExecuteEx 列印檔案</span><span class="sxs-lookup"><span data-stu-id="26c19-108">Printing Files with ShellExecuteEx</span></span>](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a><span data-ttu-id="26c19-109">印表機管理</span><span class="sxs-lookup"><span data-stu-id="26c19-109">Printer Management</span></span>

<span data-ttu-id="26c19-110">您可以使用 [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) 功能管理系統上的印表機。</span><span class="sxs-lookup"><span data-stu-id="26c19-110">You can manage printers on a system with the [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) function.</span></span> <span data-ttu-id="26c19-111">此函數可讓您：</span><span class="sxs-lookup"><span data-stu-id="26c19-111">This function allows you to:</span></span>

-   <span data-ttu-id="26c19-112">安裝印表機。</span><span class="sxs-lookup"><span data-stu-id="26c19-112">Install printers.</span></span>
-   <span data-ttu-id="26c19-113">開啟 [印表機]。</span><span class="sxs-lookup"><span data-stu-id="26c19-113">Open printers.</span></span>
-   <span data-ttu-id="26c19-114">取得印表機屬性。</span><span class="sxs-lookup"><span data-stu-id="26c19-114">Get printer properties.</span></span>
-   <span data-ttu-id="26c19-115">建立印表機連結。</span><span class="sxs-lookup"><span data-stu-id="26c19-115">Create printer links.</span></span>
-   <span data-ttu-id="26c19-116">列印測試頁。</span><span class="sxs-lookup"><span data-stu-id="26c19-116">Print a test page.</span></span>

## <a name="printing-files-with-shellexecuteex"></a><span data-ttu-id="26c19-117">使用 ShellExecuteEx 列印檔案</span><span class="sxs-lookup"><span data-stu-id="26c19-117">Printing Files with ShellExecuteEx</span></span>

<span data-ttu-id="26c19-118">如果檔案類型具有與其相關聯的列印命令，您可以使用 **print** 作為動詞來呼叫 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)來列印檔案。</span><span class="sxs-lookup"><span data-stu-id="26c19-118">If a file type has a print command associated with it, you can print the file by calling [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) with **print** as the verb.</span></span> <span data-ttu-id="26c19-119">這個命令通常與用於 **open** 動詞的命令相同，加上旗標來指示應用程式列印檔案。</span><span class="sxs-lookup"><span data-stu-id="26c19-119">This command is often the same as that used for the **open** verb, with the addition of a flag to tell the application to print the file.</span></span> <span data-ttu-id="26c19-120">比方說，Microsoft WordPad 可以列印 .txt 檔。</span><span class="sxs-lookup"><span data-stu-id="26c19-120">For instance, .txt files can be printed by Microsoft WordPad.</span></span> <span data-ttu-id="26c19-121">.Txt 檔案的 **open** 動詞將對應至類似下列的命令：</span><span class="sxs-lookup"><span data-stu-id="26c19-121">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



<span data-ttu-id="26c19-122">當您使用 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 來列印 .txt 檔案時，WordPad 會開啟檔案、列印檔案，然後關閉，將控制權傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="26c19-122">When you use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to print a .txt file, WordPad opens the file, prints it, and then closes, returning control to the application.</span></span> <span data-ttu-id="26c19-123">下列範例函式會採用完整路徑，並使用 **ShellExecuteEx** 來列印它，並使用與其副檔名相關聯的列印命令。</span><span class="sxs-lookup"><span data-stu-id="26c19-123">The following sample function takes a fully qualified path, and uses **ShellExecuteEx** to print it, using the print command associated with its file name extension.</span></span>


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



 

 



