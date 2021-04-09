---
description: 描述調試時，會使用下列詞彙。
ms.assetid: 580f2787-d944-4350-a2c2-c00816b3f515
title: 調試術語
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa12e24a6c763f9cda983ad961ba85a41c63cec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936045"
---
# <a name="debugging-terminology"></a><span data-ttu-id="72fd4-103">調試術語</span><span class="sxs-lookup"><span data-stu-id="72fd4-103">Debugging Terminology</span></span>

<span data-ttu-id="72fd4-104">描述調試時，會使用下列詞彙。</span><span class="sxs-lookup"><span data-stu-id="72fd4-104">The following terms are used when describing debugging.</span></span>

<dl> <dt>

<span data-ttu-id="72fd4-105"><span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>藍色畫面</span><span class="sxs-lookup"><span data-stu-id="72fd4-105"><span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Blue screen</span></span>
</dt> <dd>

<span data-ttu-id="72fd4-106">當系統發生硬體問題、資料不一致或類似的錯誤時，可能會顯示藍色畫面，其中包含可用來判斷錯誤原因的資訊。</span><span class="sxs-lookup"><span data-stu-id="72fd4-106">When the system encounters a hardware problem, data inconsistency, or similar error, it may display a blue screen containing information that can be used to determine the cause of the error.</span></span> <span data-ttu-id="72fd4-107">此資訊包含停止程式碼，以及是否已建立損毀傾印檔案。</span><span class="sxs-lookup"><span data-stu-id="72fd4-107">This information includes the STOP code and whether a crash dump file was created.</span></span> <span data-ttu-id="72fd4-108">它也可能包含已載入的驅動程式清單和堆疊追蹤。</span><span class="sxs-lookup"><span data-stu-id="72fd4-108">It may also include a list of loaded drivers and a stack trace.</span></span>

</dd> <dt>

<span data-ttu-id="72fd4-109"><span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>損毀傾印檔案</span><span class="sxs-lookup"><span data-stu-id="72fd4-109"><span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Crash dump file</span></span>
</dt> <dd>

<span data-ttu-id="72fd4-110">您可以設定系統在每次產生停止程式碼時，將資訊寫入硬碟中的損毀傾印檔案。</span><span class="sxs-lookup"><span data-stu-id="72fd4-110">You can configure the system to write information to a crash dump file on your hard disk whenever a STOP code is generated.</span></span> <span data-ttu-id="72fd4-111">檔案包含偵錯工具可以用來分析錯誤的資訊。</span><span class="sxs-lookup"><span data-stu-id="72fd4-111">The file contains information the debugger can use to analyze the error.</span></span> <span data-ttu-id="72fd4-112">這個檔案可以與電腦中包含的實體記憶體一樣大。</span><span class="sxs-lookup"><span data-stu-id="72fd4-112">This file can be as big as the physical memory contained in the computer.</span></span>

</dd> <dt>

<span data-ttu-id="72fd4-113"><span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>調試</span><span class="sxs-lookup"><span data-stu-id="72fd4-113"><span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Debugger</span></span>
</dt> <dd>

<span data-ttu-id="72fd4-114">設計用來協助偵測、找出及修正另一個程式中錯誤的程式。</span><span class="sxs-lookup"><span data-stu-id="72fd4-114">A program designed to help detect, locate, and correct errors in another program.</span></span> <span data-ttu-id="72fd4-115">它可讓開發人員逐步執行進程及其執行緒、監視記憶體、變數，以及進程和執行緒內容的其他元素。</span><span class="sxs-lookup"><span data-stu-id="72fd4-115">It allows the developer to step through the execution of the process and its threads, monitoring memory, variables, and other elements of process and thread context.</span></span>

</dd> <dt>

<span data-ttu-id="72fd4-116"><span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>核心模式</span><span class="sxs-lookup"><span data-stu-id="72fd4-116"><span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Kernel mode</span></span>
</dt> <dd>

<span data-ttu-id="72fd4-117">執行系統服務和設備磁碟機的處理器模式。</span><span class="sxs-lookup"><span data-stu-id="72fd4-117">The processor mode in which system services and device drivers run.</span></span> <span data-ttu-id="72fd4-118">所有介面和 CPU 指令都可供使用，而且可以存取所有的記憶體。</span><span class="sxs-lookup"><span data-stu-id="72fd4-118">All interfaces and CPU instructions are available, and all memory is accessible.</span></span>

</dd> <dt>

<span data-ttu-id="72fd4-119"><span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>小型傾印檔案</span><span class="sxs-lookup"><span data-stu-id="72fd4-119"><span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Minidump file</span></span>
</dt> <dd>

<span data-ttu-id="72fd4-120">應用程式可以產生使用者模式小型傾印檔案，其中包含損毀傾印檔案中包含的有用資訊子集。</span><span class="sxs-lookup"><span data-stu-id="72fd4-120">Applications can produce user-mode minidump files, which contain a useful subset of the information contained in a crash dump file.</span></span> <span data-ttu-id="72fd4-121">如需詳細資訊，請參閱 [小型](minidump-files.md)傾印檔案。</span><span class="sxs-lookup"><span data-stu-id="72fd4-121">For more information, see [Minidump Files](minidump-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="72fd4-122"><span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>停止程式碼</span><span class="sxs-lookup"><span data-stu-id="72fd4-122"><span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>STOP code</span></span>
</dt> <dd>

<span data-ttu-id="72fd4-123">指出停止系統核心繼續執行的錯誤的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="72fd4-123">The error code that identifies the error that stopped the system kernel from continuing to run.</span></span>

</dd> <dt>

<span data-ttu-id="72fd4-124"><span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>符號檔</span><span class="sxs-lookup"><span data-stu-id="72fd4-124"><span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Symbol files</span></span>
</dt> <dd>

<span data-ttu-id="72fd4-125">系統會建立所有系統應用程式、驅動程式和 Dll，使其偵錯工具資訊位於稱為符號檔的個別檔案中。</span><span class="sxs-lookup"><span data-stu-id="72fd4-125">All system applications, drivers, and DLLs are built such that their debugging information resides in separate files known as symbol files.</span></span> <span data-ttu-id="72fd4-126">因此，系統會變得更小且更快，但如果已安裝符號檔，仍然可以進行調試。</span><span class="sxs-lookup"><span data-stu-id="72fd4-126">Therefore, the system is smaller and faster, yet it can still be debugged if the symbol files are installed.</span></span> <span data-ttu-id="72fd4-127">如需詳細資訊，請參閱 [符號](symbol-files.md)檔。</span><span class="sxs-lookup"><span data-stu-id="72fd4-127">For more information, see [Symbol Files](symbol-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="72fd4-128"><span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>使用者模式</span><span class="sxs-lookup"><span data-stu-id="72fd4-128"><span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>User mode</span></span>
</dt> <dd>

<span data-ttu-id="72fd4-129">應用程式執行所在的處理器模式。</span><span class="sxs-lookup"><span data-stu-id="72fd4-129">The processor mode in which applications run.</span></span> <span data-ttu-id="72fd4-130">在此模式中有一組有限的介面可供使用，而且系統資料的存取會受到限制。</span><span class="sxs-lookup"><span data-stu-id="72fd4-130">A limited set of interfaces are available in this mode, and access to system data is limited.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="72fd4-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="72fd4-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72fd4-132">設定自動調試</span><span class="sxs-lookup"><span data-stu-id="72fd4-132">Configuring Automatic Debugging</span></span>](configuring-automatic-debugging.md)
</dt> </dl>

 

 



