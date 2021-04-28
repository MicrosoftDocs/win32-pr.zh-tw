---
description: 僅限64位
ms.assetid: 5d0188a5-ef5f-409e-9d2d-7639d99edc1d
title: 僅限64位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d896fcaf4b8c4ebeadf7cfd5a5c22e511cb659
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088806"
---
# <a name="64-bit-only"></a><span data-ttu-id="ec00b-103">僅限64位</span><span class="sxs-lookup"><span data-stu-id="ec00b-103">64-Bit Only</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="ec00b-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="ec00b-104">Affected Platforms</span></span>

<span data-ttu-id="ec00b-105">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec00b-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="ec00b-106">功能影響</span><span class="sxs-lookup"><span data-stu-id="ec00b-106">Feature Impact</span></span>

 <span data-ttu-id="ec00b-107">**嚴重性** -低</span><span class="sxs-lookup"><span data-stu-id="ec00b-107">**Severity** - Low</span></span>  
<span data-ttu-id="ec00b-108">**頻率** -高</span><span class="sxs-lookup"><span data-stu-id="ec00b-108">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="ec00b-109">Description</span><span class="sxs-lookup"><span data-stu-id="ec00b-109">Description</span></span>

<span data-ttu-id="ec00b-110">Windows Server 2008 R2 僅隨附64位 SKU;伺服器版本的作業系統沒有32位 SKU 可用。</span><span class="sxs-lookup"><span data-stu-id="ec00b-110">Windows Server 2008 R2 ships with a 64-bit SKU only; no 32-bit SKU is available for the server version of the operating system.</span></span> <span data-ttu-id="ec00b-111">不過，Windows 7 用戶端仍可繼續使用32位 SKU。</span><span class="sxs-lookup"><span data-stu-id="ec00b-111">However, a 32-bit SKU continues to be available for the Windows 7 client.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="ec00b-112">影響的表現</span><span class="sxs-lookup"><span data-stu-id="ec00b-112">Manifestation of Impact</span></span>

<span data-ttu-id="ec00b-113">這會影響三個區域：</span><span class="sxs-lookup"><span data-stu-id="ec00b-113">This will impact three areas:</span></span>

-   <span data-ttu-id="ec00b-114">32位驅動程式</span><span class="sxs-lookup"><span data-stu-id="ec00b-114">32-bit drivers</span></span>
-   <span data-ttu-id="ec00b-115">32位外掛程式</span><span class="sxs-lookup"><span data-stu-id="ec00b-115">32-bit plug-ins</span></span>
-   <span data-ttu-id="ec00b-116">16位可執行檔</span><span class="sxs-lookup"><span data-stu-id="ec00b-116">16-bit executables</span></span>

## <a name="solution-for-32-bit-drivers"></a><span data-ttu-id="ec00b-117">32位驅動程式的解決方案</span><span class="sxs-lookup"><span data-stu-id="ec00b-117">Solution for 32-bit Drivers</span></span>

<span data-ttu-id="ec00b-118">將32位驅動程式重新編譯為帶正負號的64位驅動程式。</span><span class="sxs-lookup"><span data-stu-id="ec00b-118">Recompile 32-bit drivers as signed 64-bit drivers.</span></span>

## <a name="solution-for-32-bit-plug-ins"></a><span data-ttu-id="ec00b-119">32位外掛程式的解決方案</span><span class="sxs-lookup"><span data-stu-id="ec00b-119">Solution for 32-bit Plug-ins</span></span>

<span data-ttu-id="ec00b-120">WoW64 是 x86 模擬器，可讓32位的 Windows 應用程式順暢地在64位 Windows 上執行。</span><span class="sxs-lookup"><span data-stu-id="ec00b-120">WoW64, an x86 emulator, allows 32-bit Windows-based applications to run seamlessly on 64-bit Windows.</span></span> <span data-ttu-id="ec00b-121">WoW64 現在是選用的功能，如果需要執行32位程式碼，則必須安裝此功能。</span><span class="sxs-lookup"><span data-stu-id="ec00b-121">WoW64 is now an optional feature that you must install if it is necessary to run 32-bit code.</span></span>

<span data-ttu-id="ec00b-122">系統會隔離32位應用程式與64位應用程式，其中包括防止檔案和登錄衝突。</span><span class="sxs-lookup"><span data-stu-id="ec00b-122">The system isolates 32-bit applications from 64-bit applications, which includes preventing file and registry collisions.</span></span> <span data-ttu-id="ec00b-123">支援主控台、GUI 及服務應用程式。</span><span class="sxs-lookup"><span data-stu-id="ec00b-123">Console, GUI, and service applications are supported.</span></span> <span data-ttu-id="ec00b-124">系統會為剪下和貼上和 COM 等案例提供32/64 界限之間的互通性。</span><span class="sxs-lookup"><span data-stu-id="ec00b-124">The system provides interoperability across the 32/64 boundary for scenarios such as cut and paste and COM.</span></span> <span data-ttu-id="ec00b-125">但是，32位進程無法載入64位的 Dll，而64位進程無法載入32位 Dll。</span><span class="sxs-lookup"><span data-stu-id="ec00b-125">However, 32-bit processes cannot load 64-bit DLLs, and 64-bit processes cannot load 32-bit DLLs.</span></span> <span data-ttu-id="ec00b-126">在針對 Windows 檔案總管所撰寫的 shell 外掛程式中，我們通常會看到這種情況。</span><span class="sxs-lookup"><span data-stu-id="ec00b-126">We commonly see this in shell plug-ins written for Windows Explorer.</span></span>

<span data-ttu-id="ec00b-127">32位應用程式可以藉由呼叫 IsWow64Process 函式，來偵測它是否正在 WOW64 下執行。</span><span class="sxs-lookup"><span data-stu-id="ec00b-127">A 32-bit application can detect whether it is running under WOW64 by calling the IsWow64Process function.</span></span> <span data-ttu-id="ec00b-128">應用程式可以使用 GetNativeSystemInfo 函式來取得處理器的其他相關資訊</span><span class="sxs-lookup"><span data-stu-id="ec00b-128">The application can obtain additional information about the processor by using the GetNativeSystemInfo function</span></span>

<span data-ttu-id="ec00b-129">請注意，64位 Windows 不支援執行以16位 Windows 為基礎的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ec00b-129">Note that 64-bit Windows does not support running 16-bit Windows-based applications.</span></span> <span data-ttu-id="ec00b-130">主要原因是控制碼在64位的 Windows 上具有32的有效位。</span><span class="sxs-lookup"><span data-stu-id="ec00b-130">The primary reason is that handles have 32 significant bits on 64-bit Windows.</span></span> <span data-ttu-id="ec00b-131">因此，無法將控制碼截斷並傳遞至16位應用程式，而不會遺失資料。</span><span class="sxs-lookup"><span data-stu-id="ec00b-131">Therefore, handles cannot be truncated and passed to 16-bit applications without loss of data.</span></span> <span data-ttu-id="ec00b-132">嘗試啟動16位應用程式失敗，並出現下列錯誤：錯誤 \_ 的 \_ EXE \_ 格式錯誤。</span><span class="sxs-lookup"><span data-stu-id="ec00b-132">Attempts to launch 16-bit applications fail with the following error: ERROR\_BAD\_EXE\_FORMAT.</span></span>

## <a name="solution-for-16-bit-executables"></a><span data-ttu-id="ec00b-133">16位可執行檔的解決方案</span><span class="sxs-lookup"><span data-stu-id="ec00b-133">Solution for 16-bit Executables</span></span>

<span data-ttu-id="ec00b-134">64位 Windows 會辨識有限數量的特定16位安裝程式，並替代已移植的32位版本。</span><span class="sxs-lookup"><span data-stu-id="ec00b-134">64-bit Windows recognizes a limited number of specific 16-bit installer programs and substitutes a ported 32-bit version.</span></span> <span data-ttu-id="ec00b-135">替代清單會儲存在登錄中的下列機碼底下： HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion NtVdm64 內 \\ 建支援數個安裝程式引擎，包括 InstallShield 5.x 安裝程式。</span><span class="sxs-lookup"><span data-stu-id="ec00b-135">The list of substitutions is stored in the registry under the following key: HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\NtVdm64 There is built-in support for several installer engines, including InstallShield 5.x installers.</span></span> <span data-ttu-id="ec00b-136">請注意，64位的 Windows Installer 可以在64位的 Windows 上順暢地安裝32位的 MSI 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ec00b-136">Note that the 64-bit Windows Installer can seamlessly install 32-bit MSI-based applications on 64-bit Windows.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="ec00b-137">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="ec00b-137">Links to Other Resources</span></span>

-   [<span data-ttu-id="ec00b-138">執行32位應用程式</span><span class="sxs-lookup"><span data-stu-id="ec00b-138">Running 32-bit Applications</span></span>](/windows/desktop/WinProg64/running-32-bit-applications)
-   [<span data-ttu-id="ec00b-139">效能和記憶體耗用量</span><span class="sxs-lookup"><span data-stu-id="ec00b-139">Performance and Memory Consumption</span></span>](/windows/desktop/WinProg64/performance-and-memory-consumption)
-   [<span data-ttu-id="ec00b-140">WOW64 執行詳細資料</span><span class="sxs-lookup"><span data-stu-id="ec00b-140">WOW64 Implementation Details</span></span>](/windows/desktop/WinProg64/wow64-implementation-details)
-   [<span data-ttu-id="ec00b-141">登錄重新導向程式</span><span class="sxs-lookup"><span data-stu-id="ec00b-141">Registry Redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
-   [<span data-ttu-id="ec00b-142">檔案系統重新導向程式</span><span class="sxs-lookup"><span data-stu-id="ec00b-142">File System Redirector</span></span>](/windows/desktop/WinProg64/file-system-redirector)
-   [<span data-ttu-id="ec00b-143">記憶體管理</span><span class="sxs-lookup"><span data-stu-id="ec00b-143">Memory Management</span></span>](/windows/desktop/WinProg64/memory-management)
-   [<span data-ttu-id="ec00b-144">處理器相似性</span><span class="sxs-lookup"><span data-stu-id="ec00b-144">Processor Affinity</span></span>](/windows/desktop/WinProg64/processor-affinity)
-   [<span data-ttu-id="ec00b-145">處理序間通訊</span><span class="sxs-lookup"><span data-stu-id="ec00b-145">Interprocess Communication</span></span>](/windows/desktop/WinProg64/interprocess-communication)
-   [<span data-ttu-id="ec00b-146">64位系統上的應用程式安裝</span><span class="sxs-lookup"><span data-stu-id="ec00b-146">Application Installation on 64-bit Systems</span></span>](/windows/desktop/WinProg64/application-installation)
-   [<span data-ttu-id="ec00b-147">調試 WOW64</span><span class="sxs-lookup"><span data-stu-id="ec00b-147">Debugging WOW64</span></span>](/windows/desktop/WinProg64/debugging-wow64)
-   [<span data-ttu-id="ec00b-148">**IsWow64Process 函式**</span><span class="sxs-lookup"><span data-stu-id="ec00b-148">**IsWow64Process Function**</span></span>](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process)
-   [<span data-ttu-id="ec00b-149">**GetNativeSystemInfo 函式**</span><span class="sxs-lookup"><span data-stu-id="ec00b-149">**GetNativeSystemInfo Function**</span></span>](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

 

 
