---
description: 本主題列出 (UMS) 的進程、執行緒、處理器、工作物件和使用者模式排程使用的結構。
ms.assetid: dbb50193-4c67-494e-9c46-2ac3106fac9a
title: 進程和執行緒結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59b2b4a8209c3f1f9fb3163c849fa2c229d2bdf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996732"
---
# <a name="process-and-thread-structures"></a><span data-ttu-id="19f4f-103">進程和執行緒結構</span><span class="sxs-lookup"><span data-stu-id="19f4f-103">Process and Thread Structures</span></span>

<span data-ttu-id="19f4f-104">本主題列出 (UMS) 的進程、執行緒、處理器、工作物件和使用者模式排程使用的結構。</span><span class="sxs-lookup"><span data-stu-id="19f4f-104">This topic lists structures that are used with processes, threads, processors, job objects, and user-mode scheduling (UMS).</span></span>

## <a name="process-and-thread-structures"></a><span data-ttu-id="19f4f-105">進程和執行緒結構</span><span class="sxs-lookup"><span data-stu-id="19f4f-105">Process and Thread Structures</span></span>

<span data-ttu-id="19f4f-106">下列結構適用于處理常式和執行緒：</span><span class="sxs-lookup"><span data-stu-id="19f4f-106">The following structures are used with processes and threads:</span></span>

-   [<span data-ttu-id="19f4f-107">**應用程式 \_ 記憶體 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="19f4f-107">**APP\_MEMORY\_INFORMATION**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [<span data-ttu-id="19f4f-108">**AR \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="19f4f-108">**AR\_STATE**</span></span>](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [<span data-ttu-id="19f4f-109">**快取 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="19f4f-109">**CACHE\_DESCRIPTOR**</span></span>](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [<span data-ttu-id="19f4f-110">**IO \_ 計數器**</span><span class="sxs-lookup"><span data-stu-id="19f4f-110">**IO\_COUNTERS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [<span data-ttu-id="19f4f-111">**方向 \_ 喜好設定**</span><span class="sxs-lookup"><span data-stu-id="19f4f-111">**ORIENTATION\_PREFERENCE**</span></span>](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [<span data-ttu-id="19f4f-112">**PEB**</span><span class="sxs-lookup"><span data-stu-id="19f4f-112">**PEB**</span></span>](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [<span data-ttu-id="19f4f-113">**PEB \_ LDR \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="19f4f-113">**PEB\_LDR\_DATA**</span></span>](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [<span data-ttu-id="19f4f-114">**處理 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="19f4f-114">**PROCESS\_INFORMATION**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [<span data-ttu-id="19f4f-115">**進程 \_ 記憶體 \_ 耗盡 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="19f4f-115">**PROCESS\_MEMORY\_EXHAUSTION\_INFO**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [<span data-ttu-id="19f4f-116">**進程 \_ 緩和 \_ ASLR \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="19f4f-116">**PROCESS\_MITIGATION\_ASLR\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [<span data-ttu-id="19f4f-117">**處理 \_ 緩和 \_ 二進位簽章 \_ \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="19f4f-117">**PROCESS\_MITIGATION\_BINARY\_SIGNATURE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [<span data-ttu-id="19f4f-118">**處理 \_ 緩和 \_ 控制 \_ 流程 \_ 防護 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="19f4f-118">**PROCESS\_MITIGATION\_CONTROL\_FLOW\_GUARD\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [<span data-ttu-id="19f4f-119">**處理 \_ 緩和 \_ DEP \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="19f4f-119">**PROCESS\_MITIGATION\_DEP\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [<span data-ttu-id="19f4f-120">**處理 \_ 緩和 \_ 動態程式 \_ 代碼 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="19f4f-120">**PROCESS\_MITIGATION\_DYNAMIC\_CODE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [<span data-ttu-id="19f4f-121">**進程 \_ 緩和 \_ 擴充 \_ 點 \_ 停用 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="19f4f-121">**PROCESS\_MITIGATION\_EXTENSION\_POINT\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [<span data-ttu-id="19f4f-122">**進程 \_ 緩和 \_ 字型 \_ 停用 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="19f4f-122">**PROCESS\_MITIGATION\_FONT\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [<span data-ttu-id="19f4f-123">**進程 \_ 緩和 \_ 映射 \_ 載入 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="19f4f-123">**PROCESS\_MITIGATION\_IMAGE\_LOAD\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [<span data-ttu-id="19f4f-124">**流程 \_ 風險降低 \_ 嚴格 \_ 控制碼 \_ 檢查 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="19f4f-124">**PROCESS\_MITIGATION\_STRICT\_HANDLE\_CHECK\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [<span data-ttu-id="19f4f-125">**進程 \_ 緩和 \_ 系統 \_ 呼叫 \_ 停用 \_ 原則**</span><span class="sxs-lookup"><span data-stu-id="19f4f-125">**PROCESS\_MITIGATION\_SYSTEM\_CALL\_DISABLE\_POLICY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [<span data-ttu-id="19f4f-126">**RTL \_ 使用者 \_ 進程 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="19f4f-126">**RTL\_USER\_PROCESS\_PARAMETERS**</span></span>](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [<span data-ttu-id="19f4f-127">**STARTUPINFO**</span><span class="sxs-lookup"><span data-stu-id="19f4f-127">**STARTUPINFO**</span></span>](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [<span data-ttu-id="19f4f-128">**STARTUPINFOEX**</span><span class="sxs-lookup"><span data-stu-id="19f4f-128">**STARTUPINFOEX**</span></span>](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [<span data-ttu-id="19f4f-129">**TEB**</span><span class="sxs-lookup"><span data-stu-id="19f4f-129">**TEB**</span></span>](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a><span data-ttu-id="19f4f-130">處理器結構</span><span class="sxs-lookup"><span data-stu-id="19f4f-130">Processor Structures</span></span>

<span data-ttu-id="19f4f-131">下列結構適用于處理器和處理器群組：</span><span class="sxs-lookup"><span data-stu-id="19f4f-131">The following structures are used with processors and processor groups:</span></span>

-   [<span data-ttu-id="19f4f-132">**快取 \_ 關聯性**</span><span class="sxs-lookup"><span data-stu-id="19f4f-132">**CACHE\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [<span data-ttu-id="19f4f-133">**群組 \_ 親和性**</span><span class="sxs-lookup"><span data-stu-id="19f4f-133">**GROUP\_AFFINITY**</span></span>](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [<span data-ttu-id="19f4f-134">**群組 \_ 關聯性**</span><span class="sxs-lookup"><span data-stu-id="19f4f-134">**GROUP\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [<span data-ttu-id="19f4f-135">**NUMA \_ 節點 \_ 關聯性**</span><span class="sxs-lookup"><span data-stu-id="19f4f-135">**NUMA\_NODE\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [<span data-ttu-id="19f4f-136">**處理器 \_ 群組 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="19f4f-136">**PROCESSOR\_GROUP\_INFO**</span></span>](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [<span data-ttu-id="19f4f-137">**處理器 \_ 編號**</span><span class="sxs-lookup"><span data-stu-id="19f4f-137">**PROCESSOR\_NUMBER**</span></span>](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [<span data-ttu-id="19f4f-138">**處理器 \_ 關聯性**</span><span class="sxs-lookup"><span data-stu-id="19f4f-138">**PROCESSOR\_RELATIONSHIP**</span></span>](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [<span data-ttu-id="19f4f-139">**系統 \_ CPU \_ 集 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="19f4f-139">**SYSTEM\_CPU\_SET\_INFORMATION**</span></span>](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [<span data-ttu-id="19f4f-140">**系統 \_ 邏輯 \_ 處理器 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="19f4f-140">**SYSTEM\_LOGICAL\_PROCESSOR\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [<span data-ttu-id="19f4f-141">**系統 \_ 邏輯 \_ 處理器 \_ 資訊， \_ 例如**</span><span class="sxs-lookup"><span data-stu-id="19f4f-141">**SYSTEM\_LOGICAL\_PROCESSOR\_INFORMATION\_EX**</span></span>](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a><span data-ttu-id="19f4f-142">發送器佇列結構</span><span class="sxs-lookup"><span data-stu-id="19f4f-142">Dispatcher Queue Structure</span></span>

<span data-ttu-id="19f4f-143">下列結構是用來建立 [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller)。</span><span class="sxs-lookup"><span data-stu-id="19f4f-143">The following structure is used to create a [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller).</span></span>

-   [<span data-ttu-id="19f4f-144">**DispatcherQueueOptions**</span><span class="sxs-lookup"><span data-stu-id="19f4f-144">**DispatcherQueueOptions**</span></span>](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a><span data-ttu-id="19f4f-145">工作物件結構</span><span class="sxs-lookup"><span data-stu-id="19f4f-145">Job Object Structures</span></span>

<span data-ttu-id="19f4f-146">下列結構適用于工作物件：</span><span class="sxs-lookup"><span data-stu-id="19f4f-146">The following structures are used with job objects:</span></span>

-   [<span data-ttu-id="19f4f-147">**JOBOBJECT \_ 建立 \_ 完成 \_ 埠的關聯**</span><span class="sxs-lookup"><span data-stu-id="19f4f-147">**JOBOBJECT\_ASSOCIATE\_COMPLETION\_PORT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [<span data-ttu-id="19f4f-148">**JOBOBJECT \_ 基本 \_ 帳戶處理 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="19f4f-148">**JOBOBJECT\_BASIC\_ACCOUNTING\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [<span data-ttu-id="19f4f-149">**JOBOBJECT \_ 基本 \_ 和 \_ IO 的 \_ 帳戶處理 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="19f4f-149">**JOBOBJECT\_BASIC\_AND\_IO\_ACCOUNTING\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [<span data-ttu-id="19f4f-150">**JOBOBJECT \_ 基本 \_ 限制 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="19f4f-150">**JOBOBJECT\_BASIC\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [<span data-ttu-id="19f4f-151">**JOBOBJECT \_ 基本 \_ 進程 \_ 標識號 \_ 清單**</span><span class="sxs-lookup"><span data-stu-id="19f4f-151">**JOBOBJECT\_BASIC\_PROCESS\_ID\_LIST**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [<span data-ttu-id="19f4f-152">**JOBOBJECT \_ 基本 \_ UI \_ 限制**</span><span class="sxs-lookup"><span data-stu-id="19f4f-152">**JOBOBJECT\_BASIC\_UI\_RESTRICTIONS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [<span data-ttu-id="19f4f-153">**JOBOBJECT \_ \_ \_ 作業 \_ 時間 \_ 資訊結束**</span><span class="sxs-lookup"><span data-stu-id="19f4f-153">**JOBOBJECT\_END\_OF\_JOB\_TIME\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [<span data-ttu-id="19f4f-154">**JOBOBJECT \_ 延伸的 \_ 限制 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="19f4f-154">**JOBOBJECT\_EXTENDED\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [<span data-ttu-id="19f4f-155">**JOBOBJECT \_ 安全性 \_ 限制 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="19f4f-155">**JOBOBJECT\_SECURITY\_LIMIT\_INFORMATION**</span></span>](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a><span data-ttu-id="19f4f-156">User-Mode 排程結構</span><span class="sxs-lookup"><span data-stu-id="19f4f-156">User-Mode Scheduling Structures</span></span>

<span data-ttu-id="19f4f-157">下列結構適用于 UMS：</span><span class="sxs-lookup"><span data-stu-id="19f4f-157">The following structures are used with UMS:</span></span>

-   [<span data-ttu-id="19f4f-158">**UMS \_ 建立 \_ 執行緒 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="19f4f-158">**UMS\_CREATE\_THREAD\_ATTRIBUTES**</span></span>](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [<span data-ttu-id="19f4f-159">**UMS 排程器 \_ \_ 啟動 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="19f4f-159">**UMS\_SCHEDULER\_STARTUP\_INFO**</span></span>](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [<span data-ttu-id="19f4f-160">**UMS \_ 系統 \_ 執行緒 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="19f4f-160">**UMS\_SYSTEM\_THREAD\_INFORMATION**</span></span>](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
