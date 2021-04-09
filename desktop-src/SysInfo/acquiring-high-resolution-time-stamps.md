---
description: Windows 提供的 Api 可讓您用來取得高解析度的時間戳記或測量時間間隔。
ms.assetid: D66E0FC2-3AF2-489B-B4B5-78648905B77B
title: 取得高解析度時間戳記
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9a1300967738b717ab8d8c822bf2af3f6a4a7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945493"
---
# <a name="acquiring-high-resolution-time-stamps"></a><span data-ttu-id="f321e-103">取得高解析度時間戳記</span><span class="sxs-lookup"><span data-stu-id="f321e-103">Acquiring high-resolution time stamps</span></span>

<span data-ttu-id="f321e-104">Windows 提供的 Api 可讓您用來取得高解析度的時間戳記或測量時間間隔。</span><span class="sxs-lookup"><span data-stu-id="f321e-104">Windows provides APIs that you can use to acquire high-resolution time stamps or measure time intervals.</span></span> <span data-ttu-id="f321e-105">原生程式碼的主要 API 是 [**QueryPerformanceCounter (QPC)**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)。</span><span class="sxs-lookup"><span data-stu-id="f321e-105">The primary API for native code is [**QueryPerformanceCounter (QPC)**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span> <span data-ttu-id="f321e-106">若為設備磁碟機，則會 [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter)核心模式 API。</span><span class="sxs-lookup"><span data-stu-id="f321e-106">For device drivers, the kernel-mode API is [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter).</span></span> <span data-ttu-id="f321e-107">針對 managed 程式碼， [**system.object**](/previous-versions/windows/) 類別會使用 **QPC** 做為精確的時間。</span><span class="sxs-lookup"><span data-stu-id="f321e-107">For managed code, the [**System.Diagnostics.Stopwatch**](/previous-versions/windows/) class uses **QPC** as its precise time basis.</span></span>

<span data-ttu-id="f321e-108">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 與無關，且不會同步處理至任何外部時間參考。</span><span class="sxs-lookup"><span data-stu-id="f321e-108">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) is independent of and isn't synchronized to any external time reference.</span></span> <span data-ttu-id="f321e-109">若要取出可同步處理至外部時間參考的時間戳記，例如，國際標準時間 (UTC) 以用於高解析度的當日時間測量，請使用 [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime)。</span><span class="sxs-lookup"><span data-stu-id="f321e-109">To retrieve time stamps that can be synchronized to an external time reference, such as, Coordinated Universal Time (UTC) for use in high-resolution time-of-day measurements, use [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).</span></span>

<span data-ttu-id="f321e-110">時間戳記和時間間隔測量是電腦和網路效能測量的不可或缺部分。</span><span class="sxs-lookup"><span data-stu-id="f321e-110">Time stamps and time-interval measurements are an integral part of computer and network performance measurements.</span></span> <span data-ttu-id="f321e-111">這些效能測量作業包括計算回應時間、輸送量和延遲，以及分析程式碼執行。</span><span class="sxs-lookup"><span data-stu-id="f321e-111">These performance measurement operations include the computation of response time, throughput, and latency as well as profiling code execution.</span></span> <span data-ttu-id="f321e-112">每一項作業都牽涉到在時間間隔內發生的活動量測，此時間間隔是由 start 和 end 事件所定義，而該時間間隔可以與任何外部的日期時間參考無關。</span><span class="sxs-lookup"><span data-stu-id="f321e-112">Each of these operations involves a measurement of activities that occur during a time interval that is defined by a start and an end event that can be independent of any external time-of-day reference.</span></span>

<span data-ttu-id="f321e-113">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 通常是使用時間戳事件的最佳方法，並測量在相同系統或虛擬機器上發生的小時間間隔。</span><span class="sxs-lookup"><span data-stu-id="f321e-113">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) is typically the best method to use to time-stamp events and measure small time intervals that occur on the same system or virtual machine.</span></span> <span data-ttu-id="f321e-114">當您想要在多部電腦上使用時間戳事件時，請考慮使用 [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) ，前提是每台機器都參與時間同步處理配置，例如網路時間通訊協定 (NTP) 。</span><span class="sxs-lookup"><span data-stu-id="f321e-114">Consider using [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) when you want to time-stamp events across multiple machines, provided that each machine is participating in a time synchronization scheme such as Network Time Protocol (NTP).</span></span> <span data-ttu-id="f321e-115">**QPC** 可協助您避免其他時間測量方法可能遇到的問題，例如直接讀取處理器的時間戳記計數器 (的 TSC) 。</span><span class="sxs-lookup"><span data-stu-id="f321e-115">**QPC** helps you avoid difficulties that can be encountered with other time measurement approaches, such as reading the processor’s time stamp counter (TSC) directly.</span></span>

-   [<span data-ttu-id="f321e-116">Windows 版本中的 QPC 支援</span><span class="sxs-lookup"><span data-stu-id="f321e-116">QPC support in Windows versions</span></span>](#qpc-support-in-windows-versions)
-   [<span data-ttu-id="f321e-117">取得時間戳記的指引</span><span class="sxs-lookup"><span data-stu-id="f321e-117">Guidance for acquiring time stamps</span></span>](#guidance-for-acquiring-time-stamps)
    -   [<span data-ttu-id="f321e-118">虛擬化</span><span class="sxs-lookup"><span data-stu-id="f321e-118">Virtualization</span></span>](#virtualization)
    -   [<span data-ttu-id="f321e-119">直接的 TSC 使用方式</span><span class="sxs-lookup"><span data-stu-id="f321e-119">Direct TSC usage</span></span>](#direct-tsc-usage)
    -   [<span data-ttu-id="f321e-120">取得時間戳記的範例</span><span class="sxs-lookup"><span data-stu-id="f321e-120">Examples for acquiring time stamps</span></span>](#examples-for-acquiring-time-stamps)
-   [<span data-ttu-id="f321e-121">關於 QPC 和 TSC 的一般常見問題</span><span class="sxs-lookup"><span data-stu-id="f321e-121">General FAQ about QPC and TSC</span></span>](#general-faq-about-qpc-and-tsc)
-   [<span data-ttu-id="f321e-122">使用 QPC 和 TSC 進行程式設計的常見問題</span><span class="sxs-lookup"><span data-stu-id="f321e-122">FAQ about programming with QPC and TSC</span></span>](#faq-about-programming-with-qpc-and-tsc)
-   [<span data-ttu-id="f321e-123">低層級硬體時鐘特性</span><span class="sxs-lookup"><span data-stu-id="f321e-123">Low-level hardware clock characteristics</span></span>](#low-level-hardware-clock-characteristics)
    -   [<span data-ttu-id="f321e-124">絕對時鐘和差異時鐘</span><span class="sxs-lookup"><span data-stu-id="f321e-124">Absolute Clocks and Difference Clocks</span></span>](#absolute-clocks-and-difference-clocks)
    -   [<span data-ttu-id="f321e-125">解析度、有效位數、精確度和穩定性</span><span class="sxs-lookup"><span data-stu-id="f321e-125">Resolution, Precision, Accuracy, and Stability</span></span>](#resolution-precision-accuracy-and-stability)
-   [<span data-ttu-id="f321e-126">硬體計時器資訊</span><span class="sxs-lookup"><span data-stu-id="f321e-126">Hardware timer info</span></span>](#hardware-timer-info)

## <a name="qpc-support-in-windows-versions"></a><span data-ttu-id="f321e-127">Windows 版本中的 QPC 支援</span><span class="sxs-lookup"><span data-stu-id="f321e-127">QPC support in Windows versions</span></span>

<span data-ttu-id="f321e-128">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 是在 windows 2000 和 windows XP 中引進，並已發展成可利用硬體平臺和處理器的增強功能。</span><span class="sxs-lookup"><span data-stu-id="f321e-128">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) was introduced in Windows 2000 and Windows XP and has evolved to take advantage of improvements in the hardware platform and processors.</span></span> <span data-ttu-id="f321e-129">我們在此說明不同 Windows 版本的 **QPC** 特性，以協助您維護在這些 windows 版本上執行的軟體。</span><span class="sxs-lookup"><span data-stu-id="f321e-129">Here we describe the characteristics of **QPC** on different Windows versions to help you maintain software that runs on those Windows versions.</span></span>

### <a name="windows-xp-and-windows-2000"></a><span data-ttu-id="f321e-130">Windows XP 和 Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f321e-130">Windows XP and Windows 2000</span></span>

<span data-ttu-id="f321e-131">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 可在 windows XP 與 windows 2000 上取得，並且在大部分的系統上都能順利運作。</span><span class="sxs-lookup"><span data-stu-id="f321e-131">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) is available on Windows XP and Windows 2000 and works well on most systems.</span></span> <span data-ttu-id="f321e-132">不過，某些硬體系統的 BIOS 並未正確指出硬體 CPU 特性 (非不變異的 TSC) ，而某些多核心或多處理器系統使用的處理器與 TSCs 無法跨核心進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="f321e-132">However, some hardware systems' BIOS didn't indicate the hardware CPU characteristics correctly (a non-invariant TSC), and some multi-core or multi-processor systems used processors with TSCs that couldn't be synchronized across cores.</span></span> <span data-ttu-id="f321e-133">如果系統具有執行這些 Windows 版本之有瑕疵的固件，執行這些版本的 Windows 可能不會在不同的核心上提供相同的 **QPC** 讀取，如果它們使用了 TSC 作為 **QPC** 的基礎。</span><span class="sxs-lookup"><span data-stu-id="f321e-133">Systems with flawed firmware that run these versions of Windows might not provide the same **QPC** reading on different cores if they used the TSC as the basis for **QPC**.</span></span>

### <a name="windows-vista-and-windows-server-2008"></a><span data-ttu-id="f321e-134">Windows Vista 與 Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f321e-134">Windows Vista and Windows Server 2008</span></span>

<span data-ttu-id="f321e-135">Windows Vista 和 Windows Server 2008 隨附的所有電腦都使用 platform 計數器 (高精確度的事件計時器 (HPET) ) 或 ACPI 電源管理計時器 (PM 計時器) 作為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)的基礎。</span><span class="sxs-lookup"><span data-stu-id="f321e-135">All computers that shipped with Windows Vista and Windows Server 2008 used a platform counter (High Precision Event Timer (HPET)) or the ACPI Power Management Timer (PM timer) as the basis for [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span> <span data-ttu-id="f321e-136">這類平臺計時器具有比 TSC 更高的存取延遲，而且會在多個處理器之間共用。</span><span class="sxs-lookup"><span data-stu-id="f321e-136">Such platform timers have higher access latency than the TSC and are shared between multiple processors.</span></span> <span data-ttu-id="f321e-137">如果是從多個處理器同時呼叫，這會限制 **QPC** 的擴充性。</span><span class="sxs-lookup"><span data-stu-id="f321e-137">This limits scalability of **QPC** if it is called concurrently from multiple processors.</span></span>

### <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="f321e-138">Windows 7 與 Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f321e-138">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="f321e-139">大部分的 Windows 7 和 Windows Server 2008 R2 電腦都有具有固定速率 TSCs 的處理器，並使用這些計數器作為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)的基礎。</span><span class="sxs-lookup"><span data-stu-id="f321e-139">The majority of Windows 7 and Windows Server 2008 R2 computers have processors with constant-rate TSCs and use these counters as the basis for [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span> <span data-ttu-id="f321e-140">TSCs 是高解析度的每個處理器硬體計數器，可利用非常低的延遲和額外負荷 (，視10s 或數百部機器週期的順序而定，這取決於處理器類型) 。</span><span class="sxs-lookup"><span data-stu-id="f321e-140">TSCs are high-resolution per-processor hardware counters that can be accessed with very low latency and overhead (in the order of 10s or 100s of machine cycles, depending on the processor type).</span></span> <span data-ttu-id="f321e-141">Windows 7 和 Windows Server 2008 R2 使用 TSCs 做為單一時鐘網域系統上的 **QPC** 基礎，其中作業系統 (或執行程式) 能夠在系統初始化期間，在所有處理器之間緊密地同步處理個別 TSCs。</span><span class="sxs-lookup"><span data-stu-id="f321e-141">Windows 7 and Windows Server 2008 R2 use TSCs as the basis of **QPC** on single-clock domain systems where the operating system (or the hypervisor) is able to tightly synchronize the individual TSCs across all processors during system initialization.</span></span> <span data-ttu-id="f321e-142">在這類系統上，相較于使用 platform 計數器的系統，讀取效能計數器的成本明顯較低。</span><span class="sxs-lookup"><span data-stu-id="f321e-142">On such systems, the cost of reading the performance counter is significantly lower compared to systems that use a platform counter.</span></span> <span data-ttu-id="f321e-143">此外，並行呼叫也不會有額外的負荷，而且使用者模式查詢通常會略過系統呼叫，進而減少額外負荷。</span><span class="sxs-lookup"><span data-stu-id="f321e-143">Furthermore, there is no added overhead for concurrent calls and user-mode queries often bypass system calls, which further reduces overhead.</span></span> <span data-ttu-id="f321e-144">在不適合 timekeeping 的系統上，Windows 會自動選取平臺計數器， (HPET 計時器或 ACPI PM 計時器) 作為 **QPC** 的基礎。</span><span class="sxs-lookup"><span data-stu-id="f321e-144">On systems where the TSC is not suitable for timekeeping, Windows automatically selects a platform counter (either the HPET timer or the ACPI PM timer) as the basis for **QPC**.</span></span>

### <a name="windows-8-windows-81-windows-server-2012-and-windows-server-2012-r2"></a><span data-ttu-id="f321e-145">Windows 8、Windows 8.1、Windows Server 2012 和 Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f321e-145">Windows 8, Windows 8.1, Windows Server 2012, and Windows Server 2012 R2</span></span>

<span data-ttu-id="f321e-146">Windows 8、Windows 8.1、Windows Server 2012 和 Windows Server 2012 R2 使用 TSCs 做為效能計數器的基礎。</span><span class="sxs-lookup"><span data-stu-id="f321e-146">Windows 8, Windows 8.1, Windows Server 2012, and Windows Server 2012 R2 use TSCs as the basis for the performance counter.</span></span> <span data-ttu-id="f321e-147">已大幅改善 TSC 同步處理演算法，以更妥善容納具有許多處理器的大型系統。</span><span class="sxs-lookup"><span data-stu-id="f321e-147">The TSC synchronization algorithm was significantly improved to better accommodate large systems with many processors.</span></span> <span data-ttu-id="f321e-148">此外，也新增了新的精確時間 API 支援，可讓您從作業系統取得精確的時鐘時間戳記。</span><span class="sxs-lookup"><span data-stu-id="f321e-148">In addition, support for the new precise time-of-day API was added, which enables acquiring precise wall clock time stamps from the operating system.</span></span> <span data-ttu-id="f321e-149">如需詳細資訊，請參閱 [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime)。</span><span class="sxs-lookup"><span data-stu-id="f321e-149">For more info, see [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).</span></span> <span data-ttu-id="f321e-150">在 Windows RT 電腦平臺上，效能計數器會以專屬平臺計數器或 Windows RT PC 一般計時器提供的系統計數器為基礎（如果平臺已有配備的話）。</span><span class="sxs-lookup"><span data-stu-id="f321e-150">On Windows RT PC platforms, the performance counter is based on either a proprietary platform counter or the system counter provided by the Windows RT PC Generic Timer if the platform is so equipped.</span></span>

## <a name="guidance-for-acquiring-time-stamps"></a><span data-ttu-id="f321e-151">取得時間戳記的指引</span><span class="sxs-lookup"><span data-stu-id="f321e-151">Guidance for acquiring time stamps</span></span>

<span data-ttu-id="f321e-152">Windows 具有並將繼續投資提供可靠且有效率的效能計數器。</span><span class="sxs-lookup"><span data-stu-id="f321e-152">Windows has and will continue to invest in providing a reliable and efficient performance counter.</span></span> <span data-ttu-id="f321e-153">當您需要以1微秒或更高解析度的時間戳記，而不需要將時間戳記同步處理至外部時間參考時，請選擇 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)、 [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter)或 [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise)。</span><span class="sxs-lookup"><span data-stu-id="f321e-153">When you need time stamps with a resolution of 1 microsecond or better and you don't need the time stamps to be synchronized to an external time reference, choose [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter), [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter), or [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise).</span></span> <span data-ttu-id="f321e-154">當您需要解析為1微秒或更高的 UTC 同步處理時間戳記時，請選擇 [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) 或 [**KeQuerySystemTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequerysystemtimeprecise)。</span><span class="sxs-lookup"><span data-stu-id="f321e-154">When you need UTC-synchronized time stamps with a resolution of 1 microsecond or better, choose [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime) or [**KeQuerySystemTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequerysystemtimeprecise).</span></span>

<span data-ttu-id="f321e-155">在相對較少的平臺上，無法使用 TSC 註冊作為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 基礎，例如，基於 [硬體計時器資訊](#hardware-timer-info)中所述的原因，取得高解析度的時間戳記可能會比取得較低解析度的時間戳記更昂貴。</span><span class="sxs-lookup"><span data-stu-id="f321e-155">On a relatively small number of platforms that can't use the TSC register as the [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) basis, for example, for reasons explained in [Hardware timer info](#hardware-timer-info), acquiring high resolution time stamps can be significantly more expensive than acquiring time stamps with lower resolution.</span></span> <span data-ttu-id="f321e-156">如果10到16毫秒的解析已足夠，您可以使用 [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64)、 [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)、 [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)、 [**KeQueryInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttime)或 [**KeQueryUnbiasedInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryunbiasedinterrupttime) 來取得未同步處理至外部時間參考的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="f321e-156">If resolution of 10 to 16 milliseconds is sufficient, you can use [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64), [**QueryInterruptTime**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime), [**QueryUnbiasedInterruptTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime), [**KeQueryInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttime), or [**KeQueryUnbiasedInterruptTime**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryunbiasedinterrupttime) to obtain time stamps that aren't synchronized to an external time reference.</span></span> <span data-ttu-id="f321e-157">針對 UTC 同步處理的時間戳記，請使用 [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) 或 [**KeQuerySystemTime**](/windows-hardware/drivers/ddi/wdm/nf-wdm-kequerysystemtime~r1)。</span><span class="sxs-lookup"><span data-stu-id="f321e-157">For UTC-synchronized time stamps, use [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) or [**KeQuerySystemTime**](/windows-hardware/drivers/ddi/wdm/nf-wdm-kequerysystemtime~r1).</span></span> <span data-ttu-id="f321e-158">如果需要較高的解析度，您可以使用 [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)、 [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise)或 [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise) 來改為取得時間戳記。</span><span class="sxs-lookup"><span data-stu-id="f321e-158">If higher resolution is needed, you can use [**QueryInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise), [**QueryUnbiasedInterruptTimePrecise**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise), or [**KeQueryInterruptTimePrecise**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kequeryinterrupttimeprecise) to obtain time stamps instead.</span></span>

<span data-ttu-id="f321e-159">一般來說，即使是在不同的執行緒或進程上測量，效能計數器的結果仍會在多核心和多處理器系統中的所有處理器之間保持一致。</span><span class="sxs-lookup"><span data-stu-id="f321e-159">In general, the performance counter results are consistent across all processors in multi-core and multi-processor systems, even when measured on different threads or processes.</span></span> <span data-ttu-id="f321e-160">以下是此規則的一些例外狀況：</span><span class="sxs-lookup"><span data-stu-id="f321e-160">Here are some exceptions to this rule:</span></span>

-   <span data-ttu-id="f321e-161">基於下列其中一個原因，在特定處理器上執行的 Windows Vista 作業系統可能會違反此一致性：</span><span class="sxs-lookup"><span data-stu-id="f321e-161">Pre-Windows Vista operating systems that run on certain processors might violate this consistency because of one of these reasons:</span></span>

    -   <span data-ttu-id="f321e-162">硬體處理器具有不具變異的 TSC，BIOS 未正確指出此狀況。</span><span class="sxs-lookup"><span data-stu-id="f321e-162">The hardware processors have a non-invariant TSC and the BIOS doesn't indicate this condition correctly.</span></span>
    -   <span data-ttu-id="f321e-163">使用的 TSC 同步處理演算法不適用於具有大量處理器的系統。</span><span class="sxs-lookup"><span data-stu-id="f321e-163">The TSC synchronization algorithm that was used wasn't suitable for systems with large numbers of processors.</span></span>

-   <span data-ttu-id="f321e-164">當您比較從不同的執行緒取得的效能計數器結果時，請考慮±1刻度的不同值會有不明確的順序。</span><span class="sxs-lookup"><span data-stu-id="f321e-164">When you compare performance counter results that are acquired from different threads, consider values that differ by ± 1 tick to have an ambiguous ordering.</span></span> <span data-ttu-id="f321e-165">如果從相同的執行緒取得時間戳記，則不會套用此±1滴答不確定性。</span><span class="sxs-lookup"><span data-stu-id="f321e-165">If the time stamps are taken from the same thread, this ± 1 tick uncertainty doesn't apply.</span></span> <span data-ttu-id="f321e-166">在此內容中，「期限」一詞是指等於1÷的一段時間， (從 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)) 取得之效能計數器的頻率。</span><span class="sxs-lookup"><span data-stu-id="f321e-166">In this context, the term tick refers to a period of time equal to 1 ÷ (the frequency of the performance counter obtained from [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)).</span></span>

<span data-ttu-id="f321e-167">當您在具有多個時鐘網域的大型伺服器系統上使用效能計數器（這些系統未在硬體中同步處理）時，Windows 會判斷該 TSC 無法用於時間用途，並選取平臺計數器作為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)的基礎。</span><span class="sxs-lookup"><span data-stu-id="f321e-167">When you use the performance counter on large server systems with multiple-clock domains that aren't synchronized in hardware, Windows determines that the TSC can't be used for timing purposes and selects a platform counter as the basis for [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span> <span data-ttu-id="f321e-168">雖然此案例仍會產生可靠的時間戳記，但存取延遲和擴充性會受到負面影響。</span><span class="sxs-lookup"><span data-stu-id="f321e-168">While this scenario still yields reliable time stamps, the access latency and scalability is adversely affected.</span></span> <span data-ttu-id="f321e-169">因此，如先前的使用指導方針所述，只有在需要這類解決方案時，才使用可提供1微秒或更佳解析度的 Api。</span><span class="sxs-lookup"><span data-stu-id="f321e-169">Therefore, as previously stated in the preceding usage guidance, only use the APIs that provide 1 microsecond or better resolution when such resolution is necessary.</span></span> <span data-ttu-id="f321e-170">您可以使用 TSC 作為 **QPC** 在多時鐘網域系統上的基礎，包括所有處理器時鐘網域的硬體同步處理，因為這樣可有效地將它們當做單一時鐘網域系統運作。</span><span class="sxs-lookup"><span data-stu-id="f321e-170">The TSC is used as the basis for **QPC** on multi-clock domain systems that include hardware synchronization of all processor clock domains, as this effectively makes them function as a single clock domain system.</span></span>

<span data-ttu-id="f321e-171">效能計數器的頻率是在系統開機時固定的，且在所有處理器都是一致的，因此您只需要在應用程式初始化時從 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) 查詢頻率，然後快取結果。</span><span class="sxs-lookup"><span data-stu-id="f321e-171">The frequency of the performance counter is fixed at system boot and is consistent across all processors so you only need to query the frequency from [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) as the application initializes, and then cache the result.</span></span>

### <a name="virtualization"></a><span data-ttu-id="f321e-172">虛擬化</span><span class="sxs-lookup"><span data-stu-id="f321e-172">Virtualization</span></span>

<span data-ttu-id="f321e-173">效能計數器預期會可靠地在所有執行的虛擬機器上執行的虛擬機器上運作。</span><span class="sxs-lookup"><span data-stu-id="f321e-173">The performance counter is expected to work reliably on all guest virtual machines running on correctly implemented hypervisors.</span></span> <span data-ttu-id="f321e-174">不過，符合程式管理版本1.0 介面和表面參考時間啟蒙的管理程式，可提供大幅較低的負荷。</span><span class="sxs-lookup"><span data-stu-id="f321e-174">However, hypervisors that comply with the hypervisor version 1.0 interface and surface the reference time enlightenment can offer substantially lower overhead.</span></span> <span data-ttu-id="f321e-175">如需有關管理程式介面和 enlightenments 的詳細資訊，請參閱 [虛擬程式規範](/virtualization/hyper-v-on-windows/reference/tlfs)。</span><span class="sxs-lookup"><span data-stu-id="f321e-175">For more information about hypervisor interfaces and enlightenments, see [Hypervisor Specifications](/virtualization/hyper-v-on-windows/reference/tlfs).</span></span>

### <a name="direct-tsc-usage"></a><span data-ttu-id="f321e-176">直接的 TSC 使用方式</span><span class="sxs-lookup"><span data-stu-id="f321e-176">Direct TSC usage</span></span>

<span data-ttu-id="f321e-177">我們強烈建議使用 **RDTSC** 或 **RDTSCP** 處理器指令來直接查詢 TSC，因為您不會在某些 Windows 版本、跨虛擬機器的即時移轉，以及不具變異或緊密同步 TSCs 的硬體系統上取得可靠的結果。</span><span class="sxs-lookup"><span data-stu-id="f321e-177">We strongly discourage using the **RDTSC** or **RDTSCP** processor instruction to directly query the TSC because you won't get reliable results on some versions of Windows, across live migrations of virtual machines, and on hardware systems without invariant or tightly synchronized TSCs.</span></span> <span data-ttu-id="f321e-178">相反地，我們鼓勵您使用 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 來利用它所提供的抽象概念、一致性和可攜性。</span><span class="sxs-lookup"><span data-stu-id="f321e-178">Instead, we encourage you to use [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) to leverage the abstraction, consistency, and portability that it offers.</span></span>

### <a name="examples-for-acquiring-time-stamps"></a><span data-ttu-id="f321e-179">取得時間戳記的範例</span><span class="sxs-lookup"><span data-stu-id="f321e-179">Examples for acquiring time stamps</span></span>

<span data-ttu-id="f321e-180">這些章節中的各種程式碼範例會示範如何取得時間戳記。</span><span class="sxs-lookup"><span data-stu-id="f321e-180">The various code examples in these sections show how to acquire time stamps.</span></span>

### <a name="using-qpc-in-native-code"></a><span data-ttu-id="f321e-181">在原生程式碼中使用 QPC</span><span class="sxs-lookup"><span data-stu-id="f321e-181">Using QPC in native code</span></span>

<span data-ttu-id="f321e-182">此範例說明如何在 C 和 c + + 機器碼中使用 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 。</span><span class="sxs-lookup"><span data-stu-id="f321e-182">This example shows how to use [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) in C and C++ native code.</span></span>


```C++
LARGE_INTEGER StartingTime, EndingTime, ElapsedMicroseconds;
LARGE_INTEGER Frequency;

QueryPerformanceFrequency(&Frequency); 
QueryPerformanceCounter(&StartingTime);

// Activity to be timed

QueryPerformanceCounter(&EndingTime);
ElapsedMicroseconds.QuadPart = EndingTime.QuadPart - StartingTime.QuadPart;


//
// We now have the elapsed number of ticks, along with the
// number of ticks-per-second. We use these values
// to convert to the number of elapsed microseconds.
// To guard against loss-of-precision, we convert
// to microseconds *before* dividing by ticks-per-second.
//

ElapsedMicroseconds.QuadPart *= 1000000;
ElapsedMicroseconds.QuadPart /= Frequency.QuadPart;
```



### <a name="acquiring-high-resolution-time-stamps-from-managed-code"></a><span data-ttu-id="f321e-183">從受控碼取得高解析度的時間戳記</span><span class="sxs-lookup"><span data-stu-id="f321e-183">Acquiring high resolution time stamps from managed code</span></span>

<span data-ttu-id="f321e-184">此範例示範如何使用 managed [**程式碼 system.object**](/previous-versions/windows/) 。</span><span class="sxs-lookup"><span data-stu-id="f321e-184">This example shows how to use the managed code [**System.Diagnostics.Stopwatch**](/previous-versions/windows/) class.</span></span>


```CSharp
using System.Diagnostics;

long StartingTime = Stopwatch.GetTimestamp();

// Activity to be timed

long EndingTime  = Stopwatch.GetTimestamp();
long ElapsedTime = EndingTime - StartingTime;

double ElapsedSeconds = ElapsedTime * (1.0 / Stopwatch.Frequency);
```



<span data-ttu-id="f321e-185">System.servicemodel [**類別也**](/previous-versions/windows/) 提供數個方便的方法來執行時間間隔測量。</span><span class="sxs-lookup"><span data-stu-id="f321e-185">The [**System.Diagnostics.Stopwatch**](/previous-versions/windows/) class also provides several convenient methods to perform time-interval measurements.</span></span>

### <a name="using-qpc-from-kernel-mode"></a><span data-ttu-id="f321e-186">使用核心模式的 QPC</span><span class="sxs-lookup"><span data-stu-id="f321e-186">Using QPC from kernel mode</span></span>

<span data-ttu-id="f321e-187">Windows 核心透過 [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) （可從中取得效能計數器和效能頻率）提供效能計數器的核心模式存取。</span><span class="sxs-lookup"><span data-stu-id="f321e-187">The Windows kernel provides kernel-mode access to the performance counter through [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) from which both the performance counter and performance frequency can be obtained.</span></span> <span data-ttu-id="f321e-188">**KeQueryPerformanceCounter** 僅適用于核心模式，並提供給設備磁碟機和其他核心模式元件的寫入器。</span><span class="sxs-lookup"><span data-stu-id="f321e-188">**KeQueryPerformanceCounter** is available from kernel mode only and is provided for writers of device drivers and other kernel-mode components.</span></span>

<span data-ttu-id="f321e-189">此範例說明如何在 C 和 c + + 核心模式中使用 [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) 。</span><span class="sxs-lookup"><span data-stu-id="f321e-189">This example shows how to use [**KeQueryPerformanceCounter**](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-kequeryperformancecounter) in C and C++ kernel mode.</span></span>


```C++
LARGE_INTEGER StartingTime, EndingTime, ElapsedMicroseconds;
LARGE_INTEGER Frequency;

StartingTime = KeQueryPerformanceCounter(&Frequency);

// Activity to be timed

EndingTime = KeQueryPerformanceCounter(NULL);
ElapsedMicroseconds.QuadPart = EndingTime.QuadPart - StartingTime.QuadPart;
ElapsedMicroseconds.QuadPart *= 1000000;
ElapsedMicroseconds.QuadPart /= Frequency.QuadPart;
```



## <a name="general-faq-about-qpc-and-tsc"></a><span data-ttu-id="f321e-190">關於 QPC 和 TSC 的一般常見問題</span><span class="sxs-lookup"><span data-stu-id="f321e-190">General FAQ about QPC and TSC</span></span>

<span data-ttu-id="f321e-191">以下是一般 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 和 TSCs 常見問題的解答。</span><span class="sxs-lookup"><span data-stu-id="f321e-191">Here are answers to frequently-asked questions about [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) and TSCs in general.</span></span>

<dl> <dt>

<span data-ttu-id="f321e-192"><span id="Is_QueryPerformanceCounter___the_same_as_the_Win32_GetTickCount___or_________GetTickCount64___function_"></span><span id="is_queryperformancecounter___the_same_as_the_win32_gettickcount___or_________gettickcount64___function_"></span><span id="IS_QUERYPERFORMANCECOUNTER___THE_SAME_AS_THE_WIN32_GETTICKCOUNT___OR_________GETTICKCOUNT64___FUNCTION_"></span>**QueryPerformanceCounter () 與 Win32 GetTickCount () 或 GetTickCount64 () 函數相同嗎？**</span><span class="sxs-lookup"><span data-stu-id="f321e-192"><span id="Is_QueryPerformanceCounter___the_same_as_the_Win32_GetTickCount___or_________GetTickCount64___function_"></span><span id="is_queryperformancecounter___the_same_as_the_win32_gettickcount___or_________gettickcount64___function_"></span><span id="IS_QUERYPERFORMANCECOUNTER___THE_SAME_AS_THE_WIN32_GETTICKCOUNT___OR_________GETTICKCOUNT64___FUNCTION_"></span>**Is QueryPerformanceCounter() the same as the Win32 GetTickCount() or GetTickCount64() function?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-193">不會。</span><span class="sxs-lookup"><span data-stu-id="f321e-193">No.</span></span> <span data-ttu-id="f321e-194">[**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) 和 [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) 與 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)無關。</span><span class="sxs-lookup"><span data-stu-id="f321e-194">[**GetTickCount**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) and [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) aren't related to [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span> <span data-ttu-id="f321e-195">**GetTickCount** 和 **GetTickCount64** 會傳回系統啟動之後的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="f321e-195">**GetTickCount** and **GetTickCount64** return the number of milliseconds since the system was started.</span></span>

</dd> <dt>

<span data-ttu-id="f321e-196"><span id="Should_I_use_QPC_or_call_the_RDTSC__RDTSCP_instructions_directly_"></span><span id="should_i_use_qpc_or_call_the_rdtsc__rdtscp_instructions_directly_"></span><span id="SHOULD_I_USE_QPC_OR_CALL_THE_RDTSC__RDTSCP_INSTRUCTIONS_DIRECTLY_"></span>**我應該使用 QPC 或直接呼叫 RDTSC/RDTSCP 指示嗎？**</span><span class="sxs-lookup"><span data-stu-id="f321e-196"><span id="Should_I_use_QPC_or_call_the_RDTSC__RDTSCP_instructions_directly_"></span><span id="should_i_use_qpc_or_call_the_rdtsc__rdtscp_instructions_directly_"></span><span id="SHOULD_I_USE_QPC_OR_CALL_THE_RDTSC__RDTSCP_INSTRUCTIONS_DIRECTLY_"></span>**Should I use QPC or call the RDTSC /RDTSCP instructions directly?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-197">為了避免 incorrectness 和可攜性問題，我們強烈建議您使用 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) ，而不是使用 TSC 登錄或 **RDTSC** 或 **RDTSCP** 處理器指示。</span><span class="sxs-lookup"><span data-stu-id="f321e-197">To avoid incorrectness and portability issues, we strongly encourage you to use [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) instead of using the TSC register or the **RDTSC** or **RDTSCP** processor instructions.</span></span>

</dd> <dt>

<span data-ttu-id="f321e-198"><span id="What_is_QPC_s_relation_to_an_external_time_epoch__Can_it_be_synchronized_to_an_________external_epoch_such_as_UTC_"></span><span id="what_is_qpc_s_relation_to_an_external_time_epoch__can_it_be_synchronized_to_an_________external_epoch_such_as_utc_"></span><span id="WHAT_IS_QPC_S_RELATION_TO_AN_EXTERNAL_TIME_EPOCH__CAN_IT_BE_SYNCHRONIZED_TO_AN_________EXTERNAL_EPOCH_SUCH_AS_UTC_"></span>**QPC 與外部時間 epoch 有何關聯？它是否可以同步處理至外部 epoch （例如 UTC）？**</span><span class="sxs-lookup"><span data-stu-id="f321e-198"><span id="What_is_QPC_s_relation_to_an_external_time_epoch__Can_it_be_synchronized_to_an_________external_epoch_such_as_UTC_"></span><span id="what_is_qpc_s_relation_to_an_external_time_epoch__can_it_be_synchronized_to_an_________external_epoch_such_as_utc_"></span><span id="WHAT_IS_QPC_S_RELATION_TO_AN_EXTERNAL_TIME_EPOCH__CAN_IT_BE_SYNCHRONIZED_TO_AN_________EXTERNAL_EPOCH_SUCH_AS_UTC_"></span>**What is QPC’s relation to an external time epoch? Can it be synchronized to an external epoch such as UTC?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-199">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 是以無法同步處理至外部時間參考的硬體計數器為基礎，例如 UTC。</span><span class="sxs-lookup"><span data-stu-id="f321e-199">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) is based on a hardware counter that can't be synchronized to an external time reference, such as UTC.</span></span> <span data-ttu-id="f321e-200">如需可同步處理至外部 UTC 參考的精確日期時間戳記，請使用 [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime)。</span><span class="sxs-lookup"><span data-stu-id="f321e-200">For precise time-of-day time stamps that can be synchronized to an external UTC reference, use [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).</span></span>

</dd> <dt>

<span data-ttu-id="f321e-201"><span id="Is_QPC_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="is_qpc_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="IS_QPC_AFFECTED_BY_DAYLIGHT_SAVINGS_TIME__LEAP_SECONDS__TIME_ZONES__OR_SYSTEM_________TIME_CHANGES_MADE_BY_THE_ADMINISTRATOR_"></span>**QPC 是否受日光節約時間、閏秒、時區或系統管理員所做的系統時間變更所影響？**</span><span class="sxs-lookup"><span data-stu-id="f321e-201"><span id="Is_QPC_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="is_qpc_affected_by_daylight_savings_time__leap_seconds__time_zones__or_system_________time_changes_made_by_the_administrator_"></span><span id="IS_QPC_AFFECTED_BY_DAYLIGHT_SAVINGS_TIME__LEAP_SECONDS__TIME_ZONES__OR_SYSTEM_________TIME_CHANGES_MADE_BY_THE_ADMINISTRATOR_"></span>**Is QPC affected by daylight savings time, leap seconds, time zones, or system time changes made by the administrator?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-202">不會。</span><span class="sxs-lookup"><span data-stu-id="f321e-202">No.</span></span> <span data-ttu-id="f321e-203">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 與系統時間和 UTC 完全無關。</span><span class="sxs-lookup"><span data-stu-id="f321e-203">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) is completely independent of the system time and UTC.</span></span>

</dd> <dt>

<span data-ttu-id="f321e-204"><span id="Is_QPC_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_Turbo_Boost_technology_"></span><span id="is_qpc_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_turbo_boost_technology_"></span><span id="IS_QPC_ACCURACY_AFFECTED_BY_PROCESSOR_FREQUENCY_CHANGES_CAUSED_BY_POWER_________MANAGEMENT_OR_TURBO_BOOST_TECHNOLOGY_"></span>**QPC 的精確度是否受到電源管理或 Turbo 加速技術所造成的處理器頻率變更所影響？**</span><span class="sxs-lookup"><span data-stu-id="f321e-204"><span id="Is_QPC_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_Turbo_Boost_technology_"></span><span id="is_qpc_accuracy_affected_by_processor_frequency_changes_caused_by_power_________management_or_turbo_boost_technology_"></span><span id="IS_QPC_ACCURACY_AFFECTED_BY_PROCESSOR_FREQUENCY_CHANGES_CAUSED_BY_POWER_________MANAGEMENT_OR_TURBO_BOOST_TECHNOLOGY_"></span>**Is QPC accuracy affected by processor frequency changes caused by power management or Turbo Boost technology?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-205">不會。</span><span class="sxs-lookup"><span data-stu-id="f321e-205">No.</span></span> <span data-ttu-id="f321e-206">如果處理器具有不變的 TSC，則 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 不會受到這類變更的影響。</span><span class="sxs-lookup"><span data-stu-id="f321e-206">If the processor has an invariant TSC, the [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) is not affected by these sort of changes.</span></span> <span data-ttu-id="f321e-207">如果處理器沒有不具變異的 TSC， **QPC** 會還原為平臺硬體計時器，而不會受到處理器頻率變更或 Turbo 加速技術的影響。</span><span class="sxs-lookup"><span data-stu-id="f321e-207">If the processor doesn't have an invariant TSC, **QPC** will revert to a platform hardware timer that won't be affected by processor frequency changes or Turbo Boost technology.</span></span>

</dd> <dt>

<span data-ttu-id="f321e-208"><span id="Does_QPC_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="does_qpc_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="DOES_QPC_RELIABLY_WORK_ON_MULTI-PROCESSOR_SYSTEMS__MULTI-CORE_SYSTEM__AND_________SYSTEMS_WITH_HYPER-THREADING_"></span>**QPC 是否可在多處理器系統、多重核心系統以及具有超執行緒的系統上可靠地運作？**</span><span class="sxs-lookup"><span data-stu-id="f321e-208"><span id="Does_QPC_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="does_qpc_reliably_work_on_multi-processor_systems__multi-core_system__and_________systems_with_hyper-threading_"></span><span id="DOES_QPC_RELIABLY_WORK_ON_MULTI-PROCESSOR_SYSTEMS__MULTI-CORE_SYSTEM__AND_________SYSTEMS_WITH_HYPER-THREADING_"></span>**Does QPC reliably work on multi-processor systems, multi-core system, and systems with hyper-threading?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-209">Yes</span><span class="sxs-lookup"><span data-stu-id="f321e-209">Yes</span></span>

</dd> <dt>

<span data-ttu-id="f321e-210"><span id="How_do_I_determine_and_validate_that_QPC_works_on_my_machine_"></span><span id="how_do_i_determine_and_validate_that_qpc_works_on_my_machine_"></span><span id="HOW_DO_I_DETERMINE_AND_VALIDATE_THAT_QPC_WORKS_ON_MY_MACHINE_"></span>**如何? 判斷並驗證 QPC 是否可在我的電腦上運作？**</span><span class="sxs-lookup"><span data-stu-id="f321e-210"><span id="How_do_I_determine_and_validate_that_QPC_works_on_my_machine_"></span><span id="how_do_i_determine_and_validate_that_qpc_works_on_my_machine_"></span><span id="HOW_DO_I_DETERMINE_AND_VALIDATE_THAT_QPC_WORKS_ON_MY_MACHINE_"></span>**How do I determine and validate that QPC works on my machine?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-211">您不需要執行這類檢查。</span><span class="sxs-lookup"><span data-stu-id="f321e-211">You don't need to perform such checks.</span></span>

</dd> <dt>

<span data-ttu-id="f321e-212"><span id="Which_processors_have_non-invariant_TSCs__How_can_I_check_if_my_system_has_a_________non-invariant_TSC_"></span><span id="which_processors_have_non-invariant_tscs__how_can_i_check_if_my_system_has_a_________non-invariant_tsc_"></span><span id="WHICH_PROCESSORS_HAVE_NON-INVARIANT_TSCS__HOW_CAN_I_CHECK_IF_MY_SYSTEM_HAS_A_________NON-INVARIANT_TSC_"></span>**哪些處理器有非變異 TSCs？如何檢查我的系統是否有不具變異的 TSC？**</span><span class="sxs-lookup"><span data-stu-id="f321e-212"><span id="Which_processors_have_non-invariant_TSCs__How_can_I_check_if_my_system_has_a_________non-invariant_TSC_"></span><span id="which_processors_have_non-invariant_tscs__how_can_i_check_if_my_system_has_a_________non-invariant_tsc_"></span><span id="WHICH_PROCESSORS_HAVE_NON-INVARIANT_TSCS__HOW_CAN_I_CHECK_IF_MY_SYSTEM_HAS_A_________NON-INVARIANT_TSC_"></span>**Which processors have non-invariant TSCs? How can I check if my system has a non-invariant TSC?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-213">您不需要自行執行這一檢查。</span><span class="sxs-lookup"><span data-stu-id="f321e-213">You don't need to perform this check yourself.</span></span> <span data-ttu-id="f321e-214">Windows 作業系統會在系統初始化期間執行數個檢查，以判斷 TSC 是否適合做為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)的基礎。</span><span class="sxs-lookup"><span data-stu-id="f321e-214">Windows operating systems perform several checks at system initialization to determine if the TSC is suitable as a basis for [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span> <span data-ttu-id="f321e-215">不過，基於參考目的，您可以使用下列其中一種方式，判斷您的處理器是否具有不變的 TSC：</span><span class="sxs-lookup"><span data-stu-id="f321e-215">However, for reference purposes, you can determine whether your processor has an invariant TSC by using one of these:</span></span>

-   <span data-ttu-id="f321e-216">Windows Sysinternals 的 Coreinfo.exe 公用程式</span><span class="sxs-lookup"><span data-stu-id="f321e-216">the Coreinfo.exe utility from Windows Sysinternals</span></span>
-   <span data-ttu-id="f321e-217">檢查與 TSC 特性相關的 CPUID 指令所傳回的值</span><span class="sxs-lookup"><span data-stu-id="f321e-217">checking the values returned by the CPUID instruction pertaining to the TSC characteristics</span></span>
-   <span data-ttu-id="f321e-218">處理器製造商的檔</span><span class="sxs-lookup"><span data-stu-id="f321e-218">the processor manufacturer’s documentation</span></span>

<span data-ttu-id="f321e-219">以下顯示 Windows Sysinternals Coreinfo.exe 公用程式 ([www.sysinternals.com](https://www.sysinternals.com)) 所提供的 TSC 非變異資訊。</span><span class="sxs-lookup"><span data-stu-id="f321e-219">The following shows the TSC-INVARIANT info that is provided by the Windows Sysinternals Coreinfo.exe utility ([www.sysinternals.com](https://www.sysinternals.com)).</span></span> <span data-ttu-id="f321e-220">星號表示 "True"。</span><span class="sxs-lookup"><span data-stu-id="f321e-220">An asterisk means "True".</span></span>

``` syntax
> Coreinfo.exe 

Coreinfo v3.2 - Dump information on system CPU and memory topology
Copyright (C) 2008-2012 Mark Russinovich
Sysinternals - www.sysinternals.com

 <unrelated text removed>

RDTSCP          * Supports RDTSCP instruction
TSC             * Supports RDTSC instruction
TSC-DEADLINE    - Local APIC supports one-shot deadline timer
TSC-INVARIANT   * TSC runs at constant rate
```

</dd> <dt>

<span data-ttu-id="f321e-221"><span id="Does_QPC_work_reliably_on__hardware_platforms_"></span><span id="does_qpc_work_reliably_on__hardware_platforms_"></span><span id="DOES_QPC_WORK_RELIABLY_ON__HARDWARE_PLATFORMS_"></span>**QPC 是否能在 Windows RT PC 硬體平臺上可靠地工作？**</span><span class="sxs-lookup"><span data-stu-id="f321e-221"><span id="Does_QPC_work_reliably_on__hardware_platforms_"></span><span id="does_qpc_work_reliably_on__hardware_platforms_"></span><span id="DOES_QPC_WORK_RELIABLY_ON__HARDWARE_PLATFORMS_"></span>**Does QPC work reliably on Windows RT PC hardware platforms?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-222">Yes</span><span class="sxs-lookup"><span data-stu-id="f321e-222">Yes</span></span>

</dd> <dt>

<span data-ttu-id="f321e-223"><span id="How_often_does_QPC_roll_over_"></span><span id="how_often_does_qpc_roll_over_"></span><span id="HOW_OFTEN_DOES_QPC_ROLL_OVER_"></span>**QPC 變換的頻率為何？**</span><span class="sxs-lookup"><span data-stu-id="f321e-223"><span id="How_often_does_QPC_roll_over_"></span><span id="how_often_does_qpc_roll_over_"></span><span id="HOW_OFTEN_DOES_QPC_ROLL_OVER_"></span>**How often does QPC roll over?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-224">從最近的系統開機不到100年，而且可能會根據使用的基礎硬體計時器而更久。</span><span class="sxs-lookup"><span data-stu-id="f321e-224">Not less than 100 years from the most recent system boot, and potentially longer based on the underlying hardware timer used.</span></span> <span data-ttu-id="f321e-225">在大部分的應用程式中，變換並不重要。</span><span class="sxs-lookup"><span data-stu-id="f321e-225">For most applications, rollover isn't a concern.</span></span>

</dd> <dt>

<span data-ttu-id="f321e-226"><span id="What_is_the_computational_cost_of_calling_QPC_"></span><span id="what_is_the_computational_cost_of_calling_qpc_"></span><span id="WHAT_IS_THE_COMPUTATIONAL_COST_OF_CALLING_QPC_"></span>**呼叫 QPC 的計算成本為何？**</span><span class="sxs-lookup"><span data-stu-id="f321e-226"><span id="What_is_the_computational_cost_of_calling_QPC_"></span><span id="what_is_the_computational_cost_of_calling_qpc_"></span><span id="WHAT_IS_THE_COMPUTATIONAL_COST_OF_CALLING_QPC_"></span>**What is the computational cost of calling QPC?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-227">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)的計算呼叫成本主要是由基礎硬體平臺所決定。</span><span class="sxs-lookup"><span data-stu-id="f321e-227">The computational calling cost of [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) is determined primarily by the underlying hardware platform.</span></span> <span data-ttu-id="f321e-228">如果使用 TSC 註冊作為 QPC 的基礎，則計算成本主要取決於處理器處理 **RDTSC** 指令所需的時間長度。</span><span class="sxs-lookup"><span data-stu-id="f321e-228">If the TSC register is used as the basis for QPC, the computational cost is determined primarily by how long the processor takes to process an **RDTSC** instruction.</span></span> <span data-ttu-id="f321e-229">這段時間的範圍是從 CPU 迴圈10s 到數百個 CPU 迴圈，視所使用的處理器而定。</span><span class="sxs-lookup"><span data-stu-id="f321e-229">This time ranges from 10s of CPU cycles to several hundred CPU cycles depending upon the processor used.</span></span> <span data-ttu-id="f321e-230">如果無法使用 TSC，系統將會選取不同的硬體時間。</span><span class="sxs-lookup"><span data-stu-id="f321e-230">If the TSC can't be used, the system will select a different hardware time basis.</span></span> <span data-ttu-id="f321e-231">因為這些時間基底位於主機板上 (例如，在 PCI 南橋接器或 PCH) 上，個別呼叫計算成本高於 TSC，而且通常會在 0.8-1.0 毫秒的鄰近範圍中，視處理器速度和其他硬體因素而定。</span><span class="sxs-lookup"><span data-stu-id="f321e-231">Because these time bases are located on the motherboard (for example, on the PCI South Bridge or PCH), the per-call computational cost is higher than the TSC, and is frequently in the vicinity of 0.8 - 1.0 microseconds depending on processor speed and other hardware factors.</span></span> <span data-ttu-id="f321e-232">這項成本的依據是存取主機板上的硬體裝置所需的時間。</span><span class="sxs-lookup"><span data-stu-id="f321e-232">This cost is dominated by the time required to access the hardware device on the motherboard.</span></span>

</dd> <dt>

<span data-ttu-id="f321e-233"><span id="Does_QPC_require_a_kernel_transition__system_call__"></span><span id="does_qpc_require_a_kernel_transition__system_call__"></span><span id="DOES_QPC_REQUIRE_A_KERNEL_TRANSITION__SYSTEM_CALL__"></span>**QPC 是否需要 (系統呼叫) 的核心轉換？**</span><span class="sxs-lookup"><span data-stu-id="f321e-233"><span id="Does_QPC_require_a_kernel_transition__system_call__"></span><span id="does_qpc_require_a_kernel_transition__system_call__"></span><span id="DOES_QPC_REQUIRE_A_KERNEL_TRANSITION__SYSTEM_CALL__"></span>**Does QPC require a kernel transition (system call)?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-234">如果系統可以使用 TSC 註冊作為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)的基礎，則不需要進行核心轉換。</span><span class="sxs-lookup"><span data-stu-id="f321e-234">A kernel transition is not required if the system can use the TSC register as the basis for [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span> <span data-ttu-id="f321e-235">如果系統必須使用不同的時間基底（例如 HPET 或 PM 計時器），則需要系統呼叫。</span><span class="sxs-lookup"><span data-stu-id="f321e-235">If the system must use a different time base, such as the HPET or PM timer, a system call is required.</span></span>

</dd> <dt>

<span data-ttu-id="f321e-236"><span id="Is_the_performance_counter_monotonic__non-decreasing__"></span><span id="is_the_performance_counter_monotonic__non-decreasing__"></span><span id="IS_THE_PERFORMANCE_COUNTER_MONOTONIC__NON-DECREASING__"></span>**效能計數器單純 (非遞減) ？**</span><span class="sxs-lookup"><span data-stu-id="f321e-236"><span id="Is_the_performance_counter_monotonic__non-decreasing__"></span><span id="is_the_performance_counter_monotonic__non-decreasing__"></span><span id="IS_THE_PERFORMANCE_COUNTER_MONOTONIC__NON-DECREASING__"></span>**Is the performance counter monotonic (non-decreasing)?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-237">Yes</span><span class="sxs-lookup"><span data-stu-id="f321e-237">Yes</span></span>

</dd> <dt>

<span data-ttu-id="f321e-238"><span id="Can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="CAN_THE_PERFORMANCE_COUNTER_BE_USED_TO_ORDER_EVENTS_IN_TIME_"></span>**效能計數器可以用來排序時間內的事件嗎？**</span><span class="sxs-lookup"><span data-stu-id="f321e-238"><span id="Can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="can_the_performance_counter_be_used_to_order_events_in_time_"></span><span id="CAN_THE_PERFORMANCE_COUNTER_BE_USED_TO_ORDER_EVENTS_IN_TIME_"></span>**Can the performance counter be used to order events in time?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-239">是。</span><span class="sxs-lookup"><span data-stu-id="f321e-239">Yes.</span></span> <span data-ttu-id="f321e-240">不過，在比較從不同執行緒取得的效能計數器結果時，依±1刻度差異的值會有不明確的順序，如同它們具有相同的時間戳記一樣。</span><span class="sxs-lookup"><span data-stu-id="f321e-240">However, when comparing performance counter results that are acquired from different threads, values that differ by ± 1 tick have an ambiguous ordering as if they had an identical time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="f321e-241"><span id="How_accurate_is_the_performance_counter_"></span><span id="how_accurate_is_the_performance_counter_"></span><span id="HOW_ACCURATE_IS_THE_PERFORMANCE_COUNTER_"></span>**效能計數器的精確度為何？**</span><span class="sxs-lookup"><span data-stu-id="f321e-241"><span id="How_accurate_is_the_performance_counter_"></span><span id="how_accurate_is_the_performance_counter_"></span><span id="HOW_ACCURATE_IS_THE_PERFORMANCE_COUNTER_"></span>**How accurate is the performance counter?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-242">答案取決於各種不同的因素。</span><span class="sxs-lookup"><span data-stu-id="f321e-242">The answer depends on a variety of factors.</span></span> <span data-ttu-id="f321e-243">如需詳細資訊，請參閱 [低層級硬體時鐘特性](#low-level-hardware-clock-characteristics)。</span><span class="sxs-lookup"><span data-stu-id="f321e-243">For more info, see [Low-level hardware clock characteristics](#low-level-hardware-clock-characteristics).</span></span>

</dd> </dl>

## <a name="faq-about-programming-with-qpc-and-tsc"></a><span data-ttu-id="f321e-244">使用 QPC 和 TSC 進行程式設計的常見問題</span><span class="sxs-lookup"><span data-stu-id="f321e-244">FAQ about programming with QPC and TSC</span></span>

<span data-ttu-id="f321e-245">以下是使用 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 和 TSCs 進行程式設計的常見問題的解答。</span><span class="sxs-lookup"><span data-stu-id="f321e-245">Here are answers to frequently-asked questions about programming with [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) and TSCs.</span></span>

<dl> <dt>

<span data-ttu-id="f321e-246"><span id="I_need_to_convert_the_QPC_output_to_milliseconds._How_can_I_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="i_need_to_convert_the_qpc_output_to_milliseconds._how_can_i_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="I_NEED_TO_CONVERT_THE_QPC_OUTPUT_TO_MILLISECONDS._HOW_CAN_I_AVOID_LOSS_OF_________PRECISION_WITH_CONVERTING_TO_DOUBLE_OR_FLOAT_"></span>**我需要將 QPC 輸出轉換成毫秒。如何避免因為轉換成 double 或 float 而失去精確度？**</span><span class="sxs-lookup"><span data-stu-id="f321e-246"><span id="I_need_to_convert_the_QPC_output_to_milliseconds._How_can_I_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="i_need_to_convert_the_qpc_output_to_milliseconds._how_can_i_avoid_loss_of_________precision_with_converting_to_double_or_float_"></span><span id="I_NEED_TO_CONVERT_THE_QPC_OUTPUT_TO_MILLISECONDS._HOW_CAN_I_AVOID_LOSS_OF_________PRECISION_WITH_CONVERTING_TO_DOUBLE_OR_FLOAT_"></span>**I need to convert the QPC output to milliseconds. How can I avoid loss of precision with converting to double or float?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-247">在整數效能計數器上執行計算時，有幾件事要牢記在心：</span><span class="sxs-lookup"><span data-stu-id="f321e-247">There are several things to keep in mind when performing calculations on integer performance counters:</span></span>

-   <span data-ttu-id="f321e-248">整數除法將會遺失餘數。</span><span class="sxs-lookup"><span data-stu-id="f321e-248">Integer division will lose the remainder.</span></span> <span data-ttu-id="f321e-249">這可能會導致在某些情況下遺失精確度。</span><span class="sxs-lookup"><span data-stu-id="f321e-249">This can cause loss of precision in some cases.</span></span>
-   <span data-ttu-id="f321e-250">64位整數和浮點數之間的轉換 (double) 可能會導致精確度遺失，因為浮點數尾數無法表示所有可能的整數值。</span><span class="sxs-lookup"><span data-stu-id="f321e-250">Conversion between 64 bit integers and floating point (double) can cause loss of precision because the floating point mantissa can't represent all possible integral values.</span></span>
-   <span data-ttu-id="f321e-251">64位整數的乘法會導致整數溢位。</span><span class="sxs-lookup"><span data-stu-id="f321e-251">Multiplication of 64 bit integers can result in integer overflow.</span></span>

<span data-ttu-id="f321e-252">一般來說，請盡可能延遲這些計算和轉換，以避免複合所引進的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f321e-252">As a general principle, delay these computations and conversions as long as possible to avoid compounding the errors introduced.</span></span>

</dd> <dt>

<span data-ttu-id="f321e-253"><span id="How_can_I_convert_QPC_to_100_nanosecond_ticks_so_I_can_add_it_to_a_________FILETIME_"></span><span id="how_can_i_convert_qpc_to_100_nanosecond_ticks_so_i_can_add_it_to_a_________filetime_"></span><span id="HOW_CAN_I_CONVERT_QPC_TO_100_NANOSECOND_TICKS_SO_I_CAN_ADD_IT_TO_A_________FILETIME_"></span>**如何將 QPC 轉換為100毫微秒的刻度，以便將它新增至 FILETIME？**</span><span class="sxs-lookup"><span data-stu-id="f321e-253"><span id="How_can_I_convert_QPC_to_100_nanosecond_ticks_so_I_can_add_it_to_a_________FILETIME_"></span><span id="how_can_i_convert_qpc_to_100_nanosecond_ticks_so_i_can_add_it_to_a_________filetime_"></span><span id="HOW_CAN_I_CONVERT_QPC_TO_100_NANOSECOND_TICKS_SO_I_CAN_ADD_IT_TO_A_________FILETIME_"></span>**How can I convert QPC to 100 nanosecond ticks so I can add it to a FILETIME?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-254">檔案時間是64位的值，代表自上午12:00 以來經過的 100-毫微秒間隔數。</span><span class="sxs-lookup"><span data-stu-id="f321e-254">A file time is a 64-bit value that represents the number of 100-nanosecond intervals that have elapsed since 12:00 A.M.</span></span> <span data-ttu-id="f321e-255">1601年1月1日國際標準時間 (UTC) 。</span><span class="sxs-lookup"><span data-stu-id="f321e-255">January 1, 1601 Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="f321e-256">傳回當日時間的 WIN32 API 呼叫（例如 [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) 和 [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime)）會使用檔案時間。</span><span class="sxs-lookup"><span data-stu-id="f321e-256">File times are used by Win32 API calls that return time-of-day, such as [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) and [**GetSystemTimePreciseAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime).</span></span> <span data-ttu-id="f321e-257">相反地， [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 會傳回代表時間的值，單位為 1/ (從 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)) 取得之效能計數器的頻率。</span><span class="sxs-lookup"><span data-stu-id="f321e-257">By contrast, [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) returns values that represent time in units of 1/(the frequency of the performance counter obtained from [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)).</span></span> <span data-ttu-id="f321e-258">兩者之間的轉換需要計算 **QPC** 間隔和 100-毫微秒間隔的比率。</span><span class="sxs-lookup"><span data-stu-id="f321e-258">Conversion between the two requires calculating the ratio of the **QPC** interval and 100-nanoseconds intervals.</span></span> <span data-ttu-id="f321e-259">請小心避免遺失精確度，因為這些值可能很小 (0.0000001/0.000000340) 。</span><span class="sxs-lookup"><span data-stu-id="f321e-259">Be careful to avoid losing precision because the values might be small (0.0000001 / 0.000000340).</span></span>

</dd> <dt>

<span data-ttu-id="f321e-260"><span id="Why_is_the_time_stamp_that_is_returned_from_QPC_a_signed_integer_"></span><span id="why_is_the_time_stamp_that_is_returned_from_qpc_a_signed_integer_"></span><span id="WHY_IS_THE_TIME_STAMP_THAT_IS_RETURNED_FROM_QPC_A_SIGNED_INTEGER_"></span>**為什麼從 QPC 帶正負號的整數傳回的時間戳記？**</span><span class="sxs-lookup"><span data-stu-id="f321e-260"><span id="Why_is_the_time_stamp_that_is_returned_from_QPC_a_signed_integer_"></span><span id="why_is_the_time_stamp_that_is_returned_from_qpc_a_signed_integer_"></span><span id="WHY_IS_THE_TIME_STAMP_THAT_IS_RETURNED_FROM_QPC_A_SIGNED_INTEGER_"></span>**Why is the time stamp that is returned from QPC a signed integer?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-261">涉及 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 時間戳記的計算可能牽涉到減法。</span><span class="sxs-lookup"><span data-stu-id="f321e-261">Calculations that involve [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) time stamps might involve subtraction.</span></span> <span data-ttu-id="f321e-262">藉由使用帶正負號的值，您可以處理可能產生負數值的計算。</span><span class="sxs-lookup"><span data-stu-id="f321e-262">By using a signed value, you can handle calculations that might yield negative values.</span></span>

</dd> <dt>

<span data-ttu-id="f321e-263"><span id="How_can_I_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="how_can_i_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="HOW_CAN_I_OBTAIN_HIGH_RESOLUTION_TIME_STAMPS_FROM_MANAGED_CODE_"></span>**如何從受控碼取得高解析度的時間戳記？**</span><span class="sxs-lookup"><span data-stu-id="f321e-263"><span id="How_can_I_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="how_can_i_obtain_high_resolution_time_stamps_from_managed_code_"></span><span id="HOW_CAN_I_OBTAIN_HIGH_RESOLUTION_TIME_STAMPS_FROM_MANAGED_CODE_"></span>**How can I obtain high resolution time stamps from managed code?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-264">從 [**GetTimeStamp**](/previous-versions/windows/) 方法中，呼叫 [**system.object**](/previous-versions/windows/) 。</span><span class="sxs-lookup"><span data-stu-id="f321e-264">Call the [**Stopwatch.GetTimeStamp**](/previous-versions/windows/) method from the [**System.Diagnostics.Stopwatch**](/previous-versions/windows/) class.</span></span> <span data-ttu-id="f321e-265">如需如何使用 **GetTimeStamp** 的範例，請參閱 [從 managed 程式碼取得高解析度的時間戳記](#acquiring-high-resolution-time-stamps-from-managed-code)。</span><span class="sxs-lookup"><span data-stu-id="f321e-265">For an example about how to use **Stopwatch.GetTimeStamp**, see [Acquiring high resolution time stamps from managed code](#acquiring-high-resolution-time-stamps-from-managed-code).</span></span>

</dd> <dt>

<span data-ttu-id="f321e-266"><span id="Under_what_circumstances_does_QueryPerformanceFrequency_return_FALSE__or_________QueryPerformanceCounter_return_zero_"></span><span id="under_what_circumstances_does_queryperformancefrequency_return_false__or_________queryperformancecounter_return_zero_"></span><span id="UNDER_WHAT_CIRCUMSTANCES_DOES_QUERYPERFORMANCEFREQUENCY_RETURN_FALSE__OR_________QUERYPERFORMANCECOUNTER_RETURN_ZERO_"></span>**在何種情況下，QueryPerformanceFrequency 會傳回 FALSE，或 QueryPerformanceCounter 會傳回零？**</span><span class="sxs-lookup"><span data-stu-id="f321e-266"><span id="Under_what_circumstances_does_QueryPerformanceFrequency_return_FALSE__or_________QueryPerformanceCounter_return_zero_"></span><span id="under_what_circumstances_does_queryperformancefrequency_return_false__or_________queryperformancecounter_return_zero_"></span><span id="UNDER_WHAT_CIRCUMSTANCES_DOES_QUERYPERFORMANCEFREQUENCY_RETURN_FALSE__OR_________QUERYPERFORMANCECOUNTER_RETURN_ZERO_"></span>**Under what circumstances does QueryPerformanceFrequency return FALSE, or QueryPerformanceCounter return zero?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-267">這不會發生在任何執行 Windows XP 或更新版本的系統上。</span><span class="sxs-lookup"><span data-stu-id="f321e-267">This won't occur on any system that runs Windows XP or later.</span></span>

</dd> <dt>

<span data-ttu-id="f321e-268"><span id="Do_I_need_to_set_the_thread_affinity_to_a_single_core_to_use_QPC_"></span><span id="do_i_need_to_set_the_thread_affinity_to_a_single_core_to_use_qpc_"></span><span id="DO_I_NEED_TO_SET_THE_THREAD_AFFINITY_TO_A_SINGLE_CORE_TO_USE_QPC_"></span>**我是否需要將執行緒親和性設定為單一核心，才能使用 QPC？**</span><span class="sxs-lookup"><span data-stu-id="f321e-268"><span id="Do_I_need_to_set_the_thread_affinity_to_a_single_core_to_use_QPC_"></span><span id="do_i_need_to_set_the_thread_affinity_to_a_single_core_to_use_qpc_"></span><span id="DO_I_NEED_TO_SET_THE_THREAD_AFFINITY_TO_A_SINGLE_CORE_TO_USE_QPC_"></span>**Do I need to set the thread affinity to a single core to use QPC?**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-269">不會。</span><span class="sxs-lookup"><span data-stu-id="f321e-269">No.</span></span> <span data-ttu-id="f321e-270">如需詳細資訊，請參閱 [取得時間戳記的指引](#guidance-for-acquiring-time-stamps)。</span><span class="sxs-lookup"><span data-stu-id="f321e-270">For more info, see [Guidance for acquiring time stamps](#guidance-for-acquiring-time-stamps).</span></span> <span data-ttu-id="f321e-271">這不是必要的，也不是理想的情況。</span><span class="sxs-lookup"><span data-stu-id="f321e-271">This scenario is neither necessary nor desirable.</span></span> <span data-ttu-id="f321e-272">如果有多個執行緒在呼叫 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)時將其親和性設定為相同的核心，執行此案例可能會將處理限制為一個核心，或在單一核心上建立瓶頸，進而對您的應用程式效能造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="f321e-272">Performing this scenario might adversely affect your application's performance by restricting processing to one core or by creating a bottleneck on a single core if multiple threads set their affinity to the same core when calling [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

</dd> </dl>

## <a name="low-level-hardware-clock-characteristics"></a><span data-ttu-id="f321e-273">低層級硬體時鐘特性</span><span class="sxs-lookup"><span data-stu-id="f321e-273">Low-level hardware clock characteristics</span></span>

<span data-ttu-id="f321e-274">這些區段會顯示低層級的硬體時鐘特性。</span><span class="sxs-lookup"><span data-stu-id="f321e-274">These sections show low-level hardware clock characteristics.</span></span>

### <a name="absolute-clocks-and-difference-clocks"></a><span data-ttu-id="f321e-275">絕對時鐘和差異時鐘</span><span class="sxs-lookup"><span data-stu-id="f321e-275">Absolute Clocks and Difference Clocks</span></span>

<span data-ttu-id="f321e-276">絕對時鐘可提供正確的每日讀取時間。</span><span class="sxs-lookup"><span data-stu-id="f321e-276">Absolute clocks provide accurate time-of-day readings.</span></span> <span data-ttu-id="f321e-277">它們通常是以國際標準時間 (UTC) 為基礎，因此其精確度取決於它們同步至外部時間參考的程度。</span><span class="sxs-lookup"><span data-stu-id="f321e-277">They are typically based on Coordinated Universal Time (UTC) and consequently their accuracy depends in part on how well they are synchronized to an external time reference.</span></span> <span data-ttu-id="f321e-278">差異時鐘測量時間間隔，通常不是以外部時間 epoch 為基礎。</span><span class="sxs-lookup"><span data-stu-id="f321e-278">Difference clocks measure time intervals and aren't typically based on an external time epoch.</span></span> <span data-ttu-id="f321e-279">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 是不同的時鐘，而且未同步處理至外部時間 epoch 或參考。</span><span class="sxs-lookup"><span data-stu-id="f321e-279">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) is a difference clock and isn't synchronized to an external time epoch or reference.</span></span> <span data-ttu-id="f321e-280">當您使用 **QPC** 進行時間間隔測量時，您通常會得到比使用衍生自絕對時鐘的時間戳記更好的精確度。</span><span class="sxs-lookup"><span data-stu-id="f321e-280">When you use **QPC** for time-interval measurements, you typically get better accuracy than you would get by using time stamps that are derived from an absolute clock.</span></span> <span data-ttu-id="f321e-281">這是因為同步處理絕對時鐘時間的程式可能會導致階段和頻率移位，從而提高短期時間間隔測量的不確定性。</span><span class="sxs-lookup"><span data-stu-id="f321e-281">This is because the process of synchronizing the time of an absolute clock can introduce phase and frequency shifts that increase the uncertainty of short term time-interval measurements.</span></span>

### <a name="resolution-precision-accuracy-and-stability"></a><span data-ttu-id="f321e-282">解析度、有效位數、精確度和穩定性</span><span class="sxs-lookup"><span data-stu-id="f321e-282">Resolution, Precision, Accuracy, and Stability</span></span>

<span data-ttu-id="f321e-283">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 會使用硬體計數器作為基礎。</span><span class="sxs-lookup"><span data-stu-id="f321e-283">[**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) uses a hardware counter as its basis.</span></span> <span data-ttu-id="f321e-284">硬體計時器包含三個部分：滴答產生器、計算刻度的計數器，以及用來抓取計數器值的方法。</span><span class="sxs-lookup"><span data-stu-id="f321e-284">Hardware timers consist of three parts: a tick generator, a counter that counts the ticks, and a means of retrieving the counter value.</span></span> <span data-ttu-id="f321e-285">這三個元件的特性會決定 **QPC** 的解析度、有效位數、精確度和穩定性。</span><span class="sxs-lookup"><span data-stu-id="f321e-285">The characteristics of these three components determine the resolution, precision, accuracy, and stability of **QPC**.</span></span>

<span data-ttu-id="f321e-286">如果硬體產生器以固定速率提供刻度，只要計算這些刻度，即可測量時間間隔。</span><span class="sxs-lookup"><span data-stu-id="f321e-286">If a hardware generator provides ticks at a constant rate, time intervals can be measured by simply counting these ticks.</span></span> <span data-ttu-id="f321e-287">產生滴答的速率稱為「頻率」，並以赫茲 (Hz) 表示。</span><span class="sxs-lookup"><span data-stu-id="f321e-287">The rate at which the ticks are generated is called the frequency and expressed in Hertz (Hz).</span></span> <span data-ttu-id="f321e-288">相較之下，頻率稱為「期間」或「滴答間隔」，並以適當的國際系統單位來表示 (SI) 時間單位 (例如，第二、毫秒、微秒或毫微秒) 。</span><span class="sxs-lookup"><span data-stu-id="f321e-288">The reciprocal of the frequency is called the period or tick interval and is expressed in an appropriate International System of Units (SI) time unit (for example, second, millisecond, microsecond, or nanosecond).</span></span>

![時間間隔](images/tick-interval.png)

<span data-ttu-id="f321e-290">計時器的解析度等於句號。</span><span class="sxs-lookup"><span data-stu-id="f321e-290">The resolution of the timer is equal to the period.</span></span> <span data-ttu-id="f321e-291">解決方式會決定區別任何兩個時間戳記的能力，並在可以測量的最小時間間隔下放置較低的界限。</span><span class="sxs-lookup"><span data-stu-id="f321e-291">Resolution determines the ability to distinguish between any two time stamps and places a lower bound on the smallest time intervals that can be measured.</span></span> <span data-ttu-id="f321e-292">這有時稱為「滴答解析」。</span><span class="sxs-lookup"><span data-stu-id="f321e-292">This is sometimes called the tick resolution.</span></span>

<span data-ttu-id="f321e-293">數位測量時間引進了±1刻度的測量不確定性，因為數位計數器會在離散步驟中前進，而時間會持續前進。</span><span class="sxs-lookup"><span data-stu-id="f321e-293">Digital measurement of time introduces a measurements uncertainty of ± 1 tick because the digital counter advances in discrete steps, while time is continuously advancing.</span></span> <span data-ttu-id="f321e-294">這種不確定性稱為「量化錯誤」。</span><span class="sxs-lookup"><span data-stu-id="f321e-294">This uncertainty is called a quantization error.</span></span> <span data-ttu-id="f321e-295">針對一般時間間隔測量，通常會忽略此效果，因為量化錯誤比測量的時間間隔小很多。</span><span class="sxs-lookup"><span data-stu-id="f321e-295">For typical time-interval measurements, this effect can often be ignored because the quantizing error is much smaller than the time interval being measured.</span></span>

![數位時間度量](images/digital-time-measure.png)

<span data-ttu-id="f321e-297">但是，如果要測量的期間很小，並接近計時器的解析度，您就必須考慮此量化錯誤。</span><span class="sxs-lookup"><span data-stu-id="f321e-297">However, if the period being measured is small and approaches the resolution of the timer, you will need to consider this quantizing error.</span></span> <span data-ttu-id="f321e-298">所引進的錯誤大小是一個時鐘期間的大小。</span><span class="sxs-lookup"><span data-stu-id="f321e-298">The size of the error introduced is that of one clock period.</span></span>

<span data-ttu-id="f321e-299">下列兩個圖表說明使用具有1個時間單位之解析度的計時器，對±1滴答不確定性的影響。</span><span class="sxs-lookup"><span data-stu-id="f321e-299">The following two diagrams illustrate the impact of the ± 1 tick uncertainty by using a timer with a resolution of 1 time unit.</span></span>

![滴答不確定性](images/tick-uncertainty.png)

<span data-ttu-id="f321e-301">[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) 會傳回 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)的頻率，且句點和解析度等於此值的倒數。</span><span class="sxs-lookup"><span data-stu-id="f321e-301">[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) returns the frequency of [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter), and the period and resolution are equal to the reciprocal of this value.</span></span> <span data-ttu-id="f321e-302">**QueryPerformanceFrequency** 傳回的效能計數器頻率是在系統初始化期間決定，而且在系統執行時不會變更。</span><span class="sxs-lookup"><span data-stu-id="f321e-302">The performance counter frequency that **QueryPerformanceFrequency** returns is determined during system initialization and doesn't change while the system is running.</span></span>

> [!Note]  
> <span data-ttu-id="f321e-303">案例可能存在，而 [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) 不會傳回硬體滴答產生器的實際頻率。</span><span class="sxs-lookup"><span data-stu-id="f321e-303">Cases might exist where [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) doesn't return the actual frequency of the hardware tick generator.</span></span> <span data-ttu-id="f321e-304">例如，在許多情況下， **QueryPerformanceFrequency** 會傳回依1024的 TSC 頻率除以;而在 Hyper-v 上，當來賓虛擬機器在執行程式管理 [版本1.0 介面](https://msdn.microsoft.com/library/Ff541458(v=VS.85).aspx)的 [虛擬](https://msdn.microsoft.com/library/Ff542584(v=VS.85).aspx)程式下執行時，效能計數器的頻率一律為 10 MHz。</span><span class="sxs-lookup"><span data-stu-id="f321e-304">For example, in many cases, **QueryPerformanceFrequency** returns the TSC frequency divided by 1024; and on Hyper-V, the performance counter frequency is always 10 MHz when the guest virtual machine runs under a [hypervisor](https://msdn.microsoft.com/library/Ff542584(v=VS.85).aspx) that implements the [hypervisor version 1.0 interface](https://msdn.microsoft.com/library/Ff541458(v=VS.85).aspx).</span></span> <span data-ttu-id="f321e-305">因此，請不要假設 **QueryPerformanceFrequency** 會傳回精確的 TSC 頻率。</span><span class="sxs-lookup"><span data-stu-id="f321e-305">As a result, don't assume that **QueryPerformanceFrequency** will return the precise TSC frequency.</span></span>

 

<span data-ttu-id="f321e-306">[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 會讀取效能計數器，並傳回自 Windows 作業系統啟動以來發生的總滴答數，包括電腦處於睡眠狀態的時間，例如待命、休眠或連線待命。</span><span class="sxs-lookup"><span data-stu-id="f321e-306">[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) reads the performance counter and returns the total number of ticks that have occurred since the Windows operating system was started, including the time when the machine was in a sleep state such as standby, hibernate, or connected standby.</span></span>

<span data-ttu-id="f321e-307">這些範例示範如何計算滴答間隔和解決方式，以及如何將滴答計數轉換成時間值。</span><span class="sxs-lookup"><span data-stu-id="f321e-307">These examples show how to calculate the tick interval and resolution and how to convert the tick count into a time value.</span></span>

<dl> <dt>

<span data-ttu-id="f321e-308"><span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**範例1**</span><span class="sxs-lookup"><span data-stu-id="f321e-308"><span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Example 1**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-309">[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) 會在特定電腦上傳回值3125000。</span><span class="sxs-lookup"><span data-stu-id="f321e-309">[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) returns the value 3,125,000 on a particular machine.</span></span> <span data-ttu-id="f321e-310">這台電腦上的 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 度量的滴答間隔和解析度為何？</span><span class="sxs-lookup"><span data-stu-id="f321e-310">What is the tick interval and resolution of [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) measurements on this machine?</span></span> <span data-ttu-id="f321e-311">滴答間隔（或期間）是3125000的倒數，也就是 0.000000320 (320 毫微秒) 。</span><span class="sxs-lookup"><span data-stu-id="f321e-311">The tick interval, or period, is the reciprocal of 3,125,000, which is 0.000000320 (320 nanoseconds).</span></span> <span data-ttu-id="f321e-312">因此，每個刻度都代表傳遞320毫微秒。</span><span class="sxs-lookup"><span data-stu-id="f321e-312">Therefore, each tick represents the passing of 320 nanoseconds.</span></span> <span data-ttu-id="f321e-313">無法在這部電腦上測量小於320毫微秒的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="f321e-313">Time intervals smaller than 320 nanoseconds can't be measured on this machine.</span></span>

<span data-ttu-id="f321e-314">滴答間隔 = 1/ (效能頻率) </span><span class="sxs-lookup"><span data-stu-id="f321e-314">Tick Interval = 1/(Performance Frequency)</span></span>

<span data-ttu-id="f321e-315">滴答間隔 = 1/3125000 = 320 ns</span><span class="sxs-lookup"><span data-stu-id="f321e-315">Tick Interval = 1/3,125,000 = 320 ns</span></span>

</dd> <dt>

<span data-ttu-id="f321e-316"><span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**範例2**</span><span class="sxs-lookup"><span data-stu-id="f321e-316"><span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Example 2**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-317">在與上述範例相同的電腦上，從兩次連續呼叫 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 傳回的值的差異為5。</span><span class="sxs-lookup"><span data-stu-id="f321e-317">On the same machine as the preceding example, the difference of the values returned from two successive calls to [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) is 5.</span></span> <span data-ttu-id="f321e-318">兩次呼叫之間經過了多少時間？</span><span class="sxs-lookup"><span data-stu-id="f321e-318">How much time has elapsed between the two calls?</span></span> <span data-ttu-id="f321e-319">5個刻度乘以320毫微秒會產生1.6 微秒。</span><span class="sxs-lookup"><span data-stu-id="f321e-319">5 ticks multiplied by 320 nanoseconds yields 1.6 microseconds.</span></span>

<span data-ttu-id="f321e-320">經過時間 = 滴答 \* 滴答間隔</span><span class="sxs-lookup"><span data-stu-id="f321e-320">ElapsedTime = Ticks \* Tick Interval</span></span>

<span data-ttu-id="f321e-321">經過時間 = 5 \* 320 ns = 1.6 μs</span><span class="sxs-lookup"><span data-stu-id="f321e-321">ElapsedTime = 5 \* 320 ns = 1.6 μs</span></span>

</dd> </dl>

<span data-ttu-id="f321e-322">從軟體存取 (讀取) 滴答計數器需要一些時間，而且此存取時間可以減少時間測量的精確度。</span><span class="sxs-lookup"><span data-stu-id="f321e-322">It takes time to access (read) the tick counter from software, and this access time can reduce the precision of the of the time measurement.</span></span> <span data-ttu-id="f321e-323">這是因為最小間隔時間 (可測量的最小時間間隔) 是解析度的較大和存取時間。</span><span class="sxs-lookup"><span data-stu-id="f321e-323">This is because the minimum interval time (the smallest time interval that can be measured) is the larger of the resolution and the access time.</span></span>

<span data-ttu-id="f321e-324">Precision = MAX \[ 解析，AccessTime\]</span><span class="sxs-lookup"><span data-stu-id="f321e-324">Precision = MAX \[ Resolution, AccessTime\]</span></span>

<span data-ttu-id="f321e-325">例如，假設有一個假設性的硬體計時器，其解析度為100的毫微秒，以及800納秒的存取時間。</span><span class="sxs-lookup"><span data-stu-id="f321e-325">For example, consider a hypothetical hardware timer with a 100 nanosecond resolution and an 800 nanosecond access time.</span></span> <span data-ttu-id="f321e-326">如果使用平臺計時器而非使用 TSC 登錄作為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)基礎，則可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="f321e-326">This might be the case if the platform timer were used instead of the TSC register as the basis of [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span> <span data-ttu-id="f321e-327">因此，精確度會是800毫微秒，不是100毫微秒，如這項計算所示。</span><span class="sxs-lookup"><span data-stu-id="f321e-327">Thus, the precision would be 800 nanoseconds not 100 nanoseconds as shown in this calculation.</span></span>

<span data-ttu-id="f321e-328">Precision = MAX \[ 800 ns，100 ns \] = 800 ns</span><span class="sxs-lookup"><span data-stu-id="f321e-328">Precision = MAX \[800 ns,100 ns\] = 800 ns</span></span>

<span data-ttu-id="f321e-329">這兩個圖表描述此效果。</span><span class="sxs-lookup"><span data-stu-id="f321e-329">These two figures depict this effect.</span></span>

![qpc 存取時間](images/qpc-access-time.png)

<span data-ttu-id="f321e-331">如果存取時間大於解決方式，請不要嘗試透過猜測來改善精確度。</span><span class="sxs-lookup"><span data-stu-id="f321e-331">If the access time is greater than the resolution, don't try to improve the precision by guessing.</span></span> <span data-ttu-id="f321e-332">換句話說，假設時間戳記是在中間，或是在呼叫的開頭或結尾時，就會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="f321e-332">In other words, it's an error to assume that the time stamp is taken precisely in the middle, or at the beginning or the end of the call.</span></span>

<span data-ttu-id="f321e-333">相反地，請考慮下列範例，其中 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 存取時間只有20個納秒，而硬體時鐘解析度為100毫微秒。</span><span class="sxs-lookup"><span data-stu-id="f321e-333">By contrast, consider the following example in which the [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) access time is only 20 nanoseconds and the hardware clock resolution is 100 nanoseconds.</span></span> <span data-ttu-id="f321e-334">如果使用 TSC 登錄作為 **QPC** 的基礎，則可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="f321e-334">This might be the case if the TSC register was used as the basis for **QPC**.</span></span> <span data-ttu-id="f321e-335">在這裡，精確度會受限於時鐘解析。</span><span class="sxs-lookup"><span data-stu-id="f321e-335">Here the precision is limited by the clock resolution.</span></span>

![qpc 精確度](images/qpc-precision.png)

<span data-ttu-id="f321e-337">在實務上，您可以找到讀取計數器所需時間大於或小於解析度的時間來源。</span><span class="sxs-lookup"><span data-stu-id="f321e-337">In practice, you can find time sources for which the time required to read the counter is larger or smaller than the resolution.</span></span> <span data-ttu-id="f321e-338">無論是哪一種情況，精確度都會是兩者中較大的一個。</span><span class="sxs-lookup"><span data-stu-id="f321e-338">In either case, the precision will be the larger of the two.</span></span>

<span data-ttu-id="f321e-339">下表提供各種時鐘的大約解析、存取時間和精確度的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f321e-339">This table provides info on the approximate resolution, access time, and precision of a variety of clocks.</span></span> <span data-ttu-id="f321e-340">請注意，有些值會隨著不同的處理器、硬體平臺和處理器速度而有所不同。</span><span class="sxs-lookup"><span data-stu-id="f321e-340">Note that some of the values will vary with different processors, hardware platforms, and processor speeds.</span></span>



| <span data-ttu-id="f321e-341">時鐘來源</span><span class="sxs-lookup"><span data-stu-id="f321e-341">Clock Source</span></span>                                                      | <span data-ttu-id="f321e-342">名義時鐘頻率</span><span class="sxs-lookup"><span data-stu-id="f321e-342">Nominal Clock Frequency</span></span> | <span data-ttu-id="f321e-343">時鐘解析</span><span class="sxs-lookup"><span data-stu-id="f321e-343">Clock Resolution</span></span>    | <span data-ttu-id="f321e-344">存取時間 (一般) </span><span class="sxs-lookup"><span data-stu-id="f321e-344">Access Time (Typical)</span></span> | <span data-ttu-id="f321e-345">準確率</span><span class="sxs-lookup"><span data-stu-id="f321e-345">Precision</span></span>       |
|-------------------------------------------------------------------|-------------------------|---------------------|-----------------------|-----------------|
| <span data-ttu-id="f321e-346">電腦 RTC</span><span class="sxs-lookup"><span data-stu-id="f321e-346">PC RTC</span></span>                                                            | <span data-ttu-id="f321e-347">64 Hz</span><span class="sxs-lookup"><span data-stu-id="f321e-347">64 Hz</span></span>                   | <span data-ttu-id="f321e-348">15.625 毫秒</span><span class="sxs-lookup"><span data-stu-id="f321e-348">15.625 milliseconds</span></span> | <span data-ttu-id="f321e-349">N/A</span><span class="sxs-lookup"><span data-stu-id="f321e-349">N/A</span></span>                   | <span data-ttu-id="f321e-350">N/A</span><span class="sxs-lookup"><span data-stu-id="f321e-350">N/A</span></span>             |
| <span data-ttu-id="f321e-351">使用具有 3 GHz 處理器時鐘的 TSC 的查詢效能計數器</span><span class="sxs-lookup"><span data-stu-id="f321e-351">Query performance counter using TSC with a 3 GHz processor clock</span></span>  | <span data-ttu-id="f321e-352">3 MHz</span><span class="sxs-lookup"><span data-stu-id="f321e-352">3 MHz</span></span>                   | <span data-ttu-id="f321e-353">333毫微秒</span><span class="sxs-lookup"><span data-stu-id="f321e-353">333 nanoseconds</span></span>     | <span data-ttu-id="f321e-354">30毫微秒</span><span class="sxs-lookup"><span data-stu-id="f321e-354">30 nanoseconds</span></span>        | <span data-ttu-id="f321e-355">333毫微秒</span><span class="sxs-lookup"><span data-stu-id="f321e-355">333 nanoseconds</span></span> |
| <span data-ttu-id="f321e-356">在具有 3 GHz 週期時間的系統上 **RDTSC** 機器指令</span><span class="sxs-lookup"><span data-stu-id="f321e-356">**RDTSC** machine instruction on a system with a 3 GHz cycle time</span></span> | <span data-ttu-id="f321e-357">3 GHz</span><span class="sxs-lookup"><span data-stu-id="f321e-357">3 GHz</span></span>                   | <span data-ttu-id="f321e-358">333 picoseconds</span><span class="sxs-lookup"><span data-stu-id="f321e-358">333 picoseconds</span></span>     | <span data-ttu-id="f321e-359">30毫微秒</span><span class="sxs-lookup"><span data-stu-id="f321e-359">30 nanoseconds</span></span>        | <span data-ttu-id="f321e-360">30毫微秒</span><span class="sxs-lookup"><span data-stu-id="f321e-360">30 nanoseconds</span></span>  |



 

<span data-ttu-id="f321e-361">由於 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 會使用硬體計數器，因此當您瞭解硬體計數器的一些基本特性時，您會瞭解 **QPC** 的功能和限制。</span><span class="sxs-lookup"><span data-stu-id="f321e-361">Because [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) uses a hardware counter, when you understand some basic characteristics of hardware counters, you gain understanding about the capabilities and limitations of **QPC**.</span></span>

<span data-ttu-id="f321e-362">最常使用的硬體滴答產生器是 crystal oscillator。</span><span class="sxs-lookup"><span data-stu-id="f321e-362">The most commonly used hardware tick generator is a crystal oscillator.</span></span> <span data-ttu-id="f321e-363">Crystal 是一小部分的 quartz 或其他 ceramic 材質，展示 piezoelectric 的特性，可提供價格實惠的頻率參考，並具備絕佳的穩定性和精確度。</span><span class="sxs-lookup"><span data-stu-id="f321e-363">The crystal is a small piece of quartz or other ceramic material that exhibits piezoelectric characteristics that provide an inexpensive frequency reference with excellent stability and accuracy.</span></span> <span data-ttu-id="f321e-364">此頻率可用來產生時鐘所計算的刻度。</span><span class="sxs-lookup"><span data-stu-id="f321e-364">This frequency is used to generate the ticks counted by the clock.</span></span>

<span data-ttu-id="f321e-365">計時器的精確度是指符合 true 或標準值的一致性程度。</span><span class="sxs-lookup"><span data-stu-id="f321e-365">The accuracy of a timer refers to the degree of conformity to a true or standard value.</span></span> <span data-ttu-id="f321e-366">這主要取決於 crystal oscillator 能以指定的頻率提供刻度。</span><span class="sxs-lookup"><span data-stu-id="f321e-366">This depends primarily on the crystal oscillator’s ability to provide ticks at the specified frequency.</span></span> <span data-ttu-id="f321e-367">如果震盪的頻率過高，時鐘將會「快速執行」，且測量的間隔將會比實際時間更長;而且，如果頻率過低，時鐘將會「執行緩慢」，且測量的間隔會比實際的時間短。</span><span class="sxs-lookup"><span data-stu-id="f321e-367">If the frequency of oscillation is too high, the clock will 'run fast', and measured intervals will appear longer than they really are; and if the frequency is too low, the clock will 'run slow', and measured intervals will appear shorter than they really are.</span></span>

<span data-ttu-id="f321e-368">針對短暫期間的一般時間間隔度量 (例如，回應時間測量、網路延遲測量等等) ，硬體 oscillator 的精確度通常就已足夠。</span><span class="sxs-lookup"><span data-stu-id="f321e-368">For typical time-interval measurements for short duration (for example, response time measurements, network latency measurements, and so on), the accuracy of the hardware oscillator is usually sufficient.</span></span> <span data-ttu-id="f321e-369">不過，對於某些測量，oscillator 頻率的精確度會變得很重要，特別是在長時間間隔內，或當您想要比較在不同電腦上所做的度量時。</span><span class="sxs-lookup"><span data-stu-id="f321e-369">However, for some measurements the oscillator frequency accuracy becomes important, particularly for long time intervals or when you want to compare measurements taken on different machines.</span></span> <span data-ttu-id="f321e-370">本節的其餘部分將探索 oscillator 精確度的影響。</span><span class="sxs-lookup"><span data-stu-id="f321e-370">The remainder of this section explores the effects of the oscillator accuracy.</span></span>

<span data-ttu-id="f321e-371">Crystals 的震盪頻率是在製造過程中設定的，製造商會以指定的頻率加上或減去製造容忍度（以「每百萬個部分」表示的製造容忍度為單位） (ppm) ，稱為最大頻率位移。</span><span class="sxs-lookup"><span data-stu-id="f321e-371">The crystals' frequency of oscillation is set during the manufacturing process and is specified by the manufacturer in terms of a specified frequency plus or minus a manufacturing tolerance expressed in 'parts per million' (ppm), called the maximum frequency offset.</span></span> <span data-ttu-id="f321e-372">如果其實際頻率介於 999990 Hz 和 1000010 Hz 之間，則指定頻率為 1000000 Hz 且最大頻率位移為± 10 ppm 的 crystal 會在規格限制內。</span><span class="sxs-lookup"><span data-stu-id="f321e-372">A crystal with a specified frequency of 1,000,000 Hz and a maximum frequency offset of ± 10 ppm would be within specification limits if its actual frequency were between 999,990 Hz and 1,000,010 Hz.</span></span>

<span data-ttu-id="f321e-373">藉由以每秒每秒的毫秒數來取代片語部分，我們可以將此頻率位移誤差套用至時間間隔測量。</span><span class="sxs-lookup"><span data-stu-id="f321e-373">By substituting the phrase parts per million with microseconds per second, we can apply this frequency offset error to time-interval measurements.</span></span> <span data-ttu-id="f321e-374">具有 + 10 ppm 位移的 oscillator 會有每秒10毫秒的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f321e-374">An oscillator with a + 10 ppm offset would have an error of 10 microseconds per second.</span></span> <span data-ttu-id="f321e-375">因此，當測量1秒的間隔時，它會快速執行，並將1秒的間隔測量為0.999990 秒。</span><span class="sxs-lookup"><span data-stu-id="f321e-375">Accordingly, when measuring a 1 second interval, it would run fast and measure a 1 second interval as 0.999990 seconds.</span></span>

<span data-ttu-id="f321e-376">很方便的參考是，100 ppm 的頻率錯誤會在24小時後導致8.64 秒的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f321e-376">A convenient reference is that a frequency error of 100 ppm causes an error of 8.64 seconds after 24 hours.</span></span> <span data-ttu-id="f321e-377">由於累積的錯誤較長的時間間隔，此資料表會顯示測量不確定性。</span><span class="sxs-lookup"><span data-stu-id="f321e-377">This table presents the measurement uncertainty due to the accumulated error for longer time intervals.</span></span>



| <span data-ttu-id="f321e-378">時間間隔持續時間</span><span class="sxs-lookup"><span data-stu-id="f321e-378">Time interval duration</span></span> | <span data-ttu-id="f321e-379">因具有 +/-10 PPM 頻率容忍性的累積錯誤而造成的測量不確定性</span><span class="sxs-lookup"><span data-stu-id="f321e-379">Measurement uncertainty due to accumulated error with +/- 10 PPM frequency tolerance</span></span> |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f321e-380">1微秒</span><span class="sxs-lookup"><span data-stu-id="f321e-380">1 microsecond</span></span>          | <span data-ttu-id="f321e-381">± 10 picoseconds (10-12) </span><span class="sxs-lookup"><span data-stu-id="f321e-381">± 10 picoseconds (10-12)</span></span>                                                             |
| <span data-ttu-id="f321e-382">1毫秒</span><span class="sxs-lookup"><span data-stu-id="f321e-382">1 millisecond</span></span>          | <span data-ttu-id="f321e-383">±10毫微秒 (10-9) </span><span class="sxs-lookup"><span data-stu-id="f321e-383">± 10 nanoseconds (10-9)</span></span>                                                              |
| <span data-ttu-id="f321e-384">1 秒</span><span class="sxs-lookup"><span data-stu-id="f321e-384">1 second</span></span>               | <span data-ttu-id="f321e-385">±10毫秒</span><span class="sxs-lookup"><span data-stu-id="f321e-385">± 10 microseconds</span></span>                                                                    |
| <span data-ttu-id="f321e-386">1 小時</span><span class="sxs-lookup"><span data-stu-id="f321e-386">1 hour</span></span>                 | <span data-ttu-id="f321e-387">±60微秒</span><span class="sxs-lookup"><span data-stu-id="f321e-387">± 60 microseconds</span></span>                                                                    |
| <span data-ttu-id="f321e-388">1 日</span><span class="sxs-lookup"><span data-stu-id="f321e-388">1 day</span></span>                  | <span data-ttu-id="f321e-389">±0.86 秒</span><span class="sxs-lookup"><span data-stu-id="f321e-389">± 0.86 seconds</span></span>                                                                       |
| <span data-ttu-id="f321e-390">1 週</span><span class="sxs-lookup"><span data-stu-id="f321e-390">1 week</span></span>                 | <span data-ttu-id="f321e-391">±6.08 秒</span><span class="sxs-lookup"><span data-stu-id="f321e-391">± 6.08 seconds</span></span>                                                                       |



 

<span data-ttu-id="f321e-392">上表顯示針對較短的時間間隔，頻率位移誤差通常可以忽略。</span><span class="sxs-lookup"><span data-stu-id="f321e-392">The preceding table shows that for small time intervals the frequency offset error can often be ignored.</span></span> <span data-ttu-id="f321e-393">不過，在長時間間隔內，即使是較小的頻率位移，也可能造成大量的測量不確定性。</span><span class="sxs-lookup"><span data-stu-id="f321e-393">However for long time intervals, even a small frequency offset can result in a substantial measurement uncertainty.</span></span>

<span data-ttu-id="f321e-394">在個人電腦和伺服器中使用的 Crystal 聲音振盪器通常會以±30到50個部分的頻率承受度製造，而且很少 crystals 可以離 500 ppm。</span><span class="sxs-lookup"><span data-stu-id="f321e-394">Crystal oscillators that are used in personal computers and servers are typically manufactured with a frequency tolerance of ± 30 to 50 parts per million, and rarely, crystals can be off by as much as 500 ppm.</span></span> <span data-ttu-id="f321e-395">雖然 crystals 具有更緊密的頻率位移容限，但它們較昂貴，因此不會在大部分的電腦中使用。</span><span class="sxs-lookup"><span data-stu-id="f321e-395">Although crystals with much tighter frequency offset tolerances are available, they are more expensive and thus are not used in most computers.</span></span>

<span data-ttu-id="f321e-396">若要降低此頻率位移錯誤的負面影響，最新的 Windows 版本（特別是 Windows 8）會使用多個硬體計時器來偵測頻率位移，並將其補償到可能的程度。</span><span class="sxs-lookup"><span data-stu-id="f321e-396">To reduce the adverse effects of this frequency offset error, recent versions of Windows, particularly Windows 8, use multiple hardware timers to detect the frequency offset and compensate for it to the extent possible.</span></span> <span data-ttu-id="f321e-397">此校正程式是在 Windows 啟動時執行。</span><span class="sxs-lookup"><span data-stu-id="f321e-397">This calibration process is performed when Windows is started.</span></span>

<span data-ttu-id="f321e-398">如下列範例所示，硬體時鐘的頻率位移錯誤會影響可達成的精確度，而且時鐘的解析度可能較不重要。</span><span class="sxs-lookup"><span data-stu-id="f321e-398">As the following examples show, the frequency offset error of a hardware clock influences the achievable accuracy, and the resolution of the clock can be less important.</span></span>

![頻率位移錯誤會影響可達成的精確度](images/freq-offset-error.png)

<dl> <dt>

<span data-ttu-id="f321e-400"><span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**範例1**</span><span class="sxs-lookup"><span data-stu-id="f321e-400"><span id="Example_1"></span><span id="example_1"></span><span id="EXAMPLE_1"></span>**Example 1**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-401">假設您使用 1 MHz oscillator （具有1微秒的解析度，以及± 50 ppm 的最大頻率位移誤差）來執行時間間隔測量。</span><span class="sxs-lookup"><span data-stu-id="f321e-401">Suppose you perform time-interval measurements by using a 1 MHz oscillator, which has a resolution of 1 microsecond, and a maximum frequency offset error of ±50 ppm.</span></span> <span data-ttu-id="f321e-402">現在，讓我們假設位移正好是 + 50 ppm。</span><span class="sxs-lookup"><span data-stu-id="f321e-402">Now, let us suppose the offset is exactly +50 ppm.</span></span> <span data-ttu-id="f321e-403">這表示實際的頻率會是 1000050 Hz。</span><span class="sxs-lookup"><span data-stu-id="f321e-403">This means that the actual frequency would be 1,000,050 Hz.</span></span> <span data-ttu-id="f321e-404">如果我們測量的是24小時的時間間隔，我們的測量會是4.3 秒太短 (23：59：55.700000 測量與24：00：00.000000 實際) 。</span><span class="sxs-lookup"><span data-stu-id="f321e-404">If we measured a time interval of 24 hours, our measurement would be 4.3 seconds too short (23:59:55.700000 measured versus 24:00:00.000000 actual).</span></span>

<span data-ttu-id="f321e-405">一天中的秒數 = 86400</span><span class="sxs-lookup"><span data-stu-id="f321e-405">Seconds in a day = 86400</span></span>

<span data-ttu-id="f321e-406">頻率位移錯誤 = 50 ppm = 0.00005</span><span class="sxs-lookup"><span data-stu-id="f321e-406">Frequency offset error = 50 ppm = 0.00005</span></span>

<span data-ttu-id="f321e-407">86400秒 \* 0.00005 = 4.3 秒</span><span class="sxs-lookup"><span data-stu-id="f321e-407">86,400 seconds \* 0.00005 = 4.3 seconds</span></span>

</dd> <dt>

<span data-ttu-id="f321e-408"><span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**範例2**</span><span class="sxs-lookup"><span data-stu-id="f321e-408"><span id="Example_2"></span><span id="example_2"></span><span id="EXAMPLE_2"></span>**Example 2**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-409">假設處理器 TSC 時鐘由 crystal oscillator 控制，並指定頻率為 3 GHz。</span><span class="sxs-lookup"><span data-stu-id="f321e-409">Suppose the processor TSC clock is controlled by a crystal oscillator and has specified frequency of 3 GHz.</span></span> <span data-ttu-id="f321e-410">這表示解析度會是 1/3000000000 或約 333 picoseconds。</span><span class="sxs-lookup"><span data-stu-id="f321e-410">This means that the resolution would be 1/3,000,000,000 or about 333 picoseconds.</span></span> <span data-ttu-id="f321e-411">假設用來控制處理器時鐘的 crystal 具有± 50 ppm 的頻率容錯，其實是 + 50 ppm。</span><span class="sxs-lookup"><span data-stu-id="f321e-411">Assume the crystal used to control the processor clock has a frequency tolerance of ±50 ppm and is actually +50 ppm.</span></span> <span data-ttu-id="f321e-412">儘管有令人印象深刻的解決方式，但24小時的時間間隔量值仍會是4.3 秒太短。</span><span class="sxs-lookup"><span data-stu-id="f321e-412">In spite of the impressive resolution, a time-interval measurement of 24 hours will still be 4.3 seconds too short.</span></span> <span data-ttu-id="f321e-413"> (23：59：55.7000000000 測量與24：00：00.0000000000 實際) 。</span><span class="sxs-lookup"><span data-stu-id="f321e-413">(23:59:55.7000000000 measured versus 24:00:00.0000000000 actual).</span></span>

<span data-ttu-id="f321e-414">一天中的秒數 = 86400</span><span class="sxs-lookup"><span data-stu-id="f321e-414">Seconds in a day = 86400</span></span>

<span data-ttu-id="f321e-415">頻率位移錯誤 = 50 ppm = 0.00005</span><span class="sxs-lookup"><span data-stu-id="f321e-415">Frequency offset error = 50 ppm = 0.00005</span></span>

<span data-ttu-id="f321e-416">86400秒 \* 0.00005 = 4.3 秒</span><span class="sxs-lookup"><span data-stu-id="f321e-416">86,400 seconds \* 0.00005 = 4.3 seconds</span></span>

<span data-ttu-id="f321e-417">這會顯示高解析度的 TSC 時鐘不一定能提供比較低解析度時鐘更精確的度量。</span><span class="sxs-lookup"><span data-stu-id="f321e-417">This shows that a high resolution TSC clock doesn't necessarily provide more accurate measurements than a lower resolution clock.</span></span>

</dd> <dt>

<span data-ttu-id="f321e-418"><span id="Example_3"></span><span id="example_3"></span><span id="EXAMPLE_3"></span>**範例3**</span><span class="sxs-lookup"><span data-stu-id="f321e-418"><span id="Example_3"></span><span id="example_3"></span><span id="EXAMPLE_3"></span>**Example 3**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-419">請考慮使用兩部不同的電腦來測量相同的24小時時間間隔。</span><span class="sxs-lookup"><span data-stu-id="f321e-419">Consider using two different computers to measure the same 24 hour time interval.</span></span> <span data-ttu-id="f321e-420">這兩部電腦都有一個 oscillator，最大頻率位移為± 50 ppm。</span><span class="sxs-lookup"><span data-stu-id="f321e-420">Both computers have an oscillator with a maximum frequency offset of ± 50 ppm.</span></span> <span data-ttu-id="f321e-421">這兩個系統上的相同時間間隔可以有多遠？</span><span class="sxs-lookup"><span data-stu-id="f321e-421">How far apart can the measurement of the same time interval on these two systems be?</span></span> <span data-ttu-id="f321e-422">如同先前的範例，± 50 ppm 會在24小時後產生最多±4.3 秒的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f321e-422">As in the previous examples, ± 50 ppm yields a maximum error of ± 4.3 seconds after 24 hours.</span></span> <span data-ttu-id="f321e-423">如果有一個系統快速執行4.3 秒，而另一個4.3 秒的速度變慢，24小時之後的最大錯誤可能會是8.6 秒。</span><span class="sxs-lookup"><span data-stu-id="f321e-423">If one system runs 4.3 seconds fast, and the other 4.3 seconds slow, the maximum error after 24 hours could be 8.6 seconds.</span></span>

<span data-ttu-id="f321e-424">一天中的秒數 = 86400</span><span class="sxs-lookup"><span data-stu-id="f321e-424">Seconds in a day = 86400</span></span>

<span data-ttu-id="f321e-425">頻率位移錯誤 = ± 50 ppm = ±0.00005</span><span class="sxs-lookup"><span data-stu-id="f321e-425">Frequency offset error = ±50 ppm = ±0.00005</span></span>

<span data-ttu-id="f321e-426">± (86400 秒 \* 0.00005) = ±4.3 秒</span><span class="sxs-lookup"><span data-stu-id="f321e-426">±(86,400 seconds \* 0.00005) = ±4.3 seconds</span></span>

<span data-ttu-id="f321e-427">兩個系統之間的最大位移 = 8.6 秒</span><span class="sxs-lookup"><span data-stu-id="f321e-427">Maximum offset between the two systems = 8.6 seconds</span></span>

<span data-ttu-id="f321e-428">總而言之，測量長時間間隔以及比較不同系統之間的度量時，頻率位移誤差會變得越來越重要。</span><span class="sxs-lookup"><span data-stu-id="f321e-428">In summary, the frequency offset error becomes increasingly important when measuring long time intervals and when comparing measurements between different systems.</span></span>

<span data-ttu-id="f321e-429">計時器的穩定性描述滴答頻率是否會隨著時間而改變，例如溫度變更的結果。</span><span class="sxs-lookup"><span data-stu-id="f321e-429">The stability of a timer describes whether the tick frequency changes over time, for example as the result of temperatures changes.</span></span> <span data-ttu-id="f321e-430">使用 Quartz crystals 做為電腦上的滴答產生器，會以頻率的函式來呈現較小的頻率變更。</span><span class="sxs-lookup"><span data-stu-id="f321e-430">Quartz crystals used as the tick generators on computers will exhibit small changes in frequency as a function of temperature.</span></span> <span data-ttu-id="f321e-431">相較于一般溫度範圍的頻率位移錯誤，散熱漂移所造成的錯誤通常很小。</span><span class="sxs-lookup"><span data-stu-id="f321e-431">The error caused by thermal drift is typically small compared to the frequency offset error for common temperature ranges.</span></span> <span data-ttu-id="f321e-432">不過，受限於大型溫度波動的可攜式裝置或設備的軟體設計人員可能需要考慮此效果。</span><span class="sxs-lookup"><span data-stu-id="f321e-432">However, designers of software for portable equipment or equipment subject to large temperature fluctuations might need to consider this effect.</span></span>

</dd> </dl>

## <a name="hardware-timer-info"></a><span data-ttu-id="f321e-433">硬體計時器資訊</span><span class="sxs-lookup"><span data-stu-id="f321e-433">Hardware timer info</span></span>

<dl> <dt>

<span data-ttu-id="f321e-434"><span id="TSC_Register"></span><span id="tsc_register"></span><span id="TSC_REGISTER"></span>**TSC 註冊**</span><span class="sxs-lookup"><span data-stu-id="f321e-434"><span id="TSC_Register"></span><span id="tsc_register"></span><span id="TSC_REGISTER"></span>**TSC Register**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-435">某些 Intel 和 AMD 處理器包含的 TSC 暫存器是64位暫存器，它會以較高的速率增加，通常等於處理器時鐘。</span><span class="sxs-lookup"><span data-stu-id="f321e-435">Some Intel and AMD processors contain a TSC register that is a 64-bit register that increases at a high rate, typically equal to the processor clock.</span></span> <span data-ttu-id="f321e-436">您可以透過 **RDTSC** 或 **RDTSCP** 機器指示讀取此計數器的值，以數十或數百部機器週期的順序提供非常低的存取時間和計算成本，視處理器而定。</span><span class="sxs-lookup"><span data-stu-id="f321e-436">The value of this counter can be read through the **RDTSC** or **RDTSCP** machine instructions, providing very low access time and computational cost in the order of tens or hundreds of machine cycles, depending upon the processor.</span></span>

<span data-ttu-id="f321e-437">雖然 TSC 登錄看起來像是理想的時間戳記機制，但在此情況下，它無法針對 timekeeping 用途可靠地運作：</span><span class="sxs-lookup"><span data-stu-id="f321e-437">Although the TSC register seems like an ideal time stamp mechanism, here are circumstances in which it can't function reliably for timekeeping purposes:</span></span>

-   <span data-ttu-id="f321e-438">並非所有處理器都有 TSC 登錄，因此使用軟體中的 TSC 註冊可直接建立可攜性問題。</span><span class="sxs-lookup"><span data-stu-id="f321e-438">Not all processors have TSC registers, so using the TSC register in software directly creates a portability problem.</span></span> <span data-ttu-id="f321e-439">在此情況下， (Windows 將會為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) 選取替代的時間來源，以避免可攜性問題。 ) </span><span class="sxs-lookup"><span data-stu-id="f321e-439">(Windows will select an alternative time source for [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) in this case, which avoids the portability problem.)</span></span>
-   <span data-ttu-id="f321e-440">有些處理器可能會改變 TSC 時鐘的頻率，或停止 TSC 登錄的進展，讓 TSC 不適合這些處理器上的時間用途。</span><span class="sxs-lookup"><span data-stu-id="f321e-440">Some processors can vary the frequency of the TSC clock or stop the advancement of the TSC register, which makes the TSC unsuitable for timing purposes on these processors.</span></span> <span data-ttu-id="f321e-441">這些處理器稱為具有非不變的 TSC 登錄。</span><span class="sxs-lookup"><span data-stu-id="f321e-441">These processors are said to have non-invariant TSC registers.</span></span> <span data-ttu-id="f321e-442"> (Windows 會自動偵測到此情況，並為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)) 選取替代的時間來源。</span><span class="sxs-lookup"><span data-stu-id="f321e-442">(Windows will automatically detect this, and select an alternative time source for [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).</span></span>
-   <span data-ttu-id="f321e-443">在多處理器或多核心系統上，有些處理器和系統無法將每個核心上的時鐘同步處理為相同的值。</span><span class="sxs-lookup"><span data-stu-id="f321e-443">On multi-processor or multi-core systems, some processors and systems are unable to synchronize the clocks on each core to the same value.</span></span> <span data-ttu-id="f321e-444"> (Windows 會自動偵測到此情況，並為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)) 選取替代的時間來源。</span><span class="sxs-lookup"><span data-stu-id="f321e-444">(Windows will automatically detect this, and select an alternative time source for [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).</span></span>
-   <span data-ttu-id="f321e-445">在某些大型的多處理器系統上，即使處理器具有不變的 TSC，您可能還是無法將處理器時鐘同步處理為相同的值。</span><span class="sxs-lookup"><span data-stu-id="f321e-445">On some large multi-processor systems, you might not be able to synchronize the processor clocks to the same value even if the processor has an invariant TSC.</span></span> <span data-ttu-id="f321e-446"> (Windows 會自動偵測到此情況，並為 [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)) 選取替代的時間來源。</span><span class="sxs-lookup"><span data-stu-id="f321e-446">(Windows will automatically detect this, and select an alternative time source for [**QPC**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)).</span></span>
-   <span data-ttu-id="f321e-447">有些處理器會依序執行指令。</span><span class="sxs-lookup"><span data-stu-id="f321e-447">Some processors will execute instructions out of order.</span></span> <span data-ttu-id="f321e-448">當使用 **RDTSC** 來時間指令序列時，這可能會導致不正確的迴圈計數，因為 **RDTSC** 指令可能會在您的程式中指定的時間以外執行。</span><span class="sxs-lookup"><span data-stu-id="f321e-448">This can result in incorrect cycle counts when **RDTSC** is used to time instruction sequences because the **RDTSC** instruction might be executed at a different time than specified in your program.</span></span> <span data-ttu-id="f321e-449">已在某些處理器上引進 **RDTSCP** 指令，以回應此問題。</span><span class="sxs-lookup"><span data-stu-id="f321e-449">The **RDTSCP** instruction has been introduced on some processors in response to this problem.</span></span>

<span data-ttu-id="f321e-450">與其他計時器一樣，TSC 是以 crystal oscillator 為基礎，其確切的頻率不事先知道，而且有頻率位移錯誤。</span><span class="sxs-lookup"><span data-stu-id="f321e-450">Like other timers, the TSC is based on a crystal oscillator whose exact frequency is not known in advance and that has a frequency offset error.</span></span> <span data-ttu-id="f321e-451">因此，在使用之前，必須使用另一個時間參考來校正。</span><span class="sxs-lookup"><span data-stu-id="f321e-451">Thus before it can be used, it must be calibrated using another timing reference.</span></span>

<span data-ttu-id="f321e-452">在系統初始化期間，Windows 會檢查 TSC 是否適用于時間用途，並執行必要的頻率校正和核心同步處理。</span><span class="sxs-lookup"><span data-stu-id="f321e-452">During system initialization, Windows checks if the TSC is suitable for timing purposes and performs the necessary frequency calibration and core synchronization.</span></span>

</dd> <dt>

<span data-ttu-id="f321e-453"><span id="PM_Clock"></span><span id="pm_clock"></span><span id="PM_CLOCK"></span>**PM 時鐘**</span><span class="sxs-lookup"><span data-stu-id="f321e-453"><span id="PM_Clock"></span><span id="pm_clock"></span><span id="PM_CLOCK"></span>**PM Clock**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-454">ACPI 計時器（也稱為 PM 時鐘）已新增至系統架構，以提供可靠的時間戳記，而不受處理器速度影響。</span><span class="sxs-lookup"><span data-stu-id="f321e-454">The ACPI timer, also known as the PM clock, was added to the system architecture to provide reliable time stamps independently of the processors speed.</span></span> <span data-ttu-id="f321e-455">因為這是此計時器的單一目標，所以它會在單一時鐘週期中提供時間戳記，但不會提供任何其他功能。</span><span class="sxs-lookup"><span data-stu-id="f321e-455">Because this was the single goal of this timer, it provides a time stamp in a single clock cycle, but it doesn't provide any other functionality.</span></span>

</dd> <dt>

<span data-ttu-id="f321e-456"><span id="HPET_Timer"></span><span id="hpet_timer"></span><span id="HPET_TIMER"></span>**HPET 計時器**</span><span class="sxs-lookup"><span data-stu-id="f321e-456"><span id="HPET_Timer"></span><span id="hpet_timer"></span><span id="HPET_TIMER"></span>**HPET Timer**</span></span>
</dt> <dd>

<span data-ttu-id="f321e-457">高精確度事件計時器 (HPET) 是由 Intel 和 Microsoft 共同開發，以符合多媒體和其他時效性應用程式的時間需求。</span><span class="sxs-lookup"><span data-stu-id="f321e-457">The High Precision Event Timer (HPET) was developed jointly by Intel and Microsoft to meet the timing requirements of multimedia and other time-sensitive applications.</span></span> <span data-ttu-id="f321e-458">Windows Vista、Windows 7 和 Windows 8 硬體標誌認證在 Windows 中一直以來都有 HPET 支援，需要硬體平臺的 HPET 支援。</span><span class="sxs-lookup"><span data-stu-id="f321e-458">HPET support has been in Windows since Windows Vista, and Windows 7 and Windows 8 Hardware Logo certification requires HPET support in the hardware platform.</span></span>

</dd> </dl>

 

 
