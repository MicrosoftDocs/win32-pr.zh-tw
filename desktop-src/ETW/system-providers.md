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
# <a name="system-providers"></a>系統提供者
 
從 Windows 10 SDK 組建20348開始，系統追蹤提供者的事件可以使用與其他 ETW 提供者相同的方式來啟用 [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)。  與系統追蹤提供者相關聯的不同旗標和 [群組遮罩](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) 已對應到新的追蹤提供者，稱為系統提供者和相符的關鍵字。  
 
就像直接啟用系統追蹤提供者一樣，系統提供者只能由具有 [EVENT_TRACE_SYSTEM_LOGGER_MODE](/windows/win32/etw/logging-mode-constants) 設定的會話啟用。

## <a name="system-provider-reference"></a>系統提供者參考

* [系統 ALPC 提供者](#system-alpc-provider)
* [系統設定提供者](#system-config-provider)
* [系統 CPU 提供者](#system-cpu-provider)
* [系統管理者提供者](#system-hypervisor-provider)
* [系統中斷提供者](#system-interrupt-provider)
* [系統 IO 提供者](#system-io-provider)
* [系統 IO 篩選器提供者](#system-io-filter-provider)
* [系統鎖定提供者](#system-lock-provider)
* [系統記憶體提供者](#system-memory-provider)
* [系統物件提供者](#system-object-provider)
* [系統電源提供者](#system-power-provider)
* [系統進程提供者](#system-process-provider)
* [系統設定檔提供者](#system-profile-provider)
* [系統登錄提供者](#system-registry-provider)
* [系統排程器提供者](#system-scheduler-provider)
* [系統 Syscall 提供者](#system-syscall-provider)
* [系統計時器提供者](#system-timer-provider)
 
### <a name="system-alpc-provider"></a>系統 ALPC 提供者

提供與 ALPC 系統相關的事件。

GUID： SystemAlpcProviderGuid {fcb9baaf-e529-4980-92e9-ced1a6aadfdf}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_ALPC_KW_GENERAL | PERF_ALPC，EVENT_TRACE_FLAG_ALPC |
 
### <a name="system-config-provider"></a>系統設定提供者 

提供系統組態事件。

GUID： SystemConfigProviderGuid {fef3a8b6-318d-4b67-a96a-3b0f6b8f18fe}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_CONFIG_KW_SYSTEM | PERF_SYSCFG_SYSTEM |
| SYSTEM_CONFIG_KW_GRAPHICS | PERF_SYSCFG_GRAPHICS |
| SYSTEM_CONFIG_KW_STORAGE | PERF_SYSCFG_STORAGE |
| SYSTEM_CONFIG_KW_NETWORK | PERF_SYSCFG_NETWORK |
| SYSTEM_CONFIG_KW_SERVICES | PERF_SYSCFG_SERVICES |
| SYSTEM_CONFIG_KW_PNP | PERF_SYSCFG_PNP |
| SYSTEM_CONFIG_KW_OPTICAL | PERF_SYSCFG_OPTICAL |
 
### <a name="system-cpu-provider"></a>系統 CPU 提供者 

提供與 CPU 相關的事件。

GUID： SystemCpuProviderGuid {c6c5265f-eae8-4650-aae4-9d48603d8510}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_CPU_KW_CONFIG | PERF_CPU_CONFIG |
| SYSTEM_CPU_KW_CACHE_FLUSH | PERF_CACHE_FLUSH |
| SYSTEM_CPU_KW_SPEC_CONTROL | PERF_SPEC_CONTROL |
 
### <a name="system-hypervisor-provider"></a>系統管理者提供者 

提供與管理程式相關的事件。

GUID： SystemHypervisorProviderGuid {bafa072a-918a-4bed-b622-bc152097098f}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_HYPERVISOR_KW_PROFILE | PERF_HV_PROFILE |
| SYSTEM_HYPERVISOR_KW_CALLOUTS | PERF_HV_CALLOUTS |
| SYSTEM_HYPERVISOR_KW_VTL_CHANGE | PERF_VTL_CHANGE |
 
### <a name="system-interrupt-provider"></a>系統中斷提供者 

提供與 Dpc 和中斷相關的事件。

GUID： SystemInterruptProviderGuid {d4bbee17-b545-4888-858b-744169015b25}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_INTERRUPT_KW_GENERAL | PERF_INTERRUPT，EVENT_TRACE_FLAG_INTERRUPT |
| SYSTEM_INTERRUPT_KW_CLOCK_INTERRUPT | PERF_CLOCK_INTERRUPT |
| SYSTEM_INTERRUPT_KW_DPC | PERF_DPC，EVENT_TRACE_FLAG_DPC |
| SYSTEM_INTERRUPT_KW_DPC_QUEUE | PERF_DPC_QUEUE |
| SYSTEM_INTERRUPT_KW_WDF_DPC | PERF_WDF_DPC |
| SYSTEM_INTERRUPT_KW_WDF_INTERRUPT | PERF_WDF_INTERRUPT |
| SYSTEM_INTERRUPT_KW_IPI | PERF_IPI |
 
 
### <a name="system-io-provider"></a>系統 IO 提供者 

提供與多種 IO （包括磁片、快取和網路）相關的事件。

GUID： SystemIoProviderGuid {3d5c43e3-0f1c-4202-b817-174c0070dc79}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_IO_KW_DISK | EVENT_TRACE_FLAG_DISK_IO |
| SYSTEM_IO_KW_DISK_INIT | PERF_DISK_IO_INIT，EVENT_TRACE_FLAG_DISK_IO_INIT |
| SYSTEM_IO_KW_FILENAME | PERF_FILENAME，EVENT_TRACE_FLAG_DISK_FILE_IO |
| SYSTEM_IO_KW_SPLIT | PERF_SPLIT_IO，EVENT_TRACE_FLAG_SPLIT_IO |
| SYSTEM_IO_KW_FILE | PERF_FILE_IO，EVENT_TRACE_FLAG_FILE_IO |
| SYSTEM_IO_KW_OPTICAL | PERF_OPTICAL_IO，EVENT_TRACE_FLAG_FILE_IO_INIT |
| SYSTEM_IO_KW_OPTICAL_INIT | PERF_OPTICAL_IO_INIT |
| SYSTEM_IO_KW_DRIVERS | PERF_DRIVERS，EVENT_TRACE_FLAG_DRIVER |
| SYSTEM_IO_KW_CC | PERF_CC |
| SYSTEM_IO_KW_NETWORK | PERF_NETWORK，EVENT_TRACE_FLAG_NETWORK_TCPIP |

注意：啟用 SYSTEM_IO_KW_DRIVERS 關鍵字也會自動啟用 SYSTEM_IO_KW_FILENAME。  使用 SYSTEM_MEMORY_KW_MEMORY 關鍵字啟用系統記憶體提供者時，也會自動開啟 SYSTEM_IO_KW_FILENAME。
 
### <a name="system-io-filter-provider"></a>系統 IO 篩選器提供者 

提供與 IO 篩選相關的事件，包括計時和失敗。

GUID： SystemIoFilterProviderGuid {fbd09363-9e22-4661-b8bf-e7a34b535b8c}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_IOFILTER_KW_GENERAL | PERF_FLT_IO |
| SYSTEM_IOFILTER_KW_INIT | PERF_FLT_IO_INIT |
| SYSTEM_IOFILTER_KW_FASTIO | PERF_FLT_FASTIO |
| SYSTEM_IOFILTER_KW_FAILURE | PERF_FLT_IO_FAILURE |
 
### <a name="system-lock-provider"></a>系統鎖定提供者 

提供與核心鎖定機制相關的事件。

GUID： SystemLockProviderGuid {721ddfd3-dacc-4e1e-b26a-a2cb31d4705a}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_LOCK_KW_SPINLOCK | PERF_SPINLOCK |
| SYSTEM_LOCK_KW_SPINLOCK_COUNTERS | PERF_SPINLOCK_CNTRS |
| SYSTEM_LOCK_KW_SYNC_OBJECTS | PERF_SYNC_OBJECTS |
 
### <a name="system-memory-provider"></a>系統記憶體提供者 

提供與記憶體管理員相關的事件。

GUID： SystemMemoryProviderGuid {82958ca9-b6cd-47f8-a3a8-03ae85a4bc24}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_MEMORY_KW_GENERAL | PERF_MEMORY |
| SYSTEM_MEMORY_KW_HARD_FAULTS | PERF_HARD_FAULTS，EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS |
| SYSTEM_MEMORY_KW_ALL_FAULTS | PERF_ALL_FAULTS，EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS |
| SYSTEM_MEMORY_KW_POOL | PERF_POOL |
| SYSTEM_MEMORY_KW_MEMINFO | PERF_MEMINFO |
| SYSTEM_MEMORY_KW_PFSECTION | PERF_PFSECTION |
| SYSTEM_MEMORY_KW_MEMINFO_WS | PERF_MEMINFO_WS |
| SYSTEM_MEMORY_KW_HEAP | PERF_HEAP |
| SYSTEM_MEMORY_KW_WS | PERF_WS |
| SYSTEM_MEMORY_KW_CONTMEM_GEN | PERF_CONTMEM_GEN |
| SYSTEM_MEMORY_KW_VIRTUAL_ALLOC | PERF_VIRTUAL_ALLOC，EVENT_TRACE_FLAG_VIRTUAL_ALLOC |
| SYSTEM_MEMORY_KW_FOOTPRINT | PERF_FOOTPRINT |
| SYSTEM_MEMORY_KW_SESSION | PERF_SESSION |
| SYSTEM_MEMORY_KW_REFSET | PERF_REFSET |
| SYSTEM_MEMORY_KW_VAMAP | PERF_VAMAP，EVENT_TRACE_FLAG_VAMAP |

注意： 
* 啟用 SYSTEM_MEMORY_KW_MEMORY 關鍵字也會自動啟用系統 IO 提供者的 SYSTEM_IO_KW_FILENAME。
* SYSTEM_MEMORY_KW_POOL 啟用的事件支援集區標籤篩選，以選擇性地只針對特定集區標記寫入事件。  這會設定為系統記憶體提供者的 [架構化篩選](/windows/win32/api/evntprov/ns-evntprov-event_filter_descriptor) 。  PoolTag 篩選器的結構如下所示：

    ```cpp
    {
    EVENT_FILTER_HEADER Header; 
    ULONG PoolTags[ETW_MAX_POOLTAG_FILTER];
    }
    ```

* [EVENT_FILTER_HEADER](/windows/win32/api/evntprov/ns-evntprov-event_filter_header)應以設定為 SYSTEM_MEMORY_POOL_FILTER_ID 的識別碼進行初始化，而 size 欄位設定為標頭大小加上 PoolTags 陣列的使用部分。  

* 每個集區標籤是在篩選中儲存為 ULONG 的4個字元字串。  
 
 
### <a name="system-object-provider"></a>系統物件提供者 

提供與物件管理員相關的事件。

GUID： SystemObjectProviderGuid {febd7460-3d1d-47eb-af49-c9eeb1e146f2}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_OBJECT_KW_HANDLE | PERF_OB_HANDLE |
| SYSTEM_OBJECT_KW_OBJECT | PERF_OB_OBJECT |
 
### <a name="system-power-provider"></a>系統電源提供者 

提供與系統電源狀態相關的事件。

GUID： SystemPowerProviderGuid {c134884a-32d5-4488-80e5-14ed7abb8269}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_POWER_KW_GENERAL | PERF_POWER |
| SYSTEM_POWER_KW_HIBER_RUNDOWN | PERF_HIBER_RUNDOWN |
| SYSTEM_POWER_KW_PROCESSOR_IDLE | PERF_PROCESSOR_IDLE |
| SYSTEM_POWER_KW_IDLE_SELECTION | PERF_IDLE_SELECTION |
| SYSTEM_POWER_KW_PPM_EXIT_LATENCY | PERF_PPM_EXIT_LATENCY |
 
### <a name="system-process-provider"></a>系統進程提供者 

提供與進程相關的事件，包括存留期資訊、影像載入事件，以及執行緒相關事件。

GUID： SystemProcessProviderGuid {151f55dc-467d-471f-83b5-5f889d46ff66}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_PROCESS_KW_GENERAL | PERF_PROCESS，EVENT_TRACE_FLAG_PROCESS |
| SYSTEM_PROCESS_KW_INSWAP | PERF_PROCESS_INSWAP |
| SYSTEM_PROCESS_KW_FREEZE | PERF_PROCESS_FREEZE |
| SYSTEM_PROCESS_KW_PERF_COUNTER | PERF_PERF_COUNTER，EVENT_TRACE_FLAG_PROCESS_COUNTERS |
| SYSTEM_PROCESS_KW_WAKE_COUNTER | PERF_WAKE_COUNTER |
| SYSTEM_PROCESS_KW_WAKE_DROP | PERF_WAKE_DROP |
| SYSTEM_PROCESS_KW_WAKE_EVENT | PERF_WAKE_EVENT |
| SYSTEM_PROCESS_KW_DEBUG_EVENTS | PERF_DEBUG_EVENTS，EVENT_TRACE_FLAG_DEBUG_EVENTS |
| SYSTEM_PROCESS_KW_DBGPRINT | PERF_DBGPRINT，EVENT_TRACE_FLAG_DBGPRINT |
| SYSTEM_PROCESS_KW_JOB | PERF_JOB，EVENT_TRACE_FLAG_JOB |
| SYSTEM_PROCESS_KW_WORKER_THREAD | PERF_WORKER_THREAD |
| SYSTEM_PROCESS_KW_THREAD | PERF_THREAD，EVENT_TRACE_FLAG_THREAD |
| SYSTEM_PROCESS_KW_LOADER | PERF_LOADER，EVENT_TRACE_FLAG_IMAGE_LOAD |
 
### <a name="system-profile-provider"></a>系統設定檔提供者 

提供分析事件。

GUID： SystemProfileProviderGuid {bfeb0324-1cee-496f-a409-2ac2b48a6322}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_PROFILE_KW_GENERAL | PERF_PROFILE，EVENT_TRACE_FLAG_PROFILE |
| SYSTEM_PROFILE_KW_PMC_PROFILE | PERF_PMC_PROFILE |
 
### <a name="system-registry-provider"></a>系統登錄提供者 

提供與登錄相關的事件。

GUID： SystemRegistryProviderGuid {16156bd9-fab4-4cfa-a232-89d1099058e3}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_REGISTRY_KW_GENERAL | PERF_REGISTRY，EVENT_TRACE_FLAG_REGISTRY |
| SYSTEM_REGISTRY_KW_HIVE | PERF_REG_HIVE |
| SYSTEM_REGISTRY_KW_NOTIFICATION | PERF_REG_NOTIF |
 
### <a name="system-scheduler-provider"></a>系統排程器提供者 

提供與排程器相關的事件。

GUID： SystemSchedulerProviderGuid {599a2a76-4d91-4910-9ac7-7d33f2e97a6c}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_SCHEDULER_KW_XSCHEDULER | PERF_XSCHEDULER |
| SYSTEM_SCHEDULER_KW_DISPATCHER | PERF_DISPATCHER，EVENT_TRACE_FLAG_DISPATCHER |
| SYSTEM_SCHEDULER_KW_KERNEL_QUEUE | PERF_KERNEL_QUEUE |
| SYSTEM_SCHEDULER_KW_SHOULD_YIELD | PERF_SHOULD_YIELD |
| SYSTEM_SCHEDULER_KW_ANTI_STAR加值稅ION | PERF_ANTI_STAR加值稅ION |
| SYSTEM_SCHEDULER_KW_LOAD_BALANCER | PERF_LOAD_BALANCER |
| SYSTEM_SCHEDULER_KW_AFFINITY | PERF_AFFINITY |
| SYSTEM_SCHEDULER_KW_PRIORITY | PERF_PRIORITY |
| SYSTEM_SCHEDULER_KW_IDEAL_PROCESSOR | PERF_IDEAL_PROCESSOR |
| SYSTEM_SCHEDULER_KW_CONTEXT_SWITCH | PERF_CONTEXT_SWITCH，EVENT_TRACE_FLAG_CSWITCH |
 
### <a name="system-syscall-provider"></a>系統 Syscall 提供者 

提供事件與系統呼叫相關的資訊。

GUID： SystemSyscallProviderGuid {434286f7-6f1b-45bb-b37e-95f623046c7c}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_SYSCALL_KW_GENERAL | PERF_SYSCALL，EVENT_TRACE_FLAG_SYSTEMCALL |
 
### <a name="system-timer-provider"></a>系統計時器提供者 

提供與核心中計時器相關的事件。

GUID： SystemTimerProviderGuid {4f061568-e215-499f-ab2e-eda0ae890a5b}

| 關鍵字 | 對應的舊版旗標和群組 |
| ------- | ------------------------------------- |
| SYSTEM_TIMER_KW_GENERAL | PERF_TIMER |
| SYSTEM_TIMER_KW_CLOCK_TIMER | PERF_CLOCK_TIMER |
 
## <a name="remarks"></a>備註

這項新的啟用機制，除了預先存在用來啟用這些事件的方法之外。  任何使用的程式碼都將繼續執行此作業。
 
由於這項新功能，系統追蹤提供者所產生的事件不會變更。  這表示輸出的事件未標示為從個別系統提供者發出。
 
如需提供者 GUID 和關鍵字定義的詳細資訊，請參閱[evntrace。](/windows/win32/api/evntrace/)

## <a name="see-also"></a>另請參閱

[設定並啟動 SystemTraceProvider 會話](configuring-and-starting-a-systemtraceprovider-session.md)

[evntrace .h 標頭](/windows/win32/api/evntrace/)