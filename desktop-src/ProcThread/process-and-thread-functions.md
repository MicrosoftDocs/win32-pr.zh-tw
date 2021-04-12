---
description: 本主題說明進程和執行緒函數。
ms.assetid: 8c8e8af0-bf50-4a4b-945c-83bae1eff7dd
title: 處理序和執行緒函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97d871c7fc3635734ce79ba5cbf231e6955e59d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192757"
---
# <a name="process-and-thread-functions"></a>處理序和執行緒函式

本主題說明進程和執行緒函數。

-   [分派佇列函數](#dispatch-queue-function)
-   [進程函式](#process-functions)
-   [處理列舉函數](#process-enumeration-functions)
-   [原則函數](#policy-functions)
-   [執行緒函數](#thread-functions)
-   [進程和執行緒擴充屬性函式](#process-and-thread-extended-attribute-functions)
-   [WOW64 函數](#wow64-functions)
-   [工作物件函數](#job-object-functions)
-   [執行緒集區函數](#thread-pool-functions)
-   [執行緒排序服務函式](#thread-ordering-service-functions)
-   [多媒體類別排程器服務函數](#multimedia-class-scheduler-service-functions)
-   [光纖函數](#fiber-functions)
-   [NUMA 支援函式](#numa-support-functions)
-   [處理器函數](#processor-functions)
-   [使用者模式排程功能](#user-mode-scheduling-functions)
-   [過時的函式](#obsolete-functions)

## <a name="dispatch-queue-function"></a>分派佇列函數

下列函數會建立 [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller)。



| 函式                                                                   | 描述                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDispatcherQueueController**](/windows/desktop/api/DispatcherQueue/nf-dispatcherqueue-createdispatcherqueuecontroller) | 建立 [DispatcherQueueController](/uwp/api/windows.system.dispatcherqueuecontroller) ，其管理在另一個執行緒上依優先權循序執行佇列工作之 [DispatcherQueue](/uwp/api/windows.system.dispatcherqueue) 的存留期。 |



 

## <a name="process-functions"></a>進程函式

下列函式可用於 [處理](child-processes.md)程式。



| 函式                                                                 | 描述                                                                                                                                                                                   |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)                                   | 建立新的進程及其主要執行緒。                                                                                                                                                 |
| [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)                       | 建立新的進程及其主要執行緒。 新的進程會在使用者的安全性內容中，以指定的權杖表示。                                                    |
| [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw)               | 建立新的進程及其主要執行緒。 然後，新的進程會在指定認證的安全性內容中執行指定的可執行檔 (使用者、網域和密碼) 。      |
| [**CreateProcessWithTokenW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithtokenw)               | 建立新的進程及其主要執行緒。 新的進程會在指定之權杖的安全性內容中執行。                                                                            |
| [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)                                       | 結束呼叫進程及其所有線程。                                                                                                                                                 |
| [**FlushProcessWriteBuffers**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushprocesswritebuffers)             | 清除執行目前進程之執行緒的每個處理器的寫入佇列。                                                                                                    |
| [**FreeEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa)                 | 釋放環境字串的區塊。                                                                                                                                                         |
| [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea)                                 | 抓取目前進程的命令列字串。                                                                                                                                    |
| [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess)                           | 抓取目前進程的虛擬控制碼。                                                                                                                                            |
| [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid)                       | 抓取呼叫進程的處理序識別碼。                                                                                                                                      |
| [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)           | 在呼叫此函式期間，抓取目前線程正在其上執行的處理器數目。                                                                                     |
| [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings)                   | 捕獲目前進程的環境區塊。                                                                                                                                      |
| [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable)                 | 從呼叫進程的環境區塊抓取指定之變數的值。                                                                                              |
| [**>getexitcodeprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess)                         | 捕獲指定進程的終止狀態。                                                                                                                                    |
| [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources)                               | 抓取指定進程使用中的圖形化使用者介面 (GUI) 物件的控制碼計數。                                                                                     |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) | 抓取邏輯處理器和相關硬體的相關資訊。                                                                                                                          |
| [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass)                             | 抓取指定進程的優先權類別。                                                                                                                                       |
| [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask)                 | 抓取指定進程的進程親和性遮罩，以及系統的系統親和性遮罩。                                                                                      |
| [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)               | 抓取指定進程的處理器群組親和性。                                                                                                                              |
| [**GetProcessHandleCount**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesshandlecount)                   | 抓取屬於指定進程的開啟控制碼數目。                                                                                                                    |
| [**GetProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessid)                                     | 捕獲指定進程的處理序識別碼。                                                                                                                                    |
| [**GetProcessIdOfThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessidofthread)                     | 抓取與指定之執行緒相關聯之進程的處理序識別碼。                                                                                                         |
| [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters)                     | 抓取指定進程所執行之所有 i/o 作業的帳戶處理資訊。                                                                                                   |
| [**GetProcessMitigationPolicy**](/windows/desktop/api/Processthreadsapi/nf-processthreadsapi-getprocessmitigationpolicy)         | 抓取呼叫進程的風險降低原則設定。                                                                                                                                 |
| [**GetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost)               | 抓取指定進程的優先權提升控制狀態。                                                                                                                          |
| [**GetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessshutdownparameters)     | 抓取目前呼叫進程的關機參數。                                                                                                                              |
| [**GetProcessTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes)                               | 取得指定進程的計時資訊。                                                                                                                                 |
| [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion)                           | 抓取指定進程預期執行的系統主要和次要版本號碼。                                                                                    |
| [**GetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-getprocessworkingsetsize)             | 抓取指定進程的最小和最大工作集大小。                                                                                                                 |
| [**GetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-getprocessworkingsetsizeex)         | 抓取指定進程的最小和最大工作集大小。                                                                                                                 |
| [**GetProcessorSystemCycleTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)       | 抓取指定群組中每個處理器執行延遲程序呼叫所花費的週期時間， (Dpc) 和插斷服務常式 (Isr) 。                                         |
| [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow)                                 | 抓取建立呼叫進程時所指定的 [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) 結構內容。                                                       |
| [**IsImmersiveProcess**](/windows/desktop/api/Winuser/nf-winuser-isimmersiveprocess)                         | 判斷進程是否屬於 Windows Store 應用程式。                                                                                                                                |
| [**NeedCurrentDirectoryForExePath**](/windows/win32/api/processenv/nf-processenv-needcurrentdirectoryforexepatha) | 判斷目前目錄是否應該包含在指定之可執行檔的搜尋路徑中。                                                                                  |
| [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)                                       | 開啟現有的本機處理常式物件。                                                                                                                                                       |
| [**QueryFullProcessImageName**](/windows/desktop/api/WinBase/nf-winbase-queryfullprocessimagenamea)           | 抓取指定進程之可執行映射的完整名稱。                                                                                                                    |
| [**QueryProcessAffinityUpdateMode**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queryprocessaffinityupdatemode) | 抓取指定進程的親和性更新模式。                                                                                                                                  |
| [**QueryProcessCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryprocesscycletime)                   | 抓取指定進程之所有線程的週期時間總和。                                                                                                                  |
| [**SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable)                 | 設定目前進程的環境變數值。                                                                                                                            |
| [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass)                             | 設定指定進程的優先權類別。                                                                                                                                            |
| [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask)                 | 設定指定進程之執行緒的處理器親和性遮罩。                                                                                                                        |
| [**SetProcessAffinityUpdateMode**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessaffinityupdatemode)     | 設定指定進程的親和性更新模式。                                                                                                                                       |
| [**SetProcessInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessinformation)                   | 設定指定進程的資訊。                                                                                                                                                   |
| [**SetProcessMitigationPolicy**](/windows/desktop/api/Processthreadsapi/nf-processthreadsapi-setprocessmitigationpolicy)         | 設定呼叫進程的風險降低原則。                                                                                                                                           |
| [**SetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost)               | 停用系統暫時提高指定進程之執行緒優先順序的能力。                                                                                 |
| [**SetProcessRestrictionExemption**](/windows/desktop/api/Winuser/nf-winuser-setprocessrestrictionexemption) | 從防止桌面進程與 Windows Store 應用程式環境互動的限制中豁免呼叫進程。 開發和偵錯工具會使用這個函式。 |
| [**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters)     | 設定目前呼叫進程的關機參數。                                                                                                                                   |
| [**SetProcessWorkingSetSize**](/windows/desktop/api/WinBase/nf-winbase-setprocessworkingsetsize)             | 設定指定進程的最小和最大工作集大小。                                                                                                                     |
| [**SetProcessWorkingSetSizeEx**](/windows/win32/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex)         | 設定指定進程的最小和最大工作集大小。                                                                                                                     |
| [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)                             | 終止指定的進程及其所有線程。                                                                                                                                      |



 

## <a name="process-enumeration-functions"></a>處理列舉函數

下列函數用來列舉進程。



| 函式                                                    | 描述                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | 抓取系統中每個處理常式物件的處理序識別碼。            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | 抓取系統快照中所發生第一個進程的相關資訊。    |
| [**Process32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | 抓取系統快照中所記錄之下一個進程的相關資訊。        |
| [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | 抓取指定終端機伺服器上使用中進程的相關資訊。 |



 

## <a name="policy-functions"></a>原則函數

下列函式適用于整個進程的原則。



|                                                      |                                                       |
|------------------------------------------------------|-------------------------------------------------------|
| 函式                                             | 描述                                           |
| [**QueryProtectedPolicy**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queryprotectedpolicy) | 查詢與受保護原則相關聯的值。 |
| [**SetProtectedPolicy**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprotectedpolicy)     | 設定受保護的原則。                              |



 

## <a name="thread-functions"></a>執行緒函數

下列函式會搭配 [執行緒](multiple-threads.md)使用。



| 函式                                                           | 描述                                                                                                                                               |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput)                     | 將一個執行緒的輸入處理機制附加至另一個執行緒的。                                                                          |
| [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)                   | 建立在另一個進程的虛擬位址空間中執行的執行緒。                                                                               |
| [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)               | 建立在另一個進程的虛擬位址空間中執行的執行緒，並選擇性地指定擴充屬性，例如處理器群組親和性。 |
| [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)                               | 建立要在呼叫進程的虛擬位址空間內執行的執行緒。                                                                      |
| [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)                                   | 結束呼叫的執行緒。                                                                                                                                  |
| [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread)                       | 抓取目前線程的虛擬控制碼。                                                                                                         |
| [**GetCurrentThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadid)                   | 抓取呼叫執行緒的執行緒識別碼。                                                                                                    |
| [**GetExitCodeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread)                     | 捕獲指定之執行緒的終止狀態。                                                                                                 |
| [**GetThreadDescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-getthreaddescription)               | 藉由呼叫 [**>setthreaddescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-setthreaddescription)來抓取指派給執行緒的描述。                                  |
| [**GetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)           | 抓取指定之執行緒的處理器群組親和性。                                                                                           |
| [**GetThreadId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadid)                                 | 抓取指定之執行緒的執行緒識別碼。                                                                                                  |
| [**GetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)     | 抓取指定執行緒的理想處理器處理器編號。                                                                           |
| [**GetThreadInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadinformation)               | 抓取指定之執行緒的相關資訊。                                                                                                         |
| [**GetThreadIOPendingFlag**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadiopendingflag)           | 判斷指定的執行緒是否有任何待處理的 i/o 要求。                                                                                       |
| [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority)                     | 抓取指定之執行緒的優先順序值。                                                                                                    |
| [**GetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost)           | 抓取指定之執行緒的優先權提升控制狀態。                                                                                       |
| [**GetThreadTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadtimes)                           | 取得指定之執行緒的計時資訊。                                                                                                    |
| [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)                                   | 開啟現有的執行緒物件。                                                                                                                          |
| [**QueryIdleProcessorCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime) | 抓取系統中每個處理器閒置執行緒的週期時間。                                                                             |
| [**QueryThreadCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-querythreadcycletime)               | 抓取指定執行緒的週期時間。                                                                                                        |
| [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread)                               | 遞減執行緒的暫停計數。                                                                                                                      |
| [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask)             | 設定指定之執行緒的處理器親和性遮罩。                                                                                                  |
| [**>setthreaddescription**](/windows/desktop/api/ProcessThreadsApi/nf-processthreadsapi-setthreaddescription)               | 將描述指派給執行緒。                                                                                                                        |
| [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)           | 設定指定之執行緒的處理器群組親和性。                                                                                               |
| [**SetThreadIdealProcessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor)         | 指定執行緒的慣用處理器。                                                                                                             |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)     | 設定指定執行緒的理想處理器，並選擇性地取出先前的理想處理器。                                                  |
| [**SetThreadInformation**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadinformation)               | 設定指定之執行緒的資訊。                                                                                                                |
| [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority)                     | 設定指定之執行緒的優先順序值。                                                                                                         |
| [**SetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost)           | 停用系統暫時提高執行緒優先順序的能力。                                                                         |
| [**SetThreadStackGuarantee**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee)         | 設定呼叫執行緒的堆疊保證。                                                                                                          |
| [**睡眠**](/windows/win32/api/synchapi/nf-synchapi-sleep)                                             | 針對指定的間隔暫停執行目前的執行緒。                                                                                    |
| [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)                                         | 暫停目前的執行緒，直到符合指定的條件為止。                                                                                         |
| [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread)                             | 暫停指定的執行緒。                                                                                                                            |
| [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)                           | 造成呼叫執行緒執行目前處理器上已就緒可執行的其他執行緒。                                             |
| [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)                         | 終止執行緒。                                                                                                                                      |
| [**ThreadProc**](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))                                   | 應用程式定義的函數，做為執行緒的起始位址。                                                                         |
| [**TlsAlloc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc)                                       |  (TLS) 索引配置執行緒區域儲存區。                                                                                                             |
| [**TlsFree**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree)                                         | 釋放 TLS 索引。                                                                                                                                     |
| [**TlsGetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue)                                 | 針對指定的 TLS 索引，抓取呼叫執行緒的 TLS 位置中的值。                                                                           |
| [**TlsSetValue**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue)                                 | 針對指定的 TLS 索引，將值儲存在呼叫執行緒的 TLS 插槽中。                                                                                |
| [**WaitForInputIdle**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle)                       | 等到指定的進程正在等候使用者輸入，但未擱置任何輸入，或直到逾時間隔經過為止。                            |



 

## <a name="process-and-thread-extended-attribute-functions"></a>進程和執行緒擴充屬性函式

下列函數用來設定進程和執行緒建立的擴充屬性。



| 函式                                                                       | 描述                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DeleteProcThreadAttributeList**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-deleteprocthreadattributelist)         | 針對進程和執行緒建立，刪除指定的屬性清單。                            |
| [**InitializeProcThreadAttributeList**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist) | 初始化指定的屬性清單，以便建立進程和執行緒。                        |
| [**UpdateProcThreadAttribute**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute)                 | 在指定的屬性清單中，更新指定的屬性，以便建立進程和執行緒。 |



 

## <a name="wow64-functions"></a>WOW64 函數

下列函式可用於 [WOW64](../winprog64/running-32-bit-applications.md)。



| 函式                                         | 描述                                                                                                                            |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**IsWow64Message**](/windows/desktop/api/Winuser/nf-winuser-iswow64message)         | 判斷從目前線程的佇列讀取的最後一個訊息是否源自于 WOW64 進程。                              |
| [**IsWow64Process**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process)         | 判斷指定的進程是否正在 WOW64 下執行。                                                                       |
| [**IsWow64Process2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2)       | 判斷指定的進程是否正在 WOW64 下執行;也會傳回額外的電腦進程和架構資訊。 |
| [**Wow64SuspendThread**](/windows/desktop/api/WinBase/nf-winbase-wow64suspendthread) | 暫停指定的 WOW64 執行緒。                                                                                                   |



 

## <a name="job-object-functions"></a>工作物件函數

下列函式可用於 [工作物件](job-objects.md)。



| 函式                                                       | 描述                                                                                          |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject)   | 將處理常式與現有的工作物件產生關聯。                                                    |
| [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta)                     | 建立或開啟工作物件。                                                                       |
| [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob)                       | 判斷進程是否正在指定的作業中執行。                                      |
| [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta)                         | 開啟現有的工作物件。                                                                        |
| [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) | 從工作物件中抓取限制和作業狀態資訊。                                       |
| [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)     | 設定工作物件的限制。                                                                         |
| [**TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject)               | 終止目前與作業相關聯的所有進程。                                          |
| [**UserHandleGrantAccess**](/windows/desktop/api/Winuser/nf-winuser-userhandlegrantaccess)         | 授與或拒絕對使用者物件之控制碼的存取權，以存取具有使用者介面限制的作業。 |



 

## <a name="thread-pool-functions"></a>執行緒集區函數

下列函式會搭配 [執行緒](thread-pools.md)集區使用。



| 函式                                                                                   | 描述                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallbackMayRunLong**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-callbackmayrunlong)                                           | 指出回呼可能不會快速傳回。                                                                                                                                                                                                 |
| [**CancelThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-cancelthreadpoolio)                                           | 取消 [**StartThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio) 函數的通知。                                                                                                                                                          |
| [**CloseThreadpool**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpool)                                                 | 關閉指定的執行緒集區。                                                                                                                                                                                                                   |
| [**CloseThreadpoolCleanupGroup**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroup)                         | 關閉指定的清除群組。                                                                                                                                                                                                                 |
| [**CloseThreadpoolCleanupGroupMembers**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolcleanupgroupmembers)           | 釋放指定之清除群組的成員、等候所有回呼函式完成，並選擇性地取消任何未處理的回呼函數。                                                                                       |
| [**CloseThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolio)                                             | 釋放指定的 i/o 完成物件。                                                                                                                                                                                                       |
| [**CloseThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpooltimer)                                       | 釋放指定的計時器物件。                                                                                                                                                                                                                |
| [**CloseThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwait)                                         | 釋放指定的等候物件。                                                                                                                                                                                                                 |
| [**CloseThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolwork)                                         | 釋放指定的工作物件。                                                                                                                                                                                                                 |
| [**CreateThreadpool**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool)                                               | 配置新的執行緒集區以執行回呼。                                                                                                                                                                                               |
| [**CreateThreadpoolCleanupGroup**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolcleanupgroup)                       | 建立可讓應用程式用來追蹤一或多個執行緒集區回呼的清除群組。                                                                                                                                                       |
| [**CreateThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio)                                           | 建立新的 i/o 完成物件。                                                                                                                                                                                                                |
| [**CreateThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer)                                     | 建立新的計時器物件。                                                                                                                                                                                                                         |
| [**CreateThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwait)                                       | 建立新的等候物件。                                                                                                                                                                                                                          |
| [**CreateThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolwork)                                       | 建立新的工作物件。                                                                                                                                                                                                                          |
| [**DestroyThreadpoolEnvironment**](/windows/desktop/api/WinBase/nf-winbase-destroythreadpoolenvironment)                       | 刪除指定的回呼環境。 如果不再需要回呼環境來建立新的執行緒集區物件，請呼叫此函式。                                                                                              |
| [**DisassociateCurrentThreadFromCallback**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-disassociatecurrentthreadfromcallback)     | 移除目前執行中回呼函式與起始回呼的物件之間的關聯。 目前的執行緒將不會再以代表物件執行回呼的方式計算。                                      |
| [**FreeLibraryWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-freelibrarywhencallbackreturns)                   | 指定當目前的回呼完成時，執行緒集區將卸載的 DLL。                                                                                                                                                             |
| [**InitializeThreadpoolEnvironment**](/windows/desktop/api/WinBase/nf-winbase-initializethreadpoolenvironment)                 | 初始化回呼環境。                                                                                                                                                                                                                 |
| [**IsThreadpoolTimerSet**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-isthreadpooltimerset)                                       | 判斷指定的計時器物件目前是否已設定。                                                                                                                                                                                     |
| [**LeaveCriticalSectionWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-leavecriticalsectionwhencallbackreturns) | 指定當目前的回呼完成時，執行緒集區將釋放的重要區段。                                                                                                                                               |
| [**QueryThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)                 | 抓取指定執行緒集區中線程的堆疊保留和認可大小。                                                                                                                                                              |
| [**ReleaseMutexWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-releasemutexwhencallbackreturns)                 | 指定當目前的回呼完成時，執行緒集區將釋放的 mutex。                                                                                                                                                          |
| [**ReleaseSemaphoreWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-releasesemaphorewhencallbackreturns)         | 指定當目前的回呼完成時，執行緒集區將釋放的信號。                                                                                                                                                      |
| [**SetEventWhenCallbackReturns**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-seteventwhencallbackreturns)                         | 指定當目前的回呼完成時，執行緒集區將設定的事件。                                                                                                                                                              |
| [**SetThreadpoolCallbackCleanupGroup**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackcleanupgroup)             | 將指定的清除群組與指定的回呼環境產生關聯。                                                                                                                                                                     |
| [**SetThreadpoolCallbackLibrary**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbacklibrary)                       | 確定指定的 DLL 維持載入狀態，只要有未處理的回呼。                                                                                                                                                           |
| [**SetThreadpoolCallbackPersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)                 | 指定回呼應該在持續性執行緒上執行。                                                                                                                                                                                      |
| [**SetThreadpoolCallbackPool**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpool)                             | 設定產生回呼時要使用的執行緒集區。                                                                                                                                                                                          |
| [**SetThreadpoolCallbackPriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)                     | 指定相對於相同執行緒集區中其他工作專案的回呼函式優先權。                                                                                                                                                 |
| [**SetThreadpoolCallbackRunsLong**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackrunslong)                     | 指出與此回呼環境相關聯的回呼可能無法快速傳回。                                                                                                                                                          |
| [**SetThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)                     | 設定指定執行緒集區中新執行緒的堆疊保留和認可大小。                                                                                                                                                               |
| [**SetThreadpoolThreadMaximum**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadmaximum)                           | 設定指定的執行緒集區可以配置以處理回呼的執行緒數目上限。                                                                                                                                                |
| [**SetThreadpoolThreadMinimum**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolthreadminimum)                           | 設定指定的執行緒集區必須可用以處理回呼的執行緒數目下限。                                                                                                                                         |
| [**SetThreadpoolTimerEx**](/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimerex)                                       | 設定計時器物件。 背景工作執行緒會在指定的超時時間過期之後，呼叫計時器物件的回呼。                                                                                                                                       |
| [**SetThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpooltimer)                                           | 設定計時器物件。 背景工作執行緒會在指定的超時時間過期之後，呼叫計時器物件的回呼。                                                                                                                                       |
| [**SetThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait)                                             | 設定等候物件。 當控制碼變成發出信號或指定的超時時間過期之後，背景工作執行緒會呼叫等候物件的回呼函數。                                                                                           |
| [**SetThreadpoolWaitEx**](/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwaitex)                                         | 設定等候物件。 當控制碼變成發出信號或指定的超時時間過期之後，背景工作執行緒會呼叫等候物件的回呼函數。                                                                                           |
| [**StartThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio)                                             | 通知執行緒集區，i/o 作業可能會從指定的 i/o 完成物件開始。 在系結至此物件的檔案控制代碼上完成作業之後，背景工作執行緒會呼叫 i/o 完成物件的回呼函式。 |
| [**SubmitThreadpoolWork**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-submitthreadpoolwork)                                       | 將工作物件張貼到執行緒集區。 背景工作執行緒會呼叫工作物件的回呼函數。                                                                                                                                                  |
| [**TpInitializeCallbackEnviron**](/windows/desktop/api/winnt/nf-winnt-tpinitializecallbackenviron)                         | 初始化執行緒集區的回呼環境。                                                                                                                                                                                             |
| [**TpDestroyCallbackEnviron**](/windows/desktop/api/winnt/nf-winnt-tpdestroycallbackenviron)                               | 刪除指定的回呼環境。 如果不再需要回呼環境來建立新的執行緒集區物件，請呼叫此函式。                                                                                              |
| [**TpSetCallbackActivationCoNtext**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackactivationcontext)                   | 將啟用內容指派給回呼環境。                                                                                                                                                                                          |
| [**TpSetCallbackCleanupGroup**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackcleanupgroup)                             | 將指定的清除群組與指定的回呼環境產生關聯。                                                                                                                                                                     |
| [**TpSetCallbackFinalizationCallback**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackfinalizationcallback)             | 指出完成回呼環境時要呼叫的函式。                                                                                                                                                                            |
| [**TpSetCallbackLongFunction**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbacklongfunction)                             | 指出與此回呼環境相關聯的回呼可能無法快速傳回。                                                                                                                                                          |
| [**TpSetCallbackNoActivationCoNtext**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbacknoactivationcontext)               | 指出回呼環境沒有啟用內容。                                                                                                                                                                                  |
| [**TpSetCallbackPersistent**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpersistent)                                 | 指定回呼應該在持續性執行緒上執行。                                                                                                                                                                                      |
| [**TpSetCallbackPriority**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackpriority)                                     | 指定相對於相同執行緒集區中其他工作專案的回呼函式優先權。                                                                                                                                                 |
| [**TpSetCallbackRaceWithDll**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackracewithdll)                               | 確定指定的 DLL 維持載入狀態，只要有未處理的回呼。                                                                                                                                                           |
| [**TpSetCallbackThreadpool**](/windows/desktop/api/winnt/nf-winnt-tpsetcallbackthreadpool)                                 | 將執行緒集區指派給回呼環境。                                                                                                                                                                                                    |
| [**TrySubmitThreadpoolCallback**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-trysubmitthreadpoolcallback)                         | 要求執行緒集區背景工作執行緒呼叫指定的回呼函數。                                                                                                                                                                     |
| [**WaitForThreadpoolIoCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooliocallbacks)                       | 等候未完成的 i/o 完成回呼完成，並選擇性地取消尚未開始執行的擱置中回呼。                                                                                                           |
| [**WaitForThreadpoolTimerCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooltimercallbacks)                 | 等候未完成的計時器回呼完成，並選擇性地取消尚未開始執行的擱置中回呼。                                                                                                                    |
| [**WaitForThreadpoolWaitCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolwaitcallbacks)                   | 等候未完成的等候回呼完成，並選擇性地取消尚未開始執行的擱置中回呼。                                                                                                                     |
| [**WaitForThreadpoolWorkCallbacks**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpoolworkcallbacks)                   | 等候未完成的工作回呼完成，並選擇性地取消尚未開始執行的擱置中回呼。                                                                                                                     |



 

下列函數是原始 [執行緒](thread-pooling.md) 共用 API 的一部分。



| 函式                                                            | 描述                                                                                                                                                                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BindIoCompletionCallback**](/windows/desktop/api/WinBase/nf-winbase-bindiocompletioncallback)        | 使執行緒集區所擁有的 i/o 完成埠與指定的檔案控制代碼產生關聯。 當包含此檔案的 i/o 要求完成時，非 i/o 工作者執行緒將會執行指定的回呼函數。 |
| [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                      | 將工作專案排入執行緒集區中的背景工作執行緒佇列。                                                                                                                                                              |
| [**RegisterWaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) | 指示執行緒集區中的等候執行緒等候物件。                                                                                                                                                        |
| [**UnregisterWaitEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-unregisterwaitex)                       | 等候一個或所有指定的物件處於已發出信號的狀態，或超過逾時間隔。                                                                                                            |



 

## <a name="thread-ordering-service-functions"></a>執行緒排序服務函式

下列函式會搭配 [執行緒順序服務](thread-ordering-service.md)使用。



| 函式                                                                   | 描述                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**AvQuerySystemResponsiveness**](/windows/desktop/api/Avrt/nf-avrt-avquerysystemresponsiveness)         | 抓取多媒體類別排程器服務所使用的系統回應性設定。 |
| [**AvRtCreateThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroup)     | 建立執行緒排序群組。                                                            |
| [**AvRtCreateThreadOrderingGroupEx**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroupexa) | 建立執行緒排序群組，並將伺服器執行緒與工作產生關聯。               |
| [**AvRtDeleteThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtdeletethreadorderinggroup)     | 刪除呼叫端所建立的指定執行緒排序群組。                          |
| [**AvRtJoinThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtjointhreadorderinggroup)         | 將用戶端執行緒加入執行緒排序群組。                                            |
| [**AvRtLeaveThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtleavethreadorderinggroup)       | 讓用戶端執行緒離開執行緒順序群組。                                    |
| [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup)     | 讓執行緒排列群組的用戶端執行緒等候，直到它們應該執行為止。        |



 

## <a name="multimedia-class-scheduler-service-functions"></a>多媒體類別排程器服務函數

下列函式會搭配 [多媒體類別](multimedia-class-scheduler-service.md)排程器服務使用。



| 函式                                                                   | 描述                                                                                           |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**AvRevertMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avrevertmmthreadcharacteristics) | 表示執行緒已不再執行與指定之工作相關聯的工作。              |
| [**AvSetMmMaxThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) | 將呼叫執行緒與指定的工作產生關聯。                                               |
| [**AvSetMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa)       | 將呼叫執行緒與指定的工作產生關聯。                                                |
| [**AvSetMmThreadPriority**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority)                     | 調整呼叫執行緒相對於執行相同工作的其他執行緒的執行緒優先權。 |



 

## <a name="fiber-functions"></a>光纖函數

下列函式會搭配使用於 [纖維](fibers.md)。



| 函式                                                 | 描述                                                                                                  |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**ConvertFiberToThread**](/windows/desktop/api/WinBase/nf-winbase-convertfibertothread)     | 將目前的光纖轉換為執行緒。                                                                    |
| [**ConvertThreadToFiber**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber)     | 將目前的執行緒轉換成光纖。                                                                    |
| [**ConvertThreadToFiberEx**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiberex) | 將目前的執行緒轉換成光纖。                                                                    |
| [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber)                       | 配置光纖物件、將堆疊指派給它，並將執行設定為從指定的起始位址開始。 |
| [**CreateFiberEx**](/windows/desktop/api/WinBase/nf-winbase-createfiberex)                   | 配置光纖物件、將堆疊指派給它，並將執行設定為從指定的起始位址開始。 |
| [**DeleteFiber**](/windows/desktop/api/WinBase/nf-winbase-deletefiber)                       | 刪除現有的光纖。                                                                                   |
| [**FiberProc**](/windows/win32/api/winbase/nc-winbase-pfiber_start_routine)                           | 搭配 [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber) 函數使用的應用程式定義函數。                   |
| [**FlsAlloc**](/windows/win32/api/fibersapi/nf-fibersapi-flsalloc)                             | 配置光纖本機儲存體 (FLS) 索引。                                                                 |
| [**FlsFree**](/windows/win32/api/fibersapi/nf-fibersapi-flsfree)                               | 釋放 FLS 索引。                                                                                       |
| [**FlsGetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flsgetvalue)                       | 針對指定的 FLS 索引，抓取呼叫光纖的 FLS 位置中的值。                               |
| [**FlsSetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flssetvalue)                       | 針對指定的 FLS 索引，將值儲存在呼叫光纖的 FLS 插槽中。                                    |
| [**IsThreadAFiber**](/windows/win32/api/fibersapi/nf-fibersapi-isthreadafiber)                 | 判斷目前的執行緒是否為光纖。                                                            |
| [**SwitchToFiber**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber)                   | 排定光纖。                                                                                           |



 

## <a name="numa-support-functions"></a>NUMA 支援函式

下列函數提供 [NUMA 支援](numa-support.md)。



| 函式                                                                 | 描述                                                                                                                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)  | 保留或認可指定進程的虛擬位址空間內的記憶體區域，並指定實體記憶體的 NUMA 節點。 |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) | 抓取邏輯處理器和相關硬體的相關資訊。                                                                                   |
| [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)         | 抓取指定節點中的可用記憶體數量。                                                                                        |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)     | 將指定節點中可用的記憶體數量，抓取為 USHORT 值。                                                              |
| [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)             | 抓取目前具有最大數目的節點。                                                                                              |
| [**GetNumaNodeNumberFromHandle**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)       | 抓取與基礎裝置相關聯的 NUMA 節點以取得檔案控制代碼。                                                                       |
| [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)             | 抓取指定節點的處理器遮罩。                                                                                                   |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)         | 將指定之 NUMA 節點的處理器遮罩抓取為 USHORT 值。                                                                            |
| [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                     | 抓取指定處理器的節點編號。                                                                                                 |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                 | 以 USHORT 值形式抓取指定之邏輯處理器的節點編號。                                                                        |
| [**GetNumaProximityNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                     | 抓取指定的相近識別碼的節點編號。                                                                                      |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                 | 將節點編號抓取為指定之相近識別碼的 USHORT 值。                                                                    |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                        | 保留或認可指定進程的虛擬位址空間內的記憶體區域，並指定實體記憶體的 NUMA 節點。 |



 

## <a name="processor-functions"></a>處理器函數

下列函式適用于邏輯處理器和 [處理器群組](processor-groups.md)。



| 函式                                                                     | 描述                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**GetActiveProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)                   | 傳回處理器群組或系統中的作用中處理器數目。                                       |
| [**GetActiveProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)         | 傳回系統中的作用中處理器群組數目。                                                         |
| [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber)               | 在呼叫此函式期間，抓取目前線程正在其上執行的處理器數目。            |
| [**GetCurrentProcessorNumberEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)           | 抓取處理器群組和呼叫執行緒執行所在的邏輯處理器數目。            |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | 抓取邏輯處理器和相關硬體的相關資訊。                                                 |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | 抓取邏輯處理器和相關硬體關聯性的相關資訊。                            |
| [**GetMaximumProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)                 | 傳回處理器群組或系統可以擁有的邏輯處理器最大數目。                      |
| [**GetMaximumProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)       | 傳回系統可以擁有之處理器群組的最大數目。                                             |
| [**QueryIdleProcessorCycleTime**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletime)           | 抓取系統中每個處理器閒置執行緒的週期時間。                                        |
| [**QueryIdleProcessorCycleTimeEx**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)       | 抓取指定處理器群組中每個邏輯處理器上閒置執行緒的累積週期時間。 |



 

## <a name="user-mode-scheduling-functions"></a>User-Mode 排程函數

下列函式會搭配使用者模式排程使用 (UMS) 。



| 函式                                                               | 描述                                                                                               |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)             | 建立 UMS 完成清單。                                                                            |
| [**CreateUmsThreadCoNtext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)               | 建立 UMS 執行緒內容以表示 UMS 背景工作執行緒。                                            |
| [**DeleteUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)             | 刪除指定的 UMS 完成清單。 清單必須是空的。                                        |
| [**DeleteUmsThreadCoNtext**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)               | 刪除指定的 UMS 執行緒內容。 必須終止執行緒。                                  |
| [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) | 從指定的 UMS 完成清單抓取 UMS 背景工作執行緒。                                      |
| [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)               | 將呼叫執行緒轉換成 UMS 排程器執行緒。                                                  |
| [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)                           | 執行指定的 UMS 背景工作執行緒。                                                                     |
| [**GetCurrentUmsThread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)                     | 傳回呼叫的 UMS 執行緒的 UMS 執行緒內容。                                                 |
| [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)                       | 傳回 UMS 執行緒內容清單中的下一個 UMS 執行緒內容。                                     |
| [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)         | 抓取與指定的 UMS 完成清單相關聯之事件的控制碼。                        |
| [**GetUmsSystemThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-getumssystemthreadinformation) | 查詢指定的執行緒是否為 UMS 排程器執行緒、UMS 背景工作執行緒或非 UMS 執行緒。 |
| [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)         | 抓取指定的 UMS 工作者執行緒的相關資訊。                                              |
| [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)             | 設定指定的 UMS 工作者執行緒的應用程式特定內容資訊。                        |
| [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)                             | 與 UMS 完成清單相關聯的應用程式定義的 UMS 排程器進入點函數。         |
| [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)                               | 將控制權產生給呼叫的 UMS 工作者執行緒執行所在的 UMS 排程器執行緒。             |



 

## <a name="obsolete-functions"></a>過時的函式

-   [**NtGetCurrentProcessorNumber**](ntgetcurrentprocessornumber.md)
-   [**NtQueryInformationProcess**](/windows/desktop/api/Winternl/nf-winternl-ntqueryinformationprocess)
-   [**NtQueryInformationThread**](/windows/desktop/api/Winternl/nf-winternl-ntqueryinformationthread)
-   [**WinExec**](/windows/desktop/api/WinBase/nf-winbase-winexec)
-   [**ZwQueryInformationProcess**](zwqueryinformationprocess.md)

 

 
