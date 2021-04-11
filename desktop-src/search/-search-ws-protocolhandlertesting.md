---
description: 測試和偵測通訊協定處理常式的整數是瞭解通訊協定處理常式的啟動方式。
ms.assetid: 33c99620-7381-4719-9fc6-4c8284481411
title: 偵錯工具通訊協定處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d59c0c7915f9bbf84a80091408ba88a9a75ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112400"
---
# <a name="debugging-protocol-handlers"></a><span data-ttu-id="00018-103">偵錯工具通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="00018-103">Debugging Protocol Handlers</span></span>

<span data-ttu-id="00018-104">測試和偵測通訊協定處理常式的整數是瞭解通訊協定處理常式的啟動方式。</span><span class="sxs-lookup"><span data-stu-id="00018-104">Integral to testing and debugging your protocol handler implementations is understanding how protocol handlers are launched.</span></span>

<span data-ttu-id="00018-105">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="00018-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="00018-106">關於偵錯工具通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="00018-106">About Debugging Protocol Handlers</span></span>](#about-debugging-protocol-handlers)
-   [<span data-ttu-id="00018-107">設定調試</span><span class="sxs-lookup"><span data-stu-id="00018-107">Setting Up Debugging</span></span>](#setting-up-debugging)
-   [<span data-ttu-id="00018-108">其他資源</span><span class="sxs-lookup"><span data-stu-id="00018-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="00018-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="00018-109">Related topics</span></span>](#related-topics)

## <a name="about-debugging-protocol-handlers"></a><span data-ttu-id="00018-110">關於偵錯工具通訊協定處理常式</span><span class="sxs-lookup"><span data-stu-id="00018-110">About Debugging Protocol Handlers</span></span>

<span data-ttu-id="00018-111">SearchIndexer 進程 (searchindexer.exe) 會在系統內容中啟動一份 SearchProtocolHost 程式 (SearchProtocolHost.exe) ，並在使用者內容中啟動另一個複本。</span><span class="sxs-lookup"><span data-stu-id="00018-111">The SearchIndexer process (searchindexer.exe) launches one copy of the SearchProtocolHost process (SearchProtocolHost.exe) in the system context and another copy in the user context.</span></span> <span data-ttu-id="00018-112">然後，您可以視需要在 SearchProtocolHost 程式中載入通訊協定處理常式。</span><span class="sxs-lookup"><span data-stu-id="00018-112">Then, the protocol handlers are loaded in the SearchProtocolHost process as needed.</span></span> <span data-ttu-id="00018-113">在搜尋服務停止之前，它們不會被卸載。</span><span class="sxs-lookup"><span data-stu-id="00018-113">They are not unloaded until the search service is stopped.</span></span> <span data-ttu-id="00018-114">當服務正在執行時，相同的通訊協定處理常式實例會重複使用任何次數。</span><span class="sxs-lookup"><span data-stu-id="00018-114">The same instance of a protocol handler is reused any number of times while the service is running.</span></span>

<span data-ttu-id="00018-115">SearchIndexer 和 SearchProtocolHost 進程會在編制索引期間經常進行通訊。</span><span class="sxs-lookup"><span data-stu-id="00018-115">The SearchIndexer and SearchProtocolHost processes communicate frequently during indexing.</span></span> <span data-ttu-id="00018-116">如果您暫停或停止 SearchProtocolHost 處理常式，SearchIndexer 將會啟動新的 SearchProtocolHost 進程，使您的偵錯工具失效。</span><span class="sxs-lookup"><span data-stu-id="00018-116">If you pause or stop the SearchProtocolHost process to debug, the SearchIndexer will launch a new SearchProtocolHost process, invalidating your debugging session.</span></span> <span data-ttu-id="00018-117">此外，如果您將偵錯工具直接附加至 SearchProtocolHost 進程，您可以中斷控制碼繼承，從 searchindexer.exe 到 searchprotocolhost.exe，而這兩個進程將無法進行通訊。</span><span class="sxs-lookup"><span data-stu-id="00018-117">Also, if you attach your debugger directly to the SearchProtocolHost process, you can break handle-inheritance from searchindexer.exe to searchprotocolhost.exe, and the two processes will be unable to communicate.</span></span>

<span data-ttu-id="00018-118">若要避免這些問題，您必須通知搜尋服務您正在進行偵測，而且您必須將偵錯工具附加至 SearchIndexer 進程，並提供偵錯工具子進程的指示，如下所述。</span><span class="sxs-lookup"><span data-stu-id="00018-118">To avoid these problems, you need to notify the search service that you are debugging, and you need to attach the debugger to the SearchIndexer process with instructions to debug child processes, as described next.</span></span>

## <a name="setting-up-debugging"></a><span data-ttu-id="00018-119">設定調試</span><span class="sxs-lookup"><span data-stu-id="00018-119">Setting Up Debugging</span></span>

<span data-ttu-id="00018-120">請遵循下列步驟來設定通訊協定處理常式的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="00018-120">Follow these steps to set up debugging for your protocol handler.</span></span>

1.  <span data-ttu-id="00018-121">將登錄中的 DebugFilters 值設為1，以通知搜尋服務您正在進行偵錯工具：</span><span class="sxs-lookup"><span data-stu-id="00018-121">Notify the search service that you are debugging by setting the DebugFilters value to 1 in the registry:</span></span>

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft
       Windows Search
          Gathering Manager
             DebugFilters = 1
    ```

2.  <span data-ttu-id="00018-122">使用 [影像檔執行選項] 登錄機碼附加偵錯工具：</span><span class="sxs-lookup"><span data-stu-id="00018-122">Attach a debugger using the Image File Execution Options registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion
       Image File Execution Options
          SearchIndexer.exe
             Debugger = <path to debugger> <debugger options> 
    ```

    <span data-ttu-id="00018-123">下表說明範例偵錯工具的選項。</span><span class="sxs-lookup"><span data-stu-id="00018-123">The options for a sample debugger are described in the following table.</span></span>

    

    <span data-ttu-id="00018-124">**使用 ntsd 偵錯工具偵錯工具的範例**   *= C：偵錯工具 \\ \\ntsd.exe-odGx-C： "sxe ld mydll.dll; g"*</span><span class="sxs-lookup"><span data-stu-id="00018-124">**Example using the ntsd debugger**   *Debugger = C:\\debuggers\\ntsd.exe -odGx -c: "sxe ld mydll.dll;g"*</span></span><br/>

3.  <span data-ttu-id="00018-125">使用 compmgmt.msc、services.msc 或命令視窗，在偵錯工具下重新開機 searchindexer.exe，如下所示：</span><span class="sxs-lookup"><span data-stu-id="00018-125">Restart searchindexer.exe under the debugger using compmgmt.msc, services.msc, or a command window with commands similar to the following:</span></span>
    ```
    net stop wsearch
    <copy new DLLs for debugging>
    net start wsearch
            
    ```

    

<span data-ttu-id="00018-126">若要區分在系統內容中執行的 SearchProtocolHost 程式，以及在使用者內容中執行的進程，您可以查看環境字串。</span><span class="sxs-lookup"><span data-stu-id="00018-126">To distinguish between a SearchProtocolHost process running in the system context and one running in the user context, you can review the environment strings.</span></span> <span data-ttu-id="00018-127">例如，有了 ntsd.exe，您可以使用延伸模組命令 **！ peb** ，在流程環境區塊 (peb) 中顯示資訊的格式化視圖。</span><span class="sxs-lookup"><span data-stu-id="00018-127">With ntsd.exe, for example, you can use extension command **!peb** to display a formatted view of the information in the process environment block (PEB).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="00018-128">其他資源</span><span class="sxs-lookup"><span data-stu-id="00018-128">Additional Resources</span></span>

-   <span data-ttu-id="00018-129">如需建立處理常式的詳細資訊，請參閱 [註冊 Shell 擴充](../shell/reg-shell-exts.md)功能。</span><span class="sxs-lookup"><span data-stu-id="00018-129">For information on creating handlers, see [Registering Shell Extensions](../shell/reg-shell-exts.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00018-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="00018-130">Related topics</span></span>

<dl> <span data-ttu-id="00018-131"><dt>**概念**</dt><dt><a href="-search-3x-wds-phaddins.md">開發通訊協定處理常式</a></dt><dt><a href="-search-3x-wds-extidx-prot-implementing.md">瞭解通訊協定處理常式</a></dt>會 <dt><a href="-search-3x-wds-notifyingofchanges.md">通知索引變更</a></dt><dt><a href="-search-3x-wds-ph-ui-extensions.md">新增圖示和內容功能表</a></dt>程式 <dt><a href="-search-3x-wds-ph-ui-samplecode.md">代碼範例：通訊協定處理常式的 Shell 擴充</a></dt>功能為通訊協定處理常式 <dt><a href="-search-3x-wds-ph-search-connector.md">建立搜尋連接器，以便</a></dt><dt><a href="-search-3x-wds-ph-install-registration.md">安裝和註冊通訊協定處理常式</a></dt> </span><span class="sxs-lookup"><span data-stu-id="00018-131"><dt>**Conceptual**</dt> <dt><a href="-search-3x-wds-phaddins.md">Developing Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-extidx-prot-implementing.md">Understanding Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">Notifying the Index of Changes</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">Adding Icons and Context Menus</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">Code Sample: Shell Extensions for Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-ph-search-connector.md">Creating a Search Connector for a Protocol Handler</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">Installing and Registering Protocol Handlers</a></dt> </span></span></dl>

 

 
