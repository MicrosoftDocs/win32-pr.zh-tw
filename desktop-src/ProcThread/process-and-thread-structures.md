---
description: 本主題列出 (UMS) 的進程、執行緒、處理器、工作物件和使用者模式排程使用的結構。
ms.assetid: dbb50193-4c67-494e-9c46-2ac3106fac9a
title: 進程和執行緒結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5893340c72ee46eff43b16db936025fbb5463fbe0cc10e2eba1829962269d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081378"
---
# <a name="process-and-thread-structures"></a>進程和執行緒結構

本主題列出 (UMS) 的進程、執行緒、處理器、工作物件和使用者模式排程使用的結構。

## <a name="process-and-thread-structures"></a>進程和執行緒結構

下列結構適用于處理常式和執行緒：

-   [**應用程式 \_ 記憶體 \_ 資訊**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-app_memory_information)
-   [**AR \_ 狀態**](/windows/win32/api/winuser/ne-winuser-ar_state)
-   [**快取 \_ 描述項**](/windows/desktop/api/WinNT/ns-winnt-cache_descriptor)
-   [**IO \_ 計數器**](/windows/desktop/api/WinNT/ns-winnt-io_counters)
-   [**方向 \_ 喜好設定**](/windows/desktop/api/WinUser/ne-winuser-orientation_preference)
-   [**PEB**](/windows/desktop/api/Winternl/ns-winternl-peb)
-   [**PEB \_ LDR \_ 資料**](/windows/desktop/api/Winternl/ns-winternl-peb_ldr_data)
-   [**處理 \_ 資訊**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information)
-   [**進程 \_ 記憶體 \_ 耗盡 \_ 資訊**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_memory_exhaustion_info)
-   [**進程 \_ 緩和 \_ ASLR \_ 原則**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_aslr_policy)
-   [**處理 \_ 緩和 \_ 二進位簽章 \_ \_ 原則**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_binary_signature_policy)
-   [**處理 \_ 緩和 \_ 控制 \_ 流程 \_ 防護 \_ 原則**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_control_flow_guard_policy)
-   [**處理 \_ 緩和 \_ DEP \_ 原則**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dep_policy)
-   [**處理 \_ 緩和 \_ 動態程式 \_ 代碼 \_ 原則**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_dynamic_code_policy)
-   [**進程 \_ 緩和 \_ 擴充 \_ 點 \_ 停用 \_ 原則**](/windows/desktop/api/winnt/ns-winnt-process_mitigation_extension_point_disable_policy)
-   [**進程 \_ 緩和 \_ 字型 \_ 停用 \_ 原則**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_font_disable_policy)
-   [**進程 \_ 緩和 \_ 映射 \_ 載入 \_ 原則**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_image_load_policy)
-   [**流程 \_ 風險降低 \_ 嚴格 \_ 控制碼 \_ 檢查 \_ 原則**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_strict_handle_check_policy)
-   [**進程 \_ 緩和 \_ 系統 \_ 呼叫 \_ 停用 \_ 原則**](/windows/desktop/api/WinNT/ns-winnt-process_mitigation_system_call_disable_policy)
-   [**RTL \_ 使用者 \_ 進程 \_ 參數**](/windows/desktop/api/Winternl/ns-winternl-rtl_user_process_parameters)
-   [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)
-   [**STARTUPINFOEX**](/windows/desktop/api/WinBase/ns-winbase-startupinfoexa)
-   [**TEB**](/windows/desktop/api/Winternl/ns-winternl-teb)

## <a name="processor-structures"></a>處理器結構

下列結構適用于處理器和處理器群組：

-   [**快取 \_ 關聯性**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)
-   [**群組 \_ 親和性**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)
-   [**群組 \_ 關聯性**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)
-   [**NUMA \_ 節點 \_ 關聯性**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)
-   [**處理器 \_ 群組 \_ 資訊**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)
-   [**處理器 \_ 編號**](/windows/desktop/api/WinNT/ns-winnt-processor_number)
-   [**處理器 \_ 關聯性**](/windows/desktop/api/WinNT/ne-winnt-logical_processor_relationship)
-   [**系統 \_ CPU \_ 集 \_ 資訊**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information)
-   [**系統 \_ 邏輯 \_ 處理器 \_ 資訊**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information)
-   [**系統 \_ 邏輯 \_ 處理器 \_ 資訊， \_ 例如**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)

## <a name="dispatcher-queue-structure"></a>發送器佇列結構

下列結構是用來建立 [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller)。

-   [**DispatcherQueueOptions**](/windows/desktop/api/DispatcherQueue/ns-dispatcherqueue-dispatcherqueueoptions)

## <a name="job-object-structures"></a>工作物件結構

下列結構適用于工作物件：

-   [**JOBOBJECT \_ 建立 \_ 完成 \_ 埠的關聯**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port)
-   [**JOBOBJECT \_ 基本 \_ 帳戶處理 \_ 資訊**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**JOBOBJECT \_ 基本 \_ 和 \_ IO 的 \_ 帳戶處理 \_ 資訊**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)
-   [**JOBOBJECT \_ 基本 \_ 限制 \_ 資訊**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**JOBOBJECT \_ 基本 \_ 進程 \_ 標識號 \_ 清單**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_process_id_list)
-   [**JOBOBJECT \_ 基本 \_ UI \_ 限制**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**JOBOBJECT \_ \_ \_ 作業 \_ 時間 \_ 資訊結束**](/windows/desktop/api/WinNT/ns-winnt-jobobject_end_of_job_time_information)
-   [**JOBOBJECT \_ 延伸的 \_ 限制 \_ 資訊**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**JOBOBJECT \_ 安全性 \_ 限制 \_ 資訊**](/windows/desktop/api/WinNT/ns-winnt-jobobject_security_limit_information)

## <a name="user-mode-scheduling-structures"></a>User-Mode 排程結構

下列結構適用于 UMS：

-   [**UMS \_ 建立 \_ 執行緒 \_ 屬性**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)
-   [**UMS 排程器 \_ \_ 啟動 \_ 資訊**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)
-   [**UMS \_ 系統 \_ 執行緒 \_ 資訊**](/windows/desktop/api/WinBase/ns-winbase-ums_system_thread_information)

 

 
