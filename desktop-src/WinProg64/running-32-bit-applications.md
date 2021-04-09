---
title: 執行32位應用程式
description: 使用 WOW64 x86 模擬器在64位 Windows 上順暢地執行32位的 Windows 應用程式。 同時瞭解登錄 director、檔案系統重新導向器、64位系統上的應用程式安裝，以及偵錯工具。
ms.assetid: ac75c5af-86e8-4282-9a8e-8db3c22cbda0
keywords:
- WOW64 64 位 Windows 程式設計
- WOW64 64 位 Windows 程式設計，關於
- 64位 Windows 64 位 Windows 程式設計上的32位應用程式
- 64位 Windows 程式設計指南64位 Windows 程式設計，WOW64 請參閱 WOW64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39872be28da0853f0cff62a9a0ab82065105c687
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933292"
---
# <a name="running-32-bit-applications"></a><span data-ttu-id="b46f4-108">執行32位應用程式</span><span class="sxs-lookup"><span data-stu-id="b46f4-108">Running 32-bit Applications</span></span>

<span data-ttu-id="b46f4-109">WOW64 是 x86 模擬器，可讓32位的 Windows 應用程式順暢地在64位 Windows 上執行。</span><span class="sxs-lookup"><span data-stu-id="b46f4-109">WOW64 is the x86 emulator that allows 32-bit Windows-based applications to run seamlessly on 64-bit Windows.</span></span> <span data-ttu-id="b46f4-110">如此一來，就能讓32位 (x86) Windows 應用程式順暢地在64位 (x64) Windows，以及32位 (x86) 和32位 (ARM) Windows 應用程式，以在 64 (ARM64) Windows 中順暢地執行。</span><span class="sxs-lookup"><span data-stu-id="b46f4-110">This allows for 32-bit (x86) Windows applications to run seamlessly in 64-bit (x64) Windows, as well as for 32-bit (x86) and 32-bit (ARM) Windows applications to run seamlessly in 64-bit (ARM64) Windows.</span></span> <span data-ttu-id="b46f4-111">WOW64 是隨作業系統提供，不需要明確啟用。</span><span class="sxs-lookup"><span data-stu-id="b46f4-111">WOW64 is provided with the operating system and does not have to be explicitly enabled.</span></span> <span data-ttu-id="b46f4-112">如需詳細資訊，請參閱 [WOW64 執行詳細資料](wow64-implementation-details.md)。</span><span class="sxs-lookup"><span data-stu-id="b46f4-112">For more information, see [WOW64 Implementation Details](wow64-implementation-details.md).</span></span>

<span data-ttu-id="b46f4-113">系統會隔離32位應用程式與64位應用程式，其中包括防止檔案和登錄衝突。</span><span class="sxs-lookup"><span data-stu-id="b46f4-113">The system isolates 32-bit applications from 64-bit applications, which includes preventing file and registry collisions.</span></span> <span data-ttu-id="b46f4-114">支援主控台、GUI 及服務應用程式。</span><span class="sxs-lookup"><span data-stu-id="b46f4-114">Console, GUI, and service applications are supported.</span></span> <span data-ttu-id="b46f4-115">系統會為剪下和貼上和 COM 等案例提供32/64 界限之間的互通性。</span><span class="sxs-lookup"><span data-stu-id="b46f4-115">The system provides interoperability across the 32/64 boundary for scenarios such as cut and paste and COM.</span></span> <span data-ttu-id="b46f4-116">但是，32位進程無法載入64位 Dll 來執行，而且64位進程無法載入32位 Dll 來執行。</span><span class="sxs-lookup"><span data-stu-id="b46f4-116">However, 32-bit processes cannot load 64-bit DLLs for execution, and 64-bit processes cannot load 32-bit DLLs for execution.</span></span> <span data-ttu-id="b46f4-117">此限制不適用於載入為資料檔案或映射資源檔的 Dll;如需詳細資訊，請參閱 [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa)。</span><span class="sxs-lookup"><span data-stu-id="b46f4-117">This restriction does not apply to DLLs loaded as data files or image resource files; for more information, see [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span></span>

<span data-ttu-id="b46f4-118">32位應用程式可以藉由呼叫 [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) 函式來偵測它是否在 WOW64 下執行， (在以 Windows 10) 為目標時使用 [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2) 。</span><span class="sxs-lookup"><span data-stu-id="b46f4-118">A 32-bit application can detect whether it is running under WOW64 by calling the [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) function (use [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2) if targeting Windows 10).</span></span> <span data-ttu-id="b46f4-119">應用程式可以使用 [**GetNativeSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) 函式來取得處理器的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b46f4-119">The application can obtain additional information about the processor by using the [**GetNativeSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) function.</span></span>

<span data-ttu-id="b46f4-120">請注意，64位 Windows 不支援執行以16位 Windows 為基礎的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b46f4-120">Note that 64-bit Windows does not support running 16-bit Windows-based applications.</span></span> <span data-ttu-id="b46f4-121">主要原因是控制碼在64位的 Windows 上具有32的有效位。</span><span class="sxs-lookup"><span data-stu-id="b46f4-121">The primary reason is that handles have 32 significant bits on 64-bit Windows.</span></span> <span data-ttu-id="b46f4-122">因此，無法將控制碼截斷並傳遞至16位應用程式，而不會遺失資料。</span><span class="sxs-lookup"><span data-stu-id="b46f4-122">Therefore, handles cannot be truncated and passed to 16-bit applications without loss of data.</span></span> <span data-ttu-id="b46f4-123">嘗試啟動16位應用程式失敗，並出現下列錯誤： **錯誤 \_ 的 \_ EXE \_ 格式錯誤**。</span><span class="sxs-lookup"><span data-stu-id="b46f4-123">Attempts to launch 16-bit applications fail with the following error: **ERROR\_BAD\_EXE\_FORMAT**.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b46f4-124">本章節內容</span><span class="sxs-lookup"><span data-stu-id="b46f4-124">In this Section</span></span>

-   [<span data-ttu-id="b46f4-125">WOW64 下的效能和記憶體耗用量</span><span class="sxs-lookup"><span data-stu-id="b46f4-125">Performance and Memory Consumption Under WOW64</span></span>](performance-and-memory-consumption.md)
-   [<span data-ttu-id="b46f4-126">WOW64 執行詳細資料</span><span class="sxs-lookup"><span data-stu-id="b46f4-126">WOW64 Implementation Details</span></span>](wow64-implementation-details.md)
-   [<span data-ttu-id="b46f4-127">登錄重新導向程式</span><span class="sxs-lookup"><span data-stu-id="b46f4-127">Registry Redirector</span></span>](registry-redirector.md)
-   [<span data-ttu-id="b46f4-128">檔案系統重新導向程式</span><span class="sxs-lookup"><span data-stu-id="b46f4-128">File System Redirector</span></span>](file-system-redirector.md)
-   [<span data-ttu-id="b46f4-129">記憶體管理</span><span class="sxs-lookup"><span data-stu-id="b46f4-129">Memory Management</span></span>](memory-management.md)
-   [<span data-ttu-id="b46f4-130">處理器相似性</span><span class="sxs-lookup"><span data-stu-id="b46f4-130">Processor Affinity</span></span>](processor-affinity.md)
-   [<span data-ttu-id="b46f4-131">處理序間通訊</span><span class="sxs-lookup"><span data-stu-id="b46f4-131">Interprocess Communication</span></span>](interprocess-communication.md)
-   [<span data-ttu-id="b46f4-132">應用程式安裝</span><span class="sxs-lookup"><span data-stu-id="b46f4-132">Application Installation</span></span>](application-installation.md)
-   [<span data-ttu-id="b46f4-133">調試 WOW64</span><span class="sxs-lookup"><span data-stu-id="b46f4-133">Debugging WOW64</span></span>](debugging-wow64.md)

 

 