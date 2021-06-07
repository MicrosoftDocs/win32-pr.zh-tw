---
title: 系統提供者
description: 使用 EnableTraceEx2 啟用系統追蹤提供者的事件。
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 48a93ab94b87a43e0eb8a292320536a04ef43477
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387791"
---
# <a name="system-providers"></a><span data-ttu-id="27a88-103">系統提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-103">System Providers</span></span>
 
<span data-ttu-id="27a88-104">從 Windows 10 SDK 組建20348開始，系統追蹤提供者的事件可以使用與其他 ETW 提供者相同的方式來啟用 [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)。</span><span class="sxs-lookup"><span data-stu-id="27a88-104">Beginning in Windows 10 SDK build 20348, the System Trace Provider's events can be enabled in the same way that other ETW providers are, with [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).</span></span>  <span data-ttu-id="27a88-105">與系統追蹤提供者相關聯的不同旗標和 [群組遮罩](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) 已對應到新的追蹤提供者，稱為系統提供者和相符的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="27a88-105">The different flags and [group masks](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) associated with the System Trace Provider have been mapped to new trace providers, called System Providers, and matching keywords.</span></span>  
 
<span data-ttu-id="27a88-106">就像直接啟用系統追蹤提供者一樣，系統提供者只能由具有 [EVENT_TRACE_SYSTEM_LOGGER_MODE](/windows/win32/etw/logging-mode-constants) 設定的會話啟用。</span><span class="sxs-lookup"><span data-stu-id="27a88-106">Like enabling the System Trace Provider directly, the System Providers can only be enabled by a session with the [EVENT_TRACE_SYSTEM_LOGGER_MODE](/windows/win32/etw/logging-mode-constants) set.</span></span>

## <a name="system-provider-reference"></a><span data-ttu-id="27a88-107">系統提供者參考</span><span class="sxs-lookup"><span data-stu-id="27a88-107">System Provider reference</span></span>

* [<span data-ttu-id="27a88-108">系統 ALPC 提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-108">System ALPC Provider</span></span>](#system-alpc-provider)
* [<span data-ttu-id="27a88-109">系統設定提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-109">System Config Provider</span></span>](#system-config-provider)
* [<span data-ttu-id="27a88-110">系統 CPU 提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-110">System CPU Provider</span></span>](#system-cpu-provider)
* [<span data-ttu-id="27a88-111">系統管理者提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-111">System Hypervisor Provider</span></span>](#system-hypervisor-provider)
* [<span data-ttu-id="27a88-112">系統中斷提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-112">System Interrupt Provider</span></span>](#system-interrupt-provider)
* [<span data-ttu-id="27a88-113">系統 IO 提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-113">System IO Provider</span></span>](#system-io-provider)
* [<span data-ttu-id="27a88-114">系統 IO 篩選器提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-114">System IO Filter Provider</span></span>](#system-io-filter-provider)
* [<span data-ttu-id="27a88-115">系統鎖定提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-115">System Lock Provider</span></span>](#system-lock-provider)
* [<span data-ttu-id="27a88-116">系統記憶體提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-116">System Memory Provider</span></span>](#system-memory-provider)
* [<span data-ttu-id="27a88-117">系統物件提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-117">System Object Provider</span></span>](#system-object-provider)
* [<span data-ttu-id="27a88-118">系統電源提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-118">System Power Provider</span></span>](#system-power-provider)
* [<span data-ttu-id="27a88-119">系統進程提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-119">System Process Provider</span></span>](#system-process-provider)
* [<span data-ttu-id="27a88-120">系統設定檔提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-120">System Profile Provider</span></span>](#system-profile-provider)
* [<span data-ttu-id="27a88-121">系統登錄提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-121">System Registry Provider</span></span>](#system-registry-provider)
* [<span data-ttu-id="27a88-122">系統排程器提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-122">System Scheduler Provider</span></span>](#system-scheduler-provider)
* [<span data-ttu-id="27a88-123">系統 Syscall 提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-123">System Syscall Provider</span></span>](#system-syscall-provider)
* [<span data-ttu-id="27a88-124">系統計時器提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-124">System Timer Provider</span></span>](#system-timer-provider)
 
### <a name="system-alpc-provider"></a><span data-ttu-id="27a88-125">系統 ALPC 提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-125">System ALPC Provider</span></span>

<span data-ttu-id="27a88-126">提供與 ALPC 系統相關的事件。</span><span class="sxs-lookup"><span data-stu-id="27a88-126">Provides events related to the ALPC system.</span></span>

<span data-ttu-id="27a88-127">GUID： SystemAlpcProviderGuid {fcb9baaf-e529-4980-92e9-ced1a6aadfdf}</span><span class="sxs-lookup"><span data-stu-id="27a88-127">GUID: SystemAlpcProviderGuid {fcb9baaf-e529-4980-92e9-ced1a6aadfdf}</span></span>

| <span data-ttu-id="27a88-128">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-128">Keyword</span></span> | <span data-ttu-id="27a88-129">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-129">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-130">SYSTEM_ALPC_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="27a88-130">SYSTEM_ALPC_KW_GENERAL</span></span> | <span data-ttu-id="27a88-131">PERF_ALPC，EVENT_TRACE_FLAG_ALPC</span><span class="sxs-lookup"><span data-stu-id="27a88-131">PERF_ALPC, EVENT_TRACE_FLAG_ALPC</span></span> |
 
### <a name="system-config-provider"></a><span data-ttu-id="27a88-132">系統設定提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-132">System Config Provider</span></span> 

<span data-ttu-id="27a88-133">提供系統組態事件。</span><span class="sxs-lookup"><span data-stu-id="27a88-133">Provides system configuration events.</span></span>

<span data-ttu-id="27a88-134">GUID： SystemConfigProviderGuid {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}</span><span class="sxs-lookup"><span data-stu-id="27a88-134">GUID: SystemConfigProviderGuid {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}</span></span>

| <span data-ttu-id="27a88-135">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-135">Keyword</span></span> | <span data-ttu-id="27a88-136">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-136">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-137">SYSTEM_CONFIG_KW_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="27a88-137">SYSTEM_CONFIG_KW_SYSTEM</span></span> | <span data-ttu-id="27a88-138">PERF_SYSCFG_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="27a88-138">PERF_SYSCFG_SYSTEM</span></span> |
| <span data-ttu-id="27a88-139">SYSTEM_CONFIG_KW_GRAPHICS</span><span class="sxs-lookup"><span data-stu-id="27a88-139">SYSTEM_CONFIG_KW_GRAPHICS</span></span> | <span data-ttu-id="27a88-140">PERF_SYSCFG_GRAPHICS</span><span class="sxs-lookup"><span data-stu-id="27a88-140">PERF_SYSCFG_GRAPHICS</span></span> |
| <span data-ttu-id="27a88-141">SYSTEM_CONFIG_KW_STORAGE</span><span class="sxs-lookup"><span data-stu-id="27a88-141">SYSTEM_CONFIG_KW_STORAGE</span></span> | <span data-ttu-id="27a88-142">PERF_SYSCFG_STORAGE</span><span class="sxs-lookup"><span data-stu-id="27a88-142">PERF_SYSCFG_STORAGE</span></span> |
| <span data-ttu-id="27a88-143">SYSTEM_CONFIG_KW_NETWORK</span><span class="sxs-lookup"><span data-stu-id="27a88-143">SYSTEM_CONFIG_KW_NETWORK</span></span> | <span data-ttu-id="27a88-144">PERF_SYSCFG_NETWORK</span><span class="sxs-lookup"><span data-stu-id="27a88-144">PERF_SYSCFG_NETWORK</span></span> |
| <span data-ttu-id="27a88-145">SYSTEM_CONFIG_KW_SERVICES</span><span class="sxs-lookup"><span data-stu-id="27a88-145">SYSTEM_CONFIG_KW_SERVICES</span></span> | <span data-ttu-id="27a88-146">PERF_SYSCFG_SERVICES</span><span class="sxs-lookup"><span data-stu-id="27a88-146">PERF_SYSCFG_SERVICES</span></span> |
| <span data-ttu-id="27a88-147">SYSTEM_CONFIG_KW_PNP</span><span class="sxs-lookup"><span data-stu-id="27a88-147">SYSTEM_CONFIG_KW_PNP</span></span> | <span data-ttu-id="27a88-148">PERF_SYSCFG_PNP</span><span class="sxs-lookup"><span data-stu-id="27a88-148">PERF_SYSCFG_PNP</span></span> |
| <span data-ttu-id="27a88-149">SYSTEM_CONFIG_KW_OPTICAL</span><span class="sxs-lookup"><span data-stu-id="27a88-149">SYSTEM_CONFIG_KW_OPTICAL</span></span> | <span data-ttu-id="27a88-150">PERF_SYSCFG_OPTICAL</span><span class="sxs-lookup"><span data-stu-id="27a88-150">PERF_SYSCFG_OPTICAL</span></span> |
 
### <a name="system-cpu-provider"></a><span data-ttu-id="27a88-151">系統 CPU 提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-151">System CPU Provider</span></span> 

<span data-ttu-id="27a88-152">提供與 CPU 相關的事件。</span><span class="sxs-lookup"><span data-stu-id="27a88-152">Provides events related to the CPU.</span></span>

<span data-ttu-id="27a88-153">GUID： SystemCpuProviderGuid {c6c5265f-eae8-4650-aae4-9d48603d8510}</span><span class="sxs-lookup"><span data-stu-id="27a88-153">GUID: SystemCpuProviderGuid {c6c5265f-eae8-4650-aae4-9d48603d8510}</span></span>

| <span data-ttu-id="27a88-154">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-154">Keyword</span></span> | <span data-ttu-id="27a88-155">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-155">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-156">SYSTEM_CPU_KW_CONFIG</span><span class="sxs-lookup"><span data-stu-id="27a88-156">SYSTEM_CPU_KW_CONFIG</span></span> | <span data-ttu-id="27a88-157">PERF_CPU_CONFIG</span><span class="sxs-lookup"><span data-stu-id="27a88-157">PERF_CPU_CONFIG</span></span> |
| <span data-ttu-id="27a88-158">SYSTEM_CPU_KW_CACHE_FLUSH</span><span class="sxs-lookup"><span data-stu-id="27a88-158">SYSTEM_CPU_KW_CACHE_FLUSH</span></span> | <span data-ttu-id="27a88-159">PERF_CACHE_FLUSH</span><span class="sxs-lookup"><span data-stu-id="27a88-159">PERF_CACHE_FLUSH</span></span> |
| <span data-ttu-id="27a88-160">SYSTEM_CPU_KW_SPEC_CONTROL</span><span class="sxs-lookup"><span data-stu-id="27a88-160">SYSTEM_CPU_KW_SPEC_CONTROL</span></span> | <span data-ttu-id="27a88-161">PERF_SPEC_CONTROL</span><span class="sxs-lookup"><span data-stu-id="27a88-161">PERF_SPEC_CONTROL</span></span> |
 
### <a name="system-hypervisor-provider"></a><span data-ttu-id="27a88-162">系統管理者提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-162">System Hypervisor Provider</span></span> 

<span data-ttu-id="27a88-163">提供與管理程式相關的事件。</span><span class="sxs-lookup"><span data-stu-id="27a88-163">Provides events relating to the hypervisor.</span></span>

<span data-ttu-id="27a88-164">GUID： SystemHypervisorProviderGuid {bafa072a-918a-4bed-b622-bc152097098f}</span><span class="sxs-lookup"><span data-stu-id="27a88-164">GUID: SystemHypervisorProviderGuid {bafa072a-918a-4bed-b622-bc152097098f}</span></span>

| <span data-ttu-id="27a88-165">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-165">Keyword</span></span> | <span data-ttu-id="27a88-166">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-166">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-167">SYSTEM_HYPERVISOR_KW_PROFILE</span><span class="sxs-lookup"><span data-stu-id="27a88-167">SYSTEM_HYPERVISOR_KW_PROFILE</span></span> | <span data-ttu-id="27a88-168">PERF_HV_PROFILE</span><span class="sxs-lookup"><span data-stu-id="27a88-168">PERF_HV_PROFILE</span></span> |
| <span data-ttu-id="27a88-169">SYSTEM_HYPERVISOR_KW_CALLOUTS</span><span class="sxs-lookup"><span data-stu-id="27a88-169">SYSTEM_HYPERVISOR_KW_CALLOUTS</span></span> | <span data-ttu-id="27a88-170">PERF_HV_CALLOUTS</span><span class="sxs-lookup"><span data-stu-id="27a88-170">PERF_HV_CALLOUTS</span></span> |
| <span data-ttu-id="27a88-171">SYSTEM_HYPERVISOR_KW_VTL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="27a88-171">SYSTEM_HYPERVISOR_KW_VTL_CHANGE</span></span> | <span data-ttu-id="27a88-172">PERF_VTL_CHANGE</span><span class="sxs-lookup"><span data-stu-id="27a88-172">PERF_VTL_CHANGE</span></span> |
 
### <a name="system-interrupt-provider"></a><span data-ttu-id="27a88-173">系統中斷提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-173">System Interrupt Provider</span></span> 

<span data-ttu-id="27a88-174">提供與 Dpc 和中斷相關的事件。</span><span class="sxs-lookup"><span data-stu-id="27a88-174">Provides events relating to DPCs and interrupts.</span></span>

<span data-ttu-id="27a88-175">GUID： SystemInterruptProviderGuid {d4bbee17-b545-4888-858b-744169015b25}</span><span class="sxs-lookup"><span data-stu-id="27a88-175">GUID: SystemInterruptProviderGuid {d4bbee17-b545-4888-858b-744169015b25}</span></span>

| <span data-ttu-id="27a88-176">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-176">Keyword</span></span> | <span data-ttu-id="27a88-177">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-177">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-178">SYSTEM_INTERRUPT_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="27a88-178">SYSTEM_INTERRUPT_KW_GENERAL</span></span> | <span data-ttu-id="27a88-179">PERF_INTERRUPT，EVENT_TRACE_FLAG_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="27a88-179">PERF_INTERRUPT, EVENT_TRACE_FLAG_INTERRUPT</span></span> |
| <span data-ttu-id="27a88-180">SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="27a88-180">SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT</span></span> | <span data-ttu-id="27a88-181">PERF_CLOCK_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="27a88-181">PERF_CLOCK_INTERRUPT</span></span> |
| <span data-ttu-id="27a88-182">SYSTEM_INTERRUPT_KW_DPC</span><span class="sxs-lookup"><span data-stu-id="27a88-182">SYSTEM_INTERRUPT_KW_DPC</span></span> | <span data-ttu-id="27a88-183">PERF_DPC，EVENT_TRACE_FLAG_DPC</span><span class="sxs-lookup"><span data-stu-id="27a88-183">PERF_DPC, EVENT_TRACE_FLAG_DPC</span></span> |
| <span data-ttu-id="27a88-184">SYSTEM_INTERRUPT_KW_DPC_QUEUE</span><span class="sxs-lookup"><span data-stu-id="27a88-184">SYSTEM_INTERRUPT_KW_DPC_QUEUE</span></span> | <span data-ttu-id="27a88-185">PERF_DPC_QUEUE</span><span class="sxs-lookup"><span data-stu-id="27a88-185">PERF_DPC_QUEUE</span></span> |
| <span data-ttu-id="27a88-186">SYSTEM_INTERRUPT_KW_WDF_DPC</span><span class="sxs-lookup"><span data-stu-id="27a88-186">SYSTEM_INTERRUPT_KW_WDF_DPC</span></span> | <span data-ttu-id="27a88-187">PERF_WDF_DPC</span><span class="sxs-lookup"><span data-stu-id="27a88-187">PERF_WDF_DPC</span></span> |
| <span data-ttu-id="27a88-188">SYSTEM_INTERRUPT_KW_WDF_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="27a88-188">SYSTEM_INTERRUPT_KW_WDF_INTERRUPT</span></span> | <span data-ttu-id="27a88-189">PERF_WDF_INTERRUPT</span><span class="sxs-lookup"><span data-stu-id="27a88-189">PERF_WDF_INTERRUPT</span></span> |
| <span data-ttu-id="27a88-190">SYSTEM_INTERRUPT_KW_IPI</span><span class="sxs-lookup"><span data-stu-id="27a88-190">SYSTEM_INTERRUPT_KW_IPI</span></span> | <span data-ttu-id="27a88-191">PERF_IPI</span><span class="sxs-lookup"><span data-stu-id="27a88-191">PERF_IPI</span></span> |
 
 
### <a name="system-io-provider"></a><span data-ttu-id="27a88-192">系統 IO 提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-192">System IO Provider</span></span> 

<span data-ttu-id="27a88-193">提供與多種 IO （包括磁片、快取和網路）相關的事件。</span><span class="sxs-lookup"><span data-stu-id="27a88-193">Provides events relating to multiple kinds of IO including disk, cache, and network.</span></span>

<span data-ttu-id="27a88-194">GUID： SystemIoProviderGuid {3d5c43e3-0f1c-4202-b817-174c0070dc79}</span><span class="sxs-lookup"><span data-stu-id="27a88-194">GUID: SystemIoProviderGuid {3d5c43e3-0f1c-4202-b817-174c0070dc79}</span></span>

| <span data-ttu-id="27a88-195">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-195">Keyword</span></span> | <span data-ttu-id="27a88-196">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-196">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-197">SYSTEM_IO_KW_DISK</span><span class="sxs-lookup"><span data-stu-id="27a88-197">SYSTEM_IO_KW_DISK</span></span> | <span data-ttu-id="27a88-198">EVENT_TRACE_FLAG_DISK_IO</span><span class="sxs-lookup"><span data-stu-id="27a88-198">EVENT_TRACE_FLAG_DISK_IO</span></span> |
| <span data-ttu-id="27a88-199">SYSTEM_IO_KW_DISK_INIT</span><span class="sxs-lookup"><span data-stu-id="27a88-199">SYSTEM_IO_KW_DISK_INIT</span></span> | <span data-ttu-id="27a88-200">PERF_DISK_IO_INIT，EVENT_TRACE_FLAG_DISK_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="27a88-200">PERF_DISK_IO_INIT, EVENT_TRACE_FLAG_DISK_IO_INIT</span></span> |
| <span data-ttu-id="27a88-201">SYSTEM_IO_KW_FILENAME</span><span class="sxs-lookup"><span data-stu-id="27a88-201">SYSTEM_IO_KW_FILENAME</span></span> | <span data-ttu-id="27a88-202">PERF_FILENAME，EVENT_TRACE_FLAG_DISK_FILE_IO</span><span class="sxs-lookup"><span data-stu-id="27a88-202">PERF_FILENAME, EVENT_TRACE_FLAG_DISK_FILE_IO</span></span> |
| <span data-ttu-id="27a88-203">SYSTEM_IO_KW_SPLIT</span><span class="sxs-lookup"><span data-stu-id="27a88-203">SYSTEM_IO_KW_SPLIT</span></span> | <span data-ttu-id="27a88-204">PERF_SPLIT_IO，EVENT_TRACE_FLAG_SPLIT_IO</span><span class="sxs-lookup"><span data-stu-id="27a88-204">PERF_SPLIT_IO, EVENT_TRACE_FLAG_SPLIT_IO</span></span> |
| <span data-ttu-id="27a88-205">SYSTEM_IO_KW_FILE</span><span class="sxs-lookup"><span data-stu-id="27a88-205">SYSTEM_IO_KW_FILE</span></span> | <span data-ttu-id="27a88-206">PERF_FILE_IO，EVENT_TRACE_FLAG_FILE_IO</span><span class="sxs-lookup"><span data-stu-id="27a88-206">PERF_FILE_IO, EVENT_TRACE_FLAG_FILE_IO</span></span> |
| <span data-ttu-id="27a88-207">SYSTEM_IO_KW_OPTICAL</span><span class="sxs-lookup"><span data-stu-id="27a88-207">SYSTEM_IO_KW_OPTICAL</span></span> | <span data-ttu-id="27a88-208">PERF_OPTICAL_IO，EVENT_TRACE_FLAG_FILE_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="27a88-208">PERF_OPTICAL_IO, EVENT_TRACE_FLAG_FILE_IO_INIT</span></span> |
| <span data-ttu-id="27a88-209">SYSTEM_IO_KW_OPTICAL_INIT</span><span class="sxs-lookup"><span data-stu-id="27a88-209">SYSTEM_IO_KW_OPTICAL_INIT</span></span> | <span data-ttu-id="27a88-210">PERF_OPTICAL_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="27a88-210">PERF_OPTICAL_IO_INIT</span></span> |
| <span data-ttu-id="27a88-211">SYSTEM_IO_KW_DRIVERS</span><span class="sxs-lookup"><span data-stu-id="27a88-211">SYSTEM_IO_KW_DRIVERS</span></span> | <span data-ttu-id="27a88-212">PERF_DRIVERS，EVENT_TRACE_FLAG_DRIVER</span><span class="sxs-lookup"><span data-stu-id="27a88-212">PERF_DRIVERS, EVENT_TRACE_FLAG_DRIVER</span></span> |
| <span data-ttu-id="27a88-213">SYSTEM_IO_KW_CC</span><span class="sxs-lookup"><span data-stu-id="27a88-213">SYSTEM_IO_KW_CC</span></span> | <span data-ttu-id="27a88-214">PERF_CC</span><span class="sxs-lookup"><span data-stu-id="27a88-214">PERF_CC</span></span> |
| <span data-ttu-id="27a88-215">SYSTEM_IO_KW_NETWORK</span><span class="sxs-lookup"><span data-stu-id="27a88-215">SYSTEM_IO_KW_NETWORK</span></span> | <span data-ttu-id="27a88-216">PERF_NETWORK，EVENT_TRACE_FLAG_NETWORK_TCPIP</span><span class="sxs-lookup"><span data-stu-id="27a88-216">PERF_NETWORK, EVENT_TRACE_FLAG_NETWORK_TCPIP</span></span> |

<span data-ttu-id="27a88-217">注意：啟用 SYSTEM_IO_KW_DRIVERS 關鍵字也會自動啟用 SYSTEM_IO_KW_FILENAME。</span><span class="sxs-lookup"><span data-stu-id="27a88-217">Note: Enabling the SYSTEM_IO_KW_DRIVERS keyword will automatically enable SYSTEM_IO_KW_FILENAME as well.</span></span>  <span data-ttu-id="27a88-218">使用 SYSTEM_MEMORY_KW_MEMORY 關鍵字啟用系統記憶體提供者時，也會自動開啟 SYSTEM_IO_KW_FILENAME。</span><span class="sxs-lookup"><span data-stu-id="27a88-218">The SYSTEM_IO_KW_FILENAME is also automatically turned on when the System Memory Provider is enabled with the SYSTEM_MEMORY_KW_MEMORY keyword.</span></span>
 
### <a name="system-io-filter-provider"></a><span data-ttu-id="27a88-219">系統 IO 篩選器提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-219">System IO Filter Provider</span></span> 

<span data-ttu-id="27a88-220">提供與 IO 篩選相關的事件，包括計時和失敗。</span><span class="sxs-lookup"><span data-stu-id="27a88-220">Provides events related to IO filtering including timing and failures.</span></span>

<span data-ttu-id="27a88-221">GUID： SystemIoFilterProviderGuid {fbd09363-9e22-4661-b8bf-e7a34b535b8c}</span><span class="sxs-lookup"><span data-stu-id="27a88-221">GUID: SystemIoFilterProviderGuid {fbd09363-9e22-4661-b8bf-e7a34b535b8c}</span></span>

| <span data-ttu-id="27a88-222">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-222">Keyword</span></span> | <span data-ttu-id="27a88-223">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-223">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-224">SYSTEM_IOFILTER_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="27a88-224">SYSTEM_IOFILTER_KW_GENERAL</span></span> | <span data-ttu-id="27a88-225">PERF_FLT_IO</span><span class="sxs-lookup"><span data-stu-id="27a88-225">PERF_FLT_IO</span></span> |
| <span data-ttu-id="27a88-226">SYSTEM_IOFILTER_KW_INIT</span><span class="sxs-lookup"><span data-stu-id="27a88-226">SYSTEM_IOFILTER_KW_INIT</span></span> | <span data-ttu-id="27a88-227">PERF_FLT_IO_INIT</span><span class="sxs-lookup"><span data-stu-id="27a88-227">PERF_FLT_IO_INIT</span></span> |
| <span data-ttu-id="27a88-228">SYSTEM_IOFILTER_KW_FASTIO</span><span class="sxs-lookup"><span data-stu-id="27a88-228">SYSTEM_IOFILTER_KW_FASTIO</span></span> | <span data-ttu-id="27a88-229">PERF_FLT_FASTIO</span><span class="sxs-lookup"><span data-stu-id="27a88-229">PERF_FLT_FASTIO</span></span> |
| <span data-ttu-id="27a88-230">SYSTEM_IOFILTER_KW_FAILURE</span><span class="sxs-lookup"><span data-stu-id="27a88-230">SYSTEM_IOFILTER_KW_FAILURE</span></span> | <span data-ttu-id="27a88-231">PERF_FLT_IO_FAILURE</span><span class="sxs-lookup"><span data-stu-id="27a88-231">PERF_FLT_IO_FAILURE</span></span> |
 
### <a name="system-lock-provider"></a><span data-ttu-id="27a88-232">系統鎖定提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-232">System Lock Provider</span></span> 

<span data-ttu-id="27a88-233">提供與核心鎖定機制相關的事件。</span><span class="sxs-lookup"><span data-stu-id="27a88-233">Provides events relating to kernel locking mechanisms.</span></span>

<span data-ttu-id="27a88-234">GUID： SystemLockProviderGuid {721ddfd3-dacc-4e1e-b26a-a2cb31d4705a}</span><span class="sxs-lookup"><span data-stu-id="27a88-234">GUID: SystemLockProviderGuid {721ddfd3-dacc-4e1e-b26a-a2cb31d4705a}</span></span>

| <span data-ttu-id="27a88-235">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-235">Keyword</span></span> | <span data-ttu-id="27a88-236">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-236">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-237">SYSTEM_LOCK_KW_SPINLOCK</span><span class="sxs-lookup"><span data-stu-id="27a88-237">SYSTEM_LOCK_KW_SPINLOCK</span></span> | <span data-ttu-id="27a88-238">PERF_SPINLOCK</span><span class="sxs-lookup"><span data-stu-id="27a88-238">PERF_SPINLOCK</span></span> |
| <span data-ttu-id="27a88-239">SYSTEM_LOCK_KW_SPINLOCK_COUNTERS</span><span class="sxs-lookup"><span data-stu-id="27a88-239">SYSTEM_LOCK_KW_SPINLOCK_COUNTERS</span></span> | <span data-ttu-id="27a88-240">PERF_SPINLOCK_CNTRS</span><span class="sxs-lookup"><span data-stu-id="27a88-240">PERF_SPINLOCK_CNTRS</span></span> |
| <span data-ttu-id="27a88-241">SYSTEM_LOCK_KW_SYNC_OBJECTS</span><span class="sxs-lookup"><span data-stu-id="27a88-241">SYSTEM_LOCK_KW_SYNC_OBJECTS</span></span> | <span data-ttu-id="27a88-242">PERF_SYNC_OBJECTS</span><span class="sxs-lookup"><span data-stu-id="27a88-242">PERF_SYNC_OBJECTS</span></span> |
 
### <a name="system-memory-provider"></a><span data-ttu-id="27a88-243">系統記憶體提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-243">System Memory Provider</span></span> 

<span data-ttu-id="27a88-244">提供與記憶體管理員相關的事件。</span><span class="sxs-lookup"><span data-stu-id="27a88-244">Provides events relating to the memory manager.</span></span>

<span data-ttu-id="27a88-245">GUID： SystemMemoryProviderGuid {82958ca9-b6cd-47f8-a3a8-03ae85a4bc24}</span><span class="sxs-lookup"><span data-stu-id="27a88-245">GUID: SystemMemoryProviderGuid {82958ca9-b6cd-47f8-a3a8-03ae85a4bc24}</span></span>

| <span data-ttu-id="27a88-246">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-246">Keyword</span></span> | <span data-ttu-id="27a88-247">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-247">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-248">SYSTEM_MEMORY_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="27a88-248">SYSTEM_MEMORY_KW_GENERAL</span></span> | <span data-ttu-id="27a88-249">PERF_MEMORY</span><span class="sxs-lookup"><span data-stu-id="27a88-249">PERF_MEMORY</span></span> |
| <span data-ttu-id="27a88-250">SYSTEM_MEMORY_KW_HARD_FAULTS</span><span class="sxs-lookup"><span data-stu-id="27a88-250">SYSTEM_MEMORY_KW_HARD_FAULTS</span></span> | <span data-ttu-id="27a88-251">PERF_HARD_FAULTS，EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS</span><span class="sxs-lookup"><span data-stu-id="27a88-251">PERF_HARD_FAULTS, EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS</span></span> |
| <span data-ttu-id="27a88-252">SYSTEM_MEMORY_KW_ALL_FAULTS</span><span class="sxs-lookup"><span data-stu-id="27a88-252">SYSTEM_MEMORY_KW_ALL_FAULTS</span></span> | <span data-ttu-id="27a88-253">PERF_ALL_FAULTS，EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS</span><span class="sxs-lookup"><span data-stu-id="27a88-253">PERF_ALL_FAULTS, EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS</span></span> |
| <span data-ttu-id="27a88-254">SYSTEM_MEMORY_KW_POOL</span><span class="sxs-lookup"><span data-stu-id="27a88-254">SYSTEM_MEMORY_KW_POOL</span></span> | <span data-ttu-id="27a88-255">PERF_POOL</span><span class="sxs-lookup"><span data-stu-id="27a88-255">PERF_POOL</span></span> |
| <span data-ttu-id="27a88-256">SYSTEM_MEMORY_KW_MEMINFO</span><span class="sxs-lookup"><span data-stu-id="27a88-256">SYSTEM_MEMORY_KW_MEMINFO</span></span> | <span data-ttu-id="27a88-257">PERF_MEMINFO</span><span class="sxs-lookup"><span data-stu-id="27a88-257">PERF_MEMINFO</span></span> |
| <span data-ttu-id="27a88-258">SYSTEM_MEMORY_KW_PFSECTION</span><span class="sxs-lookup"><span data-stu-id="27a88-258">SYSTEM_MEMORY_KW_PFSECTION</span></span> | <span data-ttu-id="27a88-259">PERF_PFSECTION</span><span class="sxs-lookup"><span data-stu-id="27a88-259">PERF_PFSECTION</span></span> |
| <span data-ttu-id="27a88-260">SYSTEM_MEMORY_KW_MEMINFO_WS</span><span class="sxs-lookup"><span data-stu-id="27a88-260">SYSTEM_MEMORY_KW_MEMINFO_WS</span></span> | <span data-ttu-id="27a88-261">PERF_MEMINFO_WS</span><span class="sxs-lookup"><span data-stu-id="27a88-261">PERF_MEMINFO_WS</span></span> |
| <span data-ttu-id="27a88-262">SYSTEM_MEMORY_KW_HEAP</span><span class="sxs-lookup"><span data-stu-id="27a88-262">SYSTEM_MEMORY_KW_HEAP</span></span> | <span data-ttu-id="27a88-263">PERF_HEAP</span><span class="sxs-lookup"><span data-stu-id="27a88-263">PERF_HEAP</span></span> |
| <span data-ttu-id="27a88-264">SYSTEM_MEMORY_KW_WS</span><span class="sxs-lookup"><span data-stu-id="27a88-264">SYSTEM_MEMORY_KW_WS</span></span> | <span data-ttu-id="27a88-265">PERF_WS</span><span class="sxs-lookup"><span data-stu-id="27a88-265">PERF_WS</span></span> |
| <span data-ttu-id="27a88-266">SYSTEM_MEMORY_KW_CONTMEM_GEN</span><span class="sxs-lookup"><span data-stu-id="27a88-266">SYSTEM_MEMORY_KW_CONTMEM_GEN</span></span> | <span data-ttu-id="27a88-267">PERF_CONTMEM_GEN</span><span class="sxs-lookup"><span data-stu-id="27a88-267">PERF_CONTMEM_GEN</span></span> |
| <span data-ttu-id="27a88-268">SYSTEM_MEMORY_KW_VIRTUAL_ALLOC</span><span class="sxs-lookup"><span data-stu-id="27a88-268">SYSTEM_MEMORY_KW_VIRTUAL_ALLOC</span></span> | <span data-ttu-id="27a88-269">PERF_VIRTUAL_ALLOC，EVENT_TRACE_FLAG_VIRTUAL_ALLOC</span><span class="sxs-lookup"><span data-stu-id="27a88-269">PERF_VIRTUAL_ALLOC, EVENT_TRACE_FLAG_VIRTUAL_ALLOC</span></span> |
| <span data-ttu-id="27a88-270">SYSTEM_MEMORY_KW_FOOTPRINT</span><span class="sxs-lookup"><span data-stu-id="27a88-270">SYSTEM_MEMORY_KW_FOOTPRINT</span></span> | <span data-ttu-id="27a88-271">PERF_FOOTPRINT</span><span class="sxs-lookup"><span data-stu-id="27a88-271">PERF_FOOTPRINT</span></span> |
| <span data-ttu-id="27a88-272">SYSTEM_MEMORY_KW_SESSION</span><span class="sxs-lookup"><span data-stu-id="27a88-272">SYSTEM_MEMORY_KW_SESSION</span></span> | <span data-ttu-id="27a88-273">PERF_SESSION</span><span class="sxs-lookup"><span data-stu-id="27a88-273">PERF_SESSION</span></span> |
| <span data-ttu-id="27a88-274">SYSTEM_MEMORY_KW_REFSET</span><span class="sxs-lookup"><span data-stu-id="27a88-274">SYSTEM_MEMORY_KW_REFSET</span></span> | <span data-ttu-id="27a88-275">PERF_REFSET</span><span class="sxs-lookup"><span data-stu-id="27a88-275">PERF_REFSET</span></span> |
| <span data-ttu-id="27a88-276">SYSTEM_MEMORY_KW_VAMAP</span><span class="sxs-lookup"><span data-stu-id="27a88-276">SYSTEM_MEMORY_KW_VAMAP</span></span> | <span data-ttu-id="27a88-277">PERF_VAMAP，EVENT_TRACE_FLAG_VAMAP</span><span class="sxs-lookup"><span data-stu-id="27a88-277">PERF_VAMAP, EVENT_TRACE_FLAG_VAMAP</span></span> |

<span data-ttu-id="27a88-278">注意：</span><span class="sxs-lookup"><span data-stu-id="27a88-278">Notes:</span></span> 
* <span data-ttu-id="27a88-279">啟用 SYSTEM_MEMORY_KW_MEMORY 關鍵字也會自動啟用系統 IO 提供者的 SYSTEM_IO_KW_FILENAME。</span><span class="sxs-lookup"><span data-stu-id="27a88-279">Enabling the SYSTEM_MEMORY_KW_MEMORY keyword will automatically enable SYSTEM_IO_KW_FILENAME on the System IO Provider as well.</span></span>
* <span data-ttu-id="27a88-280">SYSTEM_MEMORY_KW_POOL 啟用的事件支援集區標籤篩選，以選擇性地只針對特定集區標記寫入事件。</span><span class="sxs-lookup"><span data-stu-id="27a88-280">The events enabled by the SYSTEM_MEMORY_KW_POOL support a Pool Tag Filter, to selectively write events only for certain pool tags.</span></span>  <span data-ttu-id="27a88-281">這會設定為系統記憶體提供者的 [架構化篩選](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) 。</span><span class="sxs-lookup"><span data-stu-id="27a88-281">This is configured as a [Schematized Filter](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) on the System Memory Provider.</span></span>  <span data-ttu-id="27a88-282">PoolTag 篩選器的結構如下所示：</span><span class="sxs-lookup"><span data-stu-id="27a88-282">The PoolTag filter is constructed as follows:</span></span>

    ```cpp
    {
    EVENT_FILTER_HEADER Header; 
    ULONG PoolTags[ETW_MAX_POOLTAG_FILTER];
    }
    ```

* <span data-ttu-id="27a88-283">[EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header)應以設定為 SYSTEM_MEMORY_POOL_FILTER_ID 的識別碼進行初始化，而 size 欄位設定為標頭大小加上 PoolTags 陣列的使用部分。</span><span class="sxs-lookup"><span data-stu-id="27a88-283">The [EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header) should be initialized with Id set to SYSTEM_MEMORY_POOL_FILTER_ID and the size field set to the size of Header plus the used portion of the PoolTags array.</span></span>  

* <span data-ttu-id="27a88-284">每個集區標籤是在篩選中儲存為 ULONG 的4個字元字串。</span><span class="sxs-lookup"><span data-stu-id="27a88-284">Each Pool Tag is a 4 character string that is stored as a ULONG in the filter.</span></span>  
 
 
### <a name="system-object-provider"></a><span data-ttu-id="27a88-285">系統物件提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-285">System Object Provider</span></span> 

<span data-ttu-id="27a88-286">提供與物件管理員相關的事件。</span><span class="sxs-lookup"><span data-stu-id="27a88-286">Provides events relating to the Object Manager.</span></span>

<span data-ttu-id="27a88-287">GUID： SystemObjectProviderGuid {febd7460-3d1d-47eb-af49-c9eeb1e146f2}</span><span class="sxs-lookup"><span data-stu-id="27a88-287">GUID: SystemObjectProviderGuid {febd7460-3d1d-47eb-af49-c9eeb1e146f2}</span></span>

| <span data-ttu-id="27a88-288">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-288">Keyword</span></span> | <span data-ttu-id="27a88-289">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-289">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-290">SYSTEM_OBJECT_KW_HANDLE</span><span class="sxs-lookup"><span data-stu-id="27a88-290">SYSTEM_OBJECT_KW_HANDLE</span></span> | <span data-ttu-id="27a88-291">PERF_OB_HANDLE</span><span class="sxs-lookup"><span data-stu-id="27a88-291">PERF_OB_HANDLE</span></span> |
| <span data-ttu-id="27a88-292">SYSTEM_OBJECT_KW_OBJECT</span><span class="sxs-lookup"><span data-stu-id="27a88-292">SYSTEM_OBJECT_KW_OBJECT</span></span> | <span data-ttu-id="27a88-293">PERF_OB_OBJECT</span><span class="sxs-lookup"><span data-stu-id="27a88-293">PERF_OB_OBJECT</span></span> |
 
### <a name="system-power-provider"></a><span data-ttu-id="27a88-294">系統電源提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-294">System Power Provider</span></span> 

<span data-ttu-id="27a88-295">提供與系統電源狀態相關的事件。</span><span class="sxs-lookup"><span data-stu-id="27a88-295">Provides events relating to the system's power state.</span></span>

<span data-ttu-id="27a88-296">GUID： SystemPowerProviderGuid {c134884a-32d5-4488-80e5-14ed7abb8269}</span><span class="sxs-lookup"><span data-stu-id="27a88-296">GUID: SystemPowerProviderGuid {c134884a-32d5-4488-80e5-14ed7abb8269}</span></span>

| <span data-ttu-id="27a88-297">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-297">Keyword</span></span> | <span data-ttu-id="27a88-298">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-298">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-299">SYSTEM_POWER_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="27a88-299">SYSTEM_POWER_KW_GENERAL</span></span> | <span data-ttu-id="27a88-300">PERF_POWER</span><span class="sxs-lookup"><span data-stu-id="27a88-300">PERF_POWER</span></span> |
| <span data-ttu-id="27a88-301">SYSTEM_POWER_KW_HIBER_RUNDOWN</span><span class="sxs-lookup"><span data-stu-id="27a88-301">SYSTEM_POWER_KW_HIBER_RUNDOWN</span></span> | <span data-ttu-id="27a88-302">PERF_HIBER_RUNDOWN</span><span class="sxs-lookup"><span data-stu-id="27a88-302">PERF_HIBER_RUNDOWN</span></span> |
| <span data-ttu-id="27a88-303">SYSTEM_POWER_KW_PROCESSOR_IDLE</span><span class="sxs-lookup"><span data-stu-id="27a88-303">SYSTEM_POWER_KW_PROCESSOR_IDLE</span></span> | <span data-ttu-id="27a88-304">PERF_PROCESSOR_IDLE</span><span class="sxs-lookup"><span data-stu-id="27a88-304">PERF_PROCESSOR_IDLE</span></span> |
| <span data-ttu-id="27a88-305">SYSTEM_POWER_KW_IDLE_SELECTION</span><span class="sxs-lookup"><span data-stu-id="27a88-305">SYSTEM_POWER_KW_IDLE_SELECTION</span></span> | <span data-ttu-id="27a88-306">PERF_IDLE_SELECTION</span><span class="sxs-lookup"><span data-stu-id="27a88-306">PERF_IDLE_SELECTION</span></span> |
| <span data-ttu-id="27a88-307">SYSTEM_POWER_KW_PPM_EXIT_LATENCY</span><span class="sxs-lookup"><span data-stu-id="27a88-307">SYSTEM_POWER_KW_PPM_EXIT_LATENCY</span></span> | <span data-ttu-id="27a88-308">PERF_PPM_EXIT_LATENCY</span><span class="sxs-lookup"><span data-stu-id="27a88-308">PERF_PPM_EXIT_LATENCY</span></span> |
 
### <a name="system-process-provider"></a><span data-ttu-id="27a88-309">系統進程提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-309">System Process Provider</span></span> 

<span data-ttu-id="27a88-310">提供與進程相關的事件，包括存留期資訊、影像載入事件，以及執行緒相關事件。</span><span class="sxs-lookup"><span data-stu-id="27a88-310">Provides events relating to the process, including lifetime information, image load events, and thread related events.</span></span>

<span data-ttu-id="27a88-311">GUID： SystemProcessProviderGuid {151f55dc-467d-471f-83b5-5f889d46ff66}</span><span class="sxs-lookup"><span data-stu-id="27a88-311">GUID: SystemProcessProviderGuid {151f55dc-467d-471f-83b5-5f889d46ff66}</span></span>

| <span data-ttu-id="27a88-312">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-312">Keyword</span></span> | <span data-ttu-id="27a88-313">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-313">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-314">SYSTEM_PROCESS_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="27a88-314">SYSTEM_PROCESS_KW_GENERAL</span></span> | <span data-ttu-id="27a88-315">PERF_PROCESS，EVENT_TRACE_FLAG_PROCESS</span><span class="sxs-lookup"><span data-stu-id="27a88-315">PERF_PROCESS, EVENT_TRACE_FLAG_PROCESS</span></span> |
| <span data-ttu-id="27a88-316">SYSTEM_PROCESS_KW_INSWAP</span><span class="sxs-lookup"><span data-stu-id="27a88-316">SYSTEM_PROCESS_KW_INSWAP</span></span> | <span data-ttu-id="27a88-317">PERF_PROCESS_INSWAP</span><span class="sxs-lookup"><span data-stu-id="27a88-317">PERF_PROCESS_INSWAP</span></span> |
| <span data-ttu-id="27a88-318">SYSTEM_PROCESS_KW_FREEZE</span><span class="sxs-lookup"><span data-stu-id="27a88-318">SYSTEM_PROCESS_KW_FREEZE</span></span> | <span data-ttu-id="27a88-319">PERF_PROCESS_FREEZE</span><span class="sxs-lookup"><span data-stu-id="27a88-319">PERF_PROCESS_FREEZE</span></span> |
| <span data-ttu-id="27a88-320">SYSTEM_PROCESS_KW_PERF_COUNTER</span><span class="sxs-lookup"><span data-stu-id="27a88-320">SYSTEM_PROCESS_KW_PERF_COUNTER</span></span> | <span data-ttu-id="27a88-321">PERF_PERF_COUNTER，EVENT_TRACE_FLAG_PROCESS_COUNTERS</span><span class="sxs-lookup"><span data-stu-id="27a88-321">PERF_PERF_COUNTER, EVENT_TRACE_FLAG_PROCESS_COUNTERS</span></span> |
| <span data-ttu-id="27a88-322">SYSTEM_PROCESS_KW_WAKE_COUNTER</span><span class="sxs-lookup"><span data-stu-id="27a88-322">SYSTEM_PROCESS_KW_WAKE_COUNTER</span></span> | <span data-ttu-id="27a88-323">PERF_WAKE_COUNTER</span><span class="sxs-lookup"><span data-stu-id="27a88-323">PERF_WAKE_COUNTER</span></span> |
| <span data-ttu-id="27a88-324">SYSTEM_PROCESS_KW_WAKE_DROP</span><span class="sxs-lookup"><span data-stu-id="27a88-324">SYSTEM_PROCESS_KW_WAKE_DROP</span></span> | <span data-ttu-id="27a88-325">PERF_WAKE_DROP</span><span class="sxs-lookup"><span data-stu-id="27a88-325">PERF_WAKE_DROP</span></span> |
| <span data-ttu-id="27a88-326">SYSTEM_PROCESS_KW_WAKE_EVENT</span><span class="sxs-lookup"><span data-stu-id="27a88-326">SYSTEM_PROCESS_KW_WAKE_EVENT</span></span> | <span data-ttu-id="27a88-327">PERF_WAKE_EVENT</span><span class="sxs-lookup"><span data-stu-id="27a88-327">PERF_WAKE_EVENT</span></span> |
| <span data-ttu-id="27a88-328">SYSTEM_PROCESS_KW_DEBUG_EVENTS</span><span class="sxs-lookup"><span data-stu-id="27a88-328">SYSTEM_PROCESS_KW_DEBUG_EVENTS</span></span> | <span data-ttu-id="27a88-329">PERF_DEBUG_EVENTS，EVENT_TRACE_FLAG_DEBUG_EVENTS</span><span class="sxs-lookup"><span data-stu-id="27a88-329">PERF_DEBUG_EVENTS, EVENT_TRACE_FLAG_DEBUG_EVENTS</span></span> |
| <span data-ttu-id="27a88-330">SYSTEM_PROCESS_KW_DBGPRINT</span><span class="sxs-lookup"><span data-stu-id="27a88-330">SYSTEM_PROCESS_KW_DBGPRINT</span></span> | <span data-ttu-id="27a88-331">PERF_DBGPRINT，EVENT_TRACE_FLAG_DBGPRINT</span><span class="sxs-lookup"><span data-stu-id="27a88-331">PERF_DBGPRINT, EVENT_TRACE_FLAG_DBGPRINT</span></span> |
| <span data-ttu-id="27a88-332">SYSTEM_PROCESS_KW_JOB</span><span class="sxs-lookup"><span data-stu-id="27a88-332">SYSTEM_PROCESS_KW_JOB</span></span> | <span data-ttu-id="27a88-333">PERF_JOB，EVENT_TRACE_FLAG_JOB</span><span class="sxs-lookup"><span data-stu-id="27a88-333">PERF_JOB, EVENT_TRACE_FLAG_JOB</span></span> |
| <span data-ttu-id="27a88-334">SYSTEM_PROCESS_KW_WORKER_THREAD</span><span class="sxs-lookup"><span data-stu-id="27a88-334">SYSTEM_PROCESS_KW_WORKER_THREAD</span></span> | <span data-ttu-id="27a88-335">PERF_WORKER_THREAD</span><span class="sxs-lookup"><span data-stu-id="27a88-335">PERF_WORKER_THREAD</span></span> |
| <span data-ttu-id="27a88-336">SYSTEM_PROCESS_KW_THREAD</span><span class="sxs-lookup"><span data-stu-id="27a88-336">SYSTEM_PROCESS_KW_THREAD</span></span> | <span data-ttu-id="27a88-337">PERF_THREAD，EVENT_TRACE_FLAG_THREAD</span><span class="sxs-lookup"><span data-stu-id="27a88-337">PERF_THREAD, EVENT_TRACE_FLAG_THREAD</span></span> |
| <span data-ttu-id="27a88-338">SYSTEM_PROCESS_KW_LOADER</span><span class="sxs-lookup"><span data-stu-id="27a88-338">SYSTEM_PROCESS_KW_LOADER</span></span> | <span data-ttu-id="27a88-339">PERF_LOADER，EVENT_TRACE_FLAG_IMAGE_LOAD</span><span class="sxs-lookup"><span data-stu-id="27a88-339">PERF_LOADER, EVENT_TRACE_FLAG_IMAGE_LOAD</span></span> |
 
### <a name="system-profile-provider"></a><span data-ttu-id="27a88-340">系統設定檔提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-340">System Profile Provider</span></span> 

<span data-ttu-id="27a88-341">提供分析事件。</span><span class="sxs-lookup"><span data-stu-id="27a88-341">Provides profiling events.</span></span>

<span data-ttu-id="27a88-342">GUID： SystemProfileProviderGuid {bfeb0324-1cee-496f-a409-2ac2b48a6322}</span><span class="sxs-lookup"><span data-stu-id="27a88-342">GUID: SystemProfileProviderGuid {bfeb0324-1cee-496f-a409-2ac2b48a6322}</span></span>

| <span data-ttu-id="27a88-343">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-343">Keyword</span></span> | <span data-ttu-id="27a88-344">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-344">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-345">SYSTEM_PROFILE_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="27a88-345">SYSTEM_PROFILE_KW_GENERAL</span></span> | <span data-ttu-id="27a88-346">PERF_PROFILE，EVENT_TRACE_FLAG_PROFILE</span><span class="sxs-lookup"><span data-stu-id="27a88-346">PERF_PROFILE, EVENT_TRACE_FLAG_PROFILE</span></span> |
| <span data-ttu-id="27a88-347">SYSTEM_PROFILE_KW_PMC_PROFILE</span><span class="sxs-lookup"><span data-stu-id="27a88-347">SYSTEM_PROFILE_KW_PMC_PROFILE</span></span> | <span data-ttu-id="27a88-348">PERF_PMC_PROFILE</span><span class="sxs-lookup"><span data-stu-id="27a88-348">PERF_PMC_PROFILE</span></span> |
 
### <a name="system-registry-provider"></a><span data-ttu-id="27a88-349">系統登錄提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-349">System Registry Provider</span></span> 

<span data-ttu-id="27a88-350">提供與登錄相關的事件。</span><span class="sxs-lookup"><span data-stu-id="27a88-350">Provides events relating to the registry.</span></span>

<span data-ttu-id="27a88-351">GUID： SystemRegistryProviderGuid {16156bd9-fab4-4cfa-a232-89d1099058e3}</span><span class="sxs-lookup"><span data-stu-id="27a88-351">GUID: SystemRegistryProviderGuid {16156bd9-fab4-4cfa-a232-89d1099058e3}</span></span>

| <span data-ttu-id="27a88-352">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-352">Keyword</span></span> | <span data-ttu-id="27a88-353">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-353">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-354">SYSTEM_REGISTRY_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="27a88-354">SYSTEM_REGISTRY_KW_GENERAL</span></span> | <span data-ttu-id="27a88-355">PERF_REGISTRY，EVENT_TRACE_FLAG_REGISTRY</span><span class="sxs-lookup"><span data-stu-id="27a88-355">PERF_REGISTRY, EVENT_TRACE_FLAG_REGISTRY</span></span> |
| <span data-ttu-id="27a88-356">SYSTEM_REGISTRY_KW_HIVE</span><span class="sxs-lookup"><span data-stu-id="27a88-356">SYSTEM_REGISTRY_KW_HIVE</span></span> | <span data-ttu-id="27a88-357">PERF_REG_HIVE</span><span class="sxs-lookup"><span data-stu-id="27a88-357">PERF_REG_HIVE</span></span> |
| <span data-ttu-id="27a88-358">SYSTEM_REGISTRY_KW_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="27a88-358">SYSTEM_REGISTRY_KW_NOTIFICATION</span></span> | <span data-ttu-id="27a88-359">PERF_REG_NOTIF</span><span class="sxs-lookup"><span data-stu-id="27a88-359">PERF_REG_NOTIF</span></span> |
 
### <a name="system-scheduler-provider"></a><span data-ttu-id="27a88-360">系統排程器提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-360">System Scheduler Provider</span></span> 

<span data-ttu-id="27a88-361">提供與排程器相關的事件。</span><span class="sxs-lookup"><span data-stu-id="27a88-361">Provides events relating to the scheduler.</span></span>

<span data-ttu-id="27a88-362">GUID： SystemSchedulerProviderGuid {599a2a76-4d91-4910-9ac7-7d33f2e97a6c}</span><span class="sxs-lookup"><span data-stu-id="27a88-362">GUID: SystemSchedulerProviderGuid {599a2a76-4d91-4910-9ac7-7d33f2e97a6c}</span></span>

| <span data-ttu-id="27a88-363">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-363">Keyword</span></span> | <span data-ttu-id="27a88-364">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-364">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-365">SYSTEM_SCHEDULER_KW_XSCHEDULER</span><span class="sxs-lookup"><span data-stu-id="27a88-365">SYSTEM_SCHEDULER_KW_XSCHEDULER</span></span> | <span data-ttu-id="27a88-366">PERF_XSCHEDULER</span><span class="sxs-lookup"><span data-stu-id="27a88-366">PERF_XSCHEDULER</span></span> |
| <span data-ttu-id="27a88-367">SYSTEM_SCHEDULER_KW_DISPATCHER</span><span class="sxs-lookup"><span data-stu-id="27a88-367">SYSTEM_SCHEDULER_KW_DISPATCHER</span></span> | <span data-ttu-id="27a88-368">PERF_DISPATCHER，EVENT_TRACE_FLAG_DISPATCHER</span><span class="sxs-lookup"><span data-stu-id="27a88-368">PERF_DISPATCHER, EVENT_TRACE_FLAG_DISPATCHER</span></span> |
| <span data-ttu-id="27a88-369">SYSTEM_SCHEDULER_KW_KERNEL_QUEUE</span><span class="sxs-lookup"><span data-stu-id="27a88-369">SYSTEM_SCHEDULER_KW_KERNEL_QUEUE</span></span> | <span data-ttu-id="27a88-370">PERF_KERNEL_QUEUE</span><span class="sxs-lookup"><span data-stu-id="27a88-370">PERF_KERNEL_QUEUE</span></span> |
| <span data-ttu-id="27a88-371">SYSTEM_SCHEDULER_KW_SHOULD_YIELD</span><span class="sxs-lookup"><span data-stu-id="27a88-371">SYSTEM_SCHEDULER_KW_SHOULD_YIELD</span></span> | <span data-ttu-id="27a88-372">PERF_SHOULD_YIELD</span><span class="sxs-lookup"><span data-stu-id="27a88-372">PERF_SHOULD_YIELD</span></span> |
| <span data-ttu-id="27a88-373">SYSTEM_SCHEDULER_KW_ANTI_STAR加值稅ION</span><span class="sxs-lookup"><span data-stu-id="27a88-373">SYSTEM_SCHEDULER_KW_ANTI_STARVATION</span></span> | <span data-ttu-id="27a88-374">PERF_ANTI_STAR加值稅ION</span><span class="sxs-lookup"><span data-stu-id="27a88-374">PERF_ANTI_STARVATION</span></span> |
| <span data-ttu-id="27a88-375">SYSTEM_SCHEDULER_KW_LOAD_BALANCER</span><span class="sxs-lookup"><span data-stu-id="27a88-375">SYSTEM_SCHEDULER_KW_LOAD_BALANCER</span></span> | <span data-ttu-id="27a88-376">PERF_LOAD_BALANCER</span><span class="sxs-lookup"><span data-stu-id="27a88-376">PERF_LOAD_BALANCER</span></span> |
| <span data-ttu-id="27a88-377">SYSTEM_SCHEDULER_KW_AFFINITY</span><span class="sxs-lookup"><span data-stu-id="27a88-377">SYSTEM_SCHEDULER_KW_AFFINITY</span></span> | <span data-ttu-id="27a88-378">PERF_AFFINITY</span><span class="sxs-lookup"><span data-stu-id="27a88-378">PERF_AFFINITY</span></span> |
| <span data-ttu-id="27a88-379">SYSTEM_SCHEDULER_KW_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="27a88-379">SYSTEM_SCHEDULER_KW_PRIORITY</span></span> | <span data-ttu-id="27a88-380">PERF_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="27a88-380">PERF_PRIORITY</span></span> |
| <span data-ttu-id="27a88-381">SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="27a88-381">SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR</span></span> | <span data-ttu-id="27a88-382">PERF_IDEAL_PROCESSOR</span><span class="sxs-lookup"><span data-stu-id="27a88-382">PERF_IDEAL_PROCESSOR</span></span> |
| <span data-ttu-id="27a88-383">SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH</span><span class="sxs-lookup"><span data-stu-id="27a88-383">SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH</span></span> | <span data-ttu-id="27a88-384">PERF_CONTEXT_SWITCH，EVENT_TRACE_FLAG_CSWITCH</span><span class="sxs-lookup"><span data-stu-id="27a88-384">PERF_CONTEXT_SWITCH, EVENT_TRACE_FLAG_CSWITCH</span></span> |
 
### <a name="system-syscall-provider"></a><span data-ttu-id="27a88-385">系統 Syscall 提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-385">System Syscall Provider</span></span> 

<span data-ttu-id="27a88-386">提供事件與系統呼叫相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="27a88-386">Provides events with information about system calls.</span></span>

<span data-ttu-id="27a88-387">GUID： SystemSyscallProviderGuid {434286f7-6f1b-45bb-b37e-95f623046c7c}</span><span class="sxs-lookup"><span data-stu-id="27a88-387">GUID: SystemSyscallProviderGuid {434286f7-6f1b-45bb-b37e-95f623046c7c}</span></span>

| <span data-ttu-id="27a88-388">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-388">Keyword</span></span> | <span data-ttu-id="27a88-389">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-389">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-390">SYSTEM_SYSCALL_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="27a88-390">SYSTEM_SYSCALL_KW_GENERAL</span></span> | <span data-ttu-id="27a88-391">PERF_SYSCALL，EVENT_TRACE_FLAG_SYSTEMCALL</span><span class="sxs-lookup"><span data-stu-id="27a88-391">PERF_SYSCALL, EVENT_TRACE_FLAG_SYSTEMCALL</span></span> |
 
### <a name="system-timer-provider"></a><span data-ttu-id="27a88-392">系統計時器提供者</span><span class="sxs-lookup"><span data-stu-id="27a88-392">System Timer Provider</span></span> 

<span data-ttu-id="27a88-393">提供與核心中計時器相關的事件。</span><span class="sxs-lookup"><span data-stu-id="27a88-393">Provides events relating to timers in the kernel.</span></span>

<span data-ttu-id="27a88-394">GUID： SystemTimerProviderGuid {4f061568-e215-499f-ab2e-eda0ae890a5b}</span><span class="sxs-lookup"><span data-stu-id="27a88-394">GUID: SystemTimerProviderGuid {4f061568-e215-499f-ab2e-eda0ae890a5b}</span></span>

| <span data-ttu-id="27a88-395">關鍵字</span><span class="sxs-lookup"><span data-stu-id="27a88-395">Keyword</span></span> | <span data-ttu-id="27a88-396">對應的舊版旗標和群組</span><span class="sxs-lookup"><span data-stu-id="27a88-396">Corresponding Legacy Flags and Groups</span></span> |
| ------- | ------------------------------------- |
| <span data-ttu-id="27a88-397">SYSTEM_TIMER_KW_GENERAL</span><span class="sxs-lookup"><span data-stu-id="27a88-397">SYSTEM_TIMER_KW_GENERAL</span></span> | <span data-ttu-id="27a88-398">PERF_TIMER</span><span class="sxs-lookup"><span data-stu-id="27a88-398">PERF_TIMER</span></span> |
| <span data-ttu-id="27a88-399">SYSTEM_TIMER_KW_CLOCK_TIMER</span><span class="sxs-lookup"><span data-stu-id="27a88-399">SYSTEM_TIMER_KW_CLOCK_TIMER</span></span> | <span data-ttu-id="27a88-400">PERF_CLOCK_TIMER</span><span class="sxs-lookup"><span data-stu-id="27a88-400">PERF_CLOCK_TIMER</span></span> |
 
## <a name="remarks"></a><span data-ttu-id="27a88-401">備註</span><span class="sxs-lookup"><span data-stu-id="27a88-401">Remarks</span></span>

<span data-ttu-id="27a88-402">這項新的啟用機制，除了預先存在用來啟用這些事件的方法之外。</span><span class="sxs-lookup"><span data-stu-id="27a88-402">This new enablement mechanism is in addition to the pre-existing methods for enabling these events.</span></span>  <span data-ttu-id="27a88-403">任何使用的程式碼都將繼續執行此作業。</span><span class="sxs-lookup"><span data-stu-id="27a88-403">Any code that used to work, will continue to do so.</span></span>
 
<span data-ttu-id="27a88-404">由於這項新功能，系統追蹤提供者所產生的事件不會變更。</span><span class="sxs-lookup"><span data-stu-id="27a88-404">The events generated by the System Trace Provider are not changing due to this new feature.</span></span>  <span data-ttu-id="27a88-405">這表示輸出的事件未標示為從個別系統提供者發出。</span><span class="sxs-lookup"><span data-stu-id="27a88-405">This means that the outputted events are not marked as being emitted from the individual system providers.</span></span>
 
<span data-ttu-id="27a88-406">如需提供者 GUID 和關鍵字定義的詳細資訊，請參閱[evntrace。](/windows/win32/api/evntrace/)</span><span class="sxs-lookup"><span data-stu-id="27a88-406">For more information on provider GUID and keyword definitions see [evntrace.h](/windows/win32/api/evntrace/).</span></span>

## <a name="see-also"></a><span data-ttu-id="27a88-407">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27a88-407">See Also</span></span>

[<span data-ttu-id="27a88-408">設定並啟動 SystemTraceProvider 會話</span><span class="sxs-lookup"><span data-stu-id="27a88-408">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)

[<span data-ttu-id="27a88-409">evntrace .h 標頭</span><span class="sxs-lookup"><span data-stu-id="27a88-409">evntrace.h header</span></span>](/windows/win32/api/evntrace/)