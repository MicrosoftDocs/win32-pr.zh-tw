---
description: Windows 7 和 Windows Server 2008 R2 包含下列程式和執行緒的新程式設計項目。
ms.assetid: 69cd8713-b40c-4fec-a256-9c2ee3d73da5
title: 進程和執行緒的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7dfb708a2890bab1fcd3fd66385f74bd8513b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849254"
---
# <a name="whats-new-in-processes-and-threads"></a>進程和執行緒的新功能

Windows 7 和 Windows Server 2008 R2 包含下列程式和執行緒的新程式設計項目。

## <a name="new-capabilities"></a>新功能

64位版本的 Windows 7 和 Windows Server 2008 R2 在單一電腦上支援超過64個邏輯處理器。 如需詳細資訊，請參閱 [處理器群組](processor-groups.md)。

使用者模式排程 (UMS) 是一種輕量的機制，可讓應用程式用來排程自己的執行緒。 如需詳細資訊，請參閱 [使用者模式排程](user-mode-scheduling.md)。

## <a name="new-functions"></a>新函式

下列新功能可用於處理器和處理器群組。



| 函式                                                                                | 描述                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex)<br/>                         | 建立在另一個進程的虛擬位址空間中執行的執行緒，並選擇性地指定擴充屬性，例如處理器群組親和性。<br/> |
| [**GetActiveProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorcount)<br/>                   | 傳回處理器群組或系統中的作用中處理器數目。<br/>                                                                            |
| [**GetActiveProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getactiveprocessorgroupcount)<br/>         | 傳回系統中的作用中處理器群組數目。<br/>                                                                                              |
| [**GetCurrentProcessorNumberEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumberex)<br/>           | 抓取處理器群組和呼叫執行緒執行所在的邏輯處理器數目。<br/>                                                 |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex)<br/> | 抓取邏輯處理器和相關硬體關聯性的相關資訊。<br/>                                                                 |
| [**GetMaximumProcessorCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorcount)<br/>                 | 傳回處理器群組或系統可以擁有的邏輯處理器最大數目。<br/>                                                           |
| [**GetMaximumProcessorGroupCount**](/windows/desktop/api/WinBase/nf-winbase-getmaximumprocessorgroupcount)<br/>       | 傳回系統可以擁有之處理器群組的最大數目。 <br/>                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)<br/>         | 將指定節點中可用的記憶體數量，抓取為 USHORT 值。<br/>                                                                 |
| [**GetNumaNodeNumberFromHandle**](/windows/desktop/api/WinBase/nf-winbase-getnumanodenumberfromhandle)<br/>           | 抓取與基礎裝置相關聯的 NUMA 節點以取得檔案控制代碼。<br/>                                                                          |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)<br/>             | 將指定之 NUMA 節點的處理器遮罩抓取為 USHORT 值。<br/>                                                                               |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)<br/>                     | 以 USHORT 值形式抓取指定之邏輯處理器的節點編號。<br/>                                                                           |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)<br/>                     | 將節點編號抓取為指定之相近識別碼的 USHORT 值。<br/>                                                                       |
| [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity)<br/>                   | 抓取指定進程的處理器群組親和性。<br/>                                                                                          |
| [**GetProcessorSystemCycleTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getprocessorsystemcycletime)<br/>           | 抓取指定群組中每個處理器執行延遲程序呼叫所花費的週期時間， (Dpc) 和插斷服務常式 (Isr) 。<br/>     |
| [**GetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity)<br/>                     | 抓取指定之執行緒的處理器群組親和性。<br/>                                                                                           |
| [**GetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadidealprocessorex)<br/>               | 抓取指定執行緒的理想處理器處理器編號。<br/>                                                                           |
| [**QueryIdleProcessorCycleTimeEx**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryidleprocessorcycletimeex)<br/>       | 抓取指定處理器群組中每個邏輯處理器上閒置執行緒的累積週期時間。 <br/>                                     |
| [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity)<br/>                     | 設定指定之執行緒的處理器群組親和性。<br/>                                                                                               |
| [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex)<br/>               | 設定指定執行緒的理想處理器，並選擇性地取出先前的理想處理器。<br/>                                                  |



 

下列新函數會搭配執行緒集區使用。



| 函式                                                                              | 描述                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**QueryThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation)<br/> | 抓取指定執行緒集區中線程的堆疊保留和認可大小。<br/>              |
| [**SetThreadpoolCallbackPersistent**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpersistent)<br/> | 指定回呼應該在持續性執行緒上執行。<br/>                                      |
| [**SetThreadpoolCallbackPriority**](/windows/desktop/api/WinBase/nf-winbase-setthreadpoolcallbackpriority)<br/>     | 指定相對於相同執行緒集區中其他工作專案的回呼函式優先權。<br/> |
| [**SetThreadpoolStackInformation**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolstackinformation)<br/>     | 設定指定執行緒集區中新執行緒的堆疊保留和認可大小。 <br/>              |



 

下列新函數可搭配 UMS 使用。



| 函式                                                                          | 描述                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist)<br/>             | 建立 UMS 完成清單。<br/>                                                                     |
| [**CreateUmsThreadCoNtext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)<br/>               | 建立 UMS 執行緒內容以表示 UMS 背景工作執行緒。<br/>                                     |
| [**DeleteUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-deleteumscompletionlist)<br/>             | 刪除指定的 UMS 完成清單。 清單必須是空的。<br/>                                 |
| [**DeleteUmsThreadCoNtext**](/windows/desktop/api/WinBase/nf-winbase-deleteumsthreadcontext)<br/>               | 刪除指定的 UMS 執行緒內容。 必須終止執行緒。<br/>                           |
| [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems)<br/> | 從指定的 UMS 完成清單抓取 UMS 背景工作執行緒。<br/>                               |
| [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)<br/>               | 將呼叫執行緒轉換成 UMS 排程器執行緒。<br/>                                           |
| [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread)<br/>                           | 執行指定的 UMS 背景工作執行緒。<br/>                                                              |
| [**GetCurrentUmsThread**](/windows/desktop/api/WinBase/nf-winbase-getcurrentumsthread)<br/>                     | 傳回呼叫的 UMS 執行緒的 UMS 執行緒內容。<br/>                                          |
| [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem)<br/>                       | 傳回 UMS 執行緒內容清單中的下一個 UMS 執行緒內容。<br/>                              |
| [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)<br/>         | 抓取與指定的 UMS 完成清單相關聯之事件的控制碼。<br/>                 |
| [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation)<br/>         | 抓取指定的 UMS 工作者執行緒的相關資訊。<br/>                                       |
| [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation)<br/>             | 設定指定的 UMS 工作者執行緒的應用程式特定內容資訊。<br/>                 |
| [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)<br/>                             | 與 UMS 完成清單相關聯的應用程式定義的 UMS 排程器進入點函數。 <br/> |
| [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)<br/>                               | 將控制權產生給呼叫的 UMS 工作者執行緒執行所在的 UMS 排程器執行緒。<br/>      |



 

## <a name="new-structures"></a>新結構



| 結構                                                                                                 | Description                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**快取 \_ 關聯性**](/windows/desktop/api/WinNT/ns-winnt-cache_relationship)<br/>                                              | 描述快取屬性。 <br/>                                                             |
| [**群組 \_ 親和性**](/windows/desktop/api/WinNT/ns-winnt-group_affinity)<br/>                                                      | 包含處理器群組特有的親和性，例如執行緒的親和性。<br/>          |
| [**群組 \_ 關聯性**](/windows/desktop/api/WinNT/ns-winnt-group_relationship)<br/>                                              | 包含處理器群組的相關資訊。 <br/>                                            |
| [**NUMA \_ 節點 \_ 關聯性**](/windows/desktop/api/WinNT/ns-winnt-numa_node_relationship)<br/>                                     | 包含處理器群組中 NUMA 節點的相關資訊。 <br/>                            |
| [**處理器 \_ 群組 \_ 資訊**](/windows/desktop/api/WinNT/ns-winnt-processor_group_info)<br/>                                         | 包含處理器群組中處理器的數目與親和性。<br/>                     |
| [**處理器 \_ 編號**](/windows/desktop/api/WinNT/ns-winnt-processor_number)<br/>                                                  | 表示處理器群組中的邏輯處理器。<br/>                                     |
| [**處理器 \_ 關聯性**](/windows/desktop/api/WinNT/ns-winnt-processor_relationship)<br/>                                      | 包含處理器群組內親和性的相關資訊。<br/>                            |
| [**系統 \_ 邏輯 \_ 處理器 \_ 資訊， \_ 例如**](/windows/desktop/api/WinNT/ns-winnt-system_logical_processor_information_ex)<br/> | 包含邏輯處理器和相關硬體關聯性的相關資訊。<br/> |
| [**UMS \_ 建立 \_ 執行緒 \_ 屬性**](/windows/desktop/api/WinNT/ns-winnt-ums_create_thread_attributes)<br/>                        | 指定 UMS 工作者執行緒的屬性。 <br/>                                           |
| [**UMS 排程器 \_ \_ 啟動 \_ 資訊**](/windows/desktop/api/WinBase/ns-winbase-ums_scheduler_startup_info)<br/>                            | 指定 UMS 排程器執行緒的屬性<br/>                                          |



 

 

 
