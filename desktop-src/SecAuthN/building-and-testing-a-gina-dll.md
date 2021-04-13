---
description: 所有的函式、原型、結構和常數都定義于 Winwlx .h 標頭檔中。
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: 建立和測試 GINA DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e6e4a00f15e6ced4827bbc3efeb3c459f5d6a8
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321795"
---
# <a name="building-and-testing-a-gina-dll"></a><span data-ttu-id="d0df2-103">建立和測試 GINA DLL</span><span class="sxs-lookup"><span data-stu-id="d0df2-103">Building and Testing a GINA DLL</span></span>

<span data-ttu-id="d0df2-104">所有的函式、原型、結構和常數都定義于 Winwlx .h 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="d0df2-104">All functions, prototypes, structures, and constants are defined in the Winwlx.h header file.</span></span>

> [!Note]  
> <span data-ttu-id="d0df2-105">在 Windows Vista 中會忽略 GINA Dll。</span><span class="sxs-lookup"><span data-stu-id="d0df2-105">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="d0df2-106">若要測試 [*GINA*](/windows/desktop/SecGloss/g-gly) DLL，請從已檢查的作業系統版本（可透過 Microsoft Windows 驅動程式開發工具組 (DDK) 取得）使用 Winlogon.exe。</span><span class="sxs-lookup"><span data-stu-id="d0df2-106">To test a [*GINA*](/windows/desktop/SecGloss/g-gly) DLL, use the Winlogon.exe from a checked version of the operating system, which is available with the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="d0df2-107">已檢查的 [*Winlogon*](/windows/desktop/SecGloss/w-gly) 版本支援偵錯工具 gina，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d0df2-107">The checked version of [*Winlogon*](/windows/desktop/SecGloss/w-gly) supports debugging GINAs as follows:</span></span>

-   <span data-ttu-id="d0df2-108">您可以使用下列語法，在 Win.ini 中建立區段，以指定 Winlogon 調試選項。</span><span class="sxs-lookup"><span data-stu-id="d0df2-108">You can use the following syntax to create a section in Win.ini to specify Winlogon debugging options.</span></span>

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    <span data-ttu-id="d0df2-109">如果 **指定，則** 記錄檔應該包含將用來記錄偵錯工具資訊之檔案的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="d0df2-109">If specified, **LogFile** should contain the fully qualified name of the file that will be used to log debugging information.</span></span> <span data-ttu-id="d0df2-110">若檔案不存在，會建立該檔案。</span><span class="sxs-lookup"><span data-stu-id="d0df2-110">If the file does not exist, it will be created.</span></span>

    <span data-ttu-id="d0df2-111">**DebugFlags** 選項會指定要寫入記錄檔或偵錯工具的哪些類型的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="d0df2-111">The **DebugFlags** options specify which kinds of debugging information to write to the log file, or debugger.</span></span> <span data-ttu-id="d0df2-112">**DebugFlags** 可包含下列一或多個旗標。</span><span class="sxs-lookup"><span data-stu-id="d0df2-112">**DebugFlags** can contain one or more of the following flags.</span></span>

    

    | <span data-ttu-id="d0df2-113">調試旗標</span><span class="sxs-lookup"><span data-stu-id="d0df2-113">Debugging flag</span></span> | <span data-ttu-id="d0df2-114">Description</span><span class="sxs-lookup"><span data-stu-id="d0df2-114">Description</span></span>                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d0df2-115">CoolSwitch</span><span class="sxs-lookup"><span data-stu-id="d0df2-115">CoolSwitch</span></span>     | <span data-ttu-id="d0df2-116">CTRL + ALT + SHIFT + TAB 鍵組合會導致 Winlogon 中的 debug break。</span><span class="sxs-lookup"><span data-stu-id="d0df2-116">The CTRL+ALT+SHIFT+TAB key combination will cause a debug break in Winlogon.</span></span>                                                                                               |
    | <span data-ttu-id="d0df2-117">錯誤</span><span class="sxs-lookup"><span data-stu-id="d0df2-117">Error</span></span>          | <span data-ttu-id="d0df2-118">列印錯誤。</span><span class="sxs-lookup"><span data-stu-id="d0df2-118">Print errors.</span></span>                                                                                                                                                              |
    | <span data-ttu-id="d0df2-119">Init</span><span class="sxs-lookup"><span data-stu-id="d0df2-119">Init</span></span>           | <span data-ttu-id="d0df2-120">列印初始化和進度訊息。</span><span class="sxs-lookup"><span data-stu-id="d0df2-120">Print initialization and progress messages.</span></span>                                                                                                                                |
    | <span data-ttu-id="d0df2-121">Notify</span><span class="sxs-lookup"><span data-stu-id="d0df2-121">Notify</span></span>         | <span data-ttu-id="d0df2-122">列印通知套件訊息。</span><span class="sxs-lookup"><span data-stu-id="d0df2-122">Print notification package messages.</span></span>                                                                                                                                       |
    | <span data-ttu-id="d0df2-123">SAS</span><span class="sxs-lookup"><span data-stu-id="d0df2-123">SAS</span></span>            | <span data-ttu-id="d0df2-124"> (SAS) 通知，列印 [*安全注意順序*](/windows/desktop/SecGloss/s-gly) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d0df2-124">Print information about [*secure attention sequence*](/windows/desktop/SecGloss/s-gly) (SAS) notifications.</span></span> |
    | <span data-ttu-id="d0df2-125">狀態</span><span class="sxs-lookup"><span data-stu-id="d0df2-125">State</span></span>          | <span data-ttu-id="d0df2-126">當 Winlogon 變更狀態時列印訊息。</span><span class="sxs-lookup"><span data-stu-id="d0df2-126">Print messages when Winlogon changes state.</span></span>                                                                                                                                |
    | <span data-ttu-id="d0df2-127">逾時</span><span class="sxs-lookup"><span data-stu-id="d0df2-127">Timeout</span></span>        | <span data-ttu-id="d0df2-128">在設定時間限制或達到時間限制時列印訊息。</span><span class="sxs-lookup"><span data-stu-id="d0df2-128">Print messages when a time limit is set or a time limit is reached.</span></span>                                                                                                        |
    | <span data-ttu-id="d0df2-129">追蹤</span><span class="sxs-lookup"><span data-stu-id="d0df2-129">Trace</span></span>          | <span data-ttu-id="d0df2-130">列印詳細資訊追蹤資訊。</span><span class="sxs-lookup"><span data-stu-id="d0df2-130">Print verbose trace information.</span></span>                                                                                                                                           |
    | <span data-ttu-id="d0df2-131">警告</span><span class="sxs-lookup"><span data-stu-id="d0df2-131">Warn</span></span>           | <span data-ttu-id="d0df2-132">列印警告。</span><span class="sxs-lookup"><span data-stu-id="d0df2-132">Print warnings.</span></span>                                                                                                                                                            |

    

     

-   <span data-ttu-id="d0df2-133">若要在偵錯工具中啟動已檢查的 Winlogon 版本，請在登錄中新增下列專案：</span><span class="sxs-lookup"><span data-stu-id="d0df2-133">To start the checked version of Winlogon in a debugger, add the following entry to the registry:</span></span>

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
> <span data-ttu-id="d0df2-134">您必須使用 Windows 符號偵錯工具 (NTSD) 來偵測 Winlogon。</span><span class="sxs-lookup"><span data-stu-id="d0df2-134">You must use the Windows symbolic debugger (NTSD) to debug Winlogon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0df2-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0df2-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0df2-136">載入和執行 GINA DLL</span><span class="sxs-lookup"><span data-stu-id="d0df2-136">Loading and Running a GINA DLL</span></span>](loading-and-running-a-gina-dll.md)
</dt> <dt>

[<span data-ttu-id="d0df2-137">GINA 匯出函數</span><span class="sxs-lookup"><span data-stu-id="d0df2-137">GINA Export Functions</span></span>](authentication-functions.md)
</dt> <dt>

[<span data-ttu-id="d0df2-138">GINA 結構</span><span class="sxs-lookup"><span data-stu-id="d0df2-138">GINA Structures</span></span>](authentication-structures.md)
</dt> <dt>

[<span data-ttu-id="d0df2-139">終端機服務 GINA 函式</span><span class="sxs-lookup"><span data-stu-id="d0df2-139">Terminal Services GINA Functions</span></span>](terminal-services-gina-functions.md)
</dt> </dl>

 

 
