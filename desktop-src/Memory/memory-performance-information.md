---
description: 記憶體效能資訊可透過系統效能計數器，以及透過 GetPerformanceInfo、GetProcessMemoryInfo 和 GlobalMemoryStatusEx 等函式，從記憶體管理員取得。
ms.assetid: b27ca747-8fd2-4267-9979-4e2e14a5a19f
title: 記憶體效能資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdef1cfeff57f26e7ee7eb92bd730a601598a4b4608191e38aeed3d9cc5b3d20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822138"
---
# <a name="memory-performance-information"></a>記憶體效能資訊

記憶體效能資訊可透過系統 [效能計數器](../perfctrs/performance-counters-portal.md) ，以及透過 [**GetPerformanceInfo**](/windows/win32/api/psapi/nf-psapi-getperformanceinfo)、 [**GetProcessMemoryInfo**](/windows/win32/api/psapi/nf-psapi-getprocessmemoryinfo)和 [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex)等函式，從記憶體管理員取得。 應用程式（例如 Windows 工作管理員、可靠性和效能監視器以及[Process Explorer](/sysinternals/downloads/process-explorer)工具）都會使用效能計數器來顯示系統和個別進程的記憶體資訊。

本主題會將效能計數器與記憶體效能函數和 Windows 工作管理員所傳回的資料產生關聯：

-   [系統記憶體效能資訊](#system-memory-performance-information)
-   [進程記憶體效能資訊](#process-memory-performance-information)
-   [相關主題](#related-topics)

## <a name="system-memory-performance-information"></a>系統記憶體效能資訊

下表將記憶體物件效能計數器與 [**MEMORYSTATUSEX**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-memorystatusex)、 [**效能 \_ 資訊**](/windows/win32/api/psapi/ns-psapi-performance_information)和 [**進程 \_ 記憶體 \_ 計數器 \_**](/windows/win32/api/psapi/ns-psapi-process_memory_counters_ex) 中的記憶體效能函數所傳回的資料產生關聯，以及使用工作管理員所顯示的對應資訊。



| 除非另有注明，否則記憶體物件計數器 ()                                                                                                                                                                                                                  | 結構                                                                                                                                                | Windows Server 2008 和 Windows Vista 的工作管理員效能] 索引標籤              | Windows Server 2003 和 Windows XP 的工作管理員效能] 索引標籤 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| 可用 KB                                                                                                                                                                                                                                                   | [**MEMORYSTATUSEX**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-memorystatusex)。**ullAvailPhys** 和 [**效能 \_ 資訊**](/windows/win32/api/psapi/ns-psapi-performance_information)。**PhysicalAvailable** | 從實體記憶體減去 **記憶體** 圖表中顯示的使用量值 **(MB) ：總計** | **實體記憶體：可用**                                      |
| 無                                                                                                                                                                                                                                                           | [**MEMORYSTATUSEX**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-memorystatusex)。**ullTotalPhys** 和 [**效能 \_ 資訊**](/windows/win32/api/psapi/ns-psapi-performance_information)。**PhysicalTotal**     | **實體記憶體 (MB) ：總計**                                                     | **實體記憶體：總計**                                          |
| 認可的位元組                                                                                                                                                                                                                                                | [**效能 \_資訊**](/windows/win32/api/psapi/ns-psapi-performance_information)。**CommitTotal**                                                                         | **System： Page File** first VALUE (MB)                                            | **認可費用：總計**                                            |
| 認可限制                                                                                                                                                                                                                                                   | [**MEMORYSTATUSEX**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-memorystatusex)。**ullTotalPageFile** 和 [**效能 \_ 資訊**](/windows/win32/api/psapi/ns-psapi-performance_information)。**CommitLimit**   | **System： Page File** second VALUE (MB)                                           | **認可費用：限制**                                            |
| 免費 & 零頁面清單位元組 **Windows 伺服器2003和 Windows XP：** 不支援此效能計數器。<br/>                                                                                                                                      | 無                                                                                                                                                     | **實體記憶體 (MB) ：免費**                                                      | 不適用                                                      |
| 無                                                                                                                                                                                                                                                           | [**效能 \_資訊**](/windows/win32/api/psapi/ns-psapi-performance_information)。**CommitPeak**                                                                          | 無                                                                                | **認可費用：尖峰**                                             |
| 無                                                                                                                                                                                                                                                           | [**效能 \_資訊**](/windows/win32/api/psapi/ns-psapi-performance_information)。**HandleCount**                                                                         | **系統：控制碼**                                                                 | **總計：控制碼**                                                 |
| 無                                                                                                                                                                                                                                                           | [**MEMORYSTATUSEX**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-memorystatusex)。**ullAvailPageFile**                                                                                        | 無                                                                                | 無                                                                |
| Pool Nonpaged Bytes                                                                                                                                                                                                                                            | [**效能 \_資訊**](/windows/win32/api/psapi/ns-psapi-performance_information)。**KernelNonpaged**                                                                      | **核心記憶體：非分頁**                                                         | **核心記憶體：非分頁**                                         |
| Pool Paged Bytes                                                                                                                                                                                                                                               | [**效能 \_資訊**](/windows/win32/api/psapi/ns-psapi-performance_information)。**KernelPaged**                                                                         | **核心記憶體：分頁**                                                            | **核心記憶體：分頁**                                            |
| 集區分頁位元組 + 集區未分頁位元組                                                                                                                                                                                                                         | [**效能 \_資訊**](/windows/win32/api/psapi/ns-psapi-performance_information)。**KernelTotal**                                                                         | **核心記憶體：總計**                                                            | **核心記憶體：總計**                                            |
| 處理 (物件物件)                                                                                                                                                                                                                                      | [**效能 \_資訊**](/windows/win32/api/psapi/ns-psapi-performance_information)。**ProcessCount**                                                                        | **系統：進程**                                                               | **總計：進程**                                               |
| 執行緒計數 (進程 (\_) 物件總數)                                                                                                                                                                                                                          | [**效能 \_資訊**](/windows/win32/api/psapi/ns-psapi-performance_information)。**ThreadCount**                                                                         | **系統：執行緒**                                                                 | **總計：執行緒**                                                 |
| 快取位元組 + 待命和修改清單上可共用的頁面                                                                                                                                                                                                 | [**效能 \_資訊**](/windows/win32/api/psapi/ns-psapi-performance_information)。**SystemCache**                                                                         | 無                                                                                | **系統快取**                                                    |
| 快取位元組 + 修改過的頁面清單位元組 + 待命快取保留字節 + 待命快取一般優先順序位元組 + 待命快取程式碼位元組 **Windows Server 2003 和 Windows XP：** 除了快取位元組以外，不支援這些效能計數器。<br/> | 無                                                                                                                                                     | **實體記憶體 (MB) ：快取**                                                    | 不適用                                                      |



 

## <a name="process-memory-performance-information"></a>進程記憶體效能資訊

下表將處理物件效能計數器與 [**MEMORYSTATUSEX**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-memorystatusex)、 [**效能 \_ 資訊**](/windows/win32/api/psapi/ns-psapi-performance_information)和 [**進程 \_ 記憶體 \_ 計數器 \_**](/windows/win32/api/psapi/ns-psapi-process_memory_counters_ex) 中的記憶體效能函數所傳回的資料產生關聯，以及使用工作管理員所顯示的對應資訊。



| Process 物件計數器                                                                                              | 結構                                                                                                 | Windows Server 2008 和 Windows Vista 的工作管理員進程] 索引標籤                                              | Windows Server 2003 和 Windows XP 的工作管理員進程] 索引標籤                                             |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 控制代碼計數                                                                                                        | 無                                                                                                      | **處理**                                                                                                       | **處理**                                                                                                   |
| 分頁檔位元組                                                                                                     | [**進程 \_記憶體 \_ 計數器， \_ 例如**](/windows/win32/api/psapi/ns-psapi-process_memory_counters_ex)**PagefileUsage**                    | 所有進程的 **認可大小**（系統進程除外）。 針對系統進程，分頁檔案位元組一律為0。 | 所有進程的 **VM 大小**（系統進程除外）。 針對系統進程，分頁檔案位元組一律為0。 |
| 分頁檔案位元組尖峰                                                                                                | [**進程 \_記憶體 \_ 計數器， \_ 例如**](/windows/win32/api/psapi/ns-psapi-process_memory_counters_ex)**PeakPagefileUsage**                | 無                                                                                                              | 無                                                                                                          |
| Pool Nonpaged Bytes                                                                                                 | [**進程 \_記憶體 \_ 計數器， \_ 例如**](/windows/win32/api/psapi/ns-psapi-process_memory_counters_ex)**QuotaNonPagedPoolUsage**           | **NP 集區**                                                                                                       | **NP 集區**                                                                                                   |
| Pool Paged Bytes                                                                                                    | [**進程 \_記憶體 \_ 計數器， \_ 例如**](/windows/win32/api/psapi/ns-psapi-process_memory_counters_ex)**QuotaPagedPoolUsage**              | **分頁集區**                                                                                                    | **分頁集區**                                                                                                |
| 私用位元組                                                                                                       | [**進程 \_記憶體 \_ 計數器， \_ 例如**](/windows/win32/api/psapi/ns-psapi-process_memory_counters_ex)**PrivateUsage**                     | **認可大小**                                                                                                   | **VM 大小**                                                                                                   |
|  (處理指定映射 () 的執行緒計數 <image name>)                                                   | 無                                                                                                      | **執行緒**                                                                                                       | **執行緒**                                                                                                   |
| 虛擬位元組                                                                                                       | [**MEMORYSTATUSEX**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-memorystatusex)。**ullTotalVirtual** – **MEMORYSTATUSEX**。**ullAvailVirtual** | 無                                                                                                              | 無                                                                                                          |
| Virtual Bytes Peak                                                                                                  | 無                                                                                                      | 無                                                                                                              | 無                                                                                                          |
| 工作集                                                                                                         | [**進程 \_記憶體 \_ 計數器， \_ 例如**](/windows/win32/api/psapi/ns-psapi-process_memory_counters_ex)**WorkingSetSize**                   | **工作集 (記憶體)**                                                                                          | **記憶體使用量**                                                                                                 |
| Working Set Peak                                                                                                    | [**進程 \_記憶體 \_ 計數器， \_ 例如**](/windows/win32/api/psapi/ns-psapi-process_memory_counters_ex)**PeakWorkingSetSize**               | **(記憶體) 的尖峰工作集**                                                                                     | **尖峰記憶體使用量**                                                                                            |
| 工作集-私用 **Windows Server 2003 和 Windows XP：** 不支援此效能計數器。<br/> | 無                                                                                                      | **私用工作集**                                                                                           | 不適用                                                                                                |
| 無                                                                                                                | [**進程 \_記憶體 \_ 計數器， \_ 例如**](/windows/win32/api/psapi/ns-psapi-process_memory_counters_ex)**QuotaPeakNonPagedPoolUsage**       | 無                                                                                                              | 無                                                                                                          |
| 無                                                                                                                | [**進程 \_記憶體 \_ 計數器， \_ 例如**](/windows/win32/api/psapi/ns-psapi-process_memory_counters_ex)**QuotaPeakPagedPoolUsage**          | 無                                                                                                              | 無                                                                                                          |
| 無                                                                                                                | [**MEMORYSTATUSEX**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-memorystatusex)。**ullAvailPageFile**                                         | 無                                                                                                              | 無                                                                                                          |
| 無                                                                                                                | [**MEMORYSTATUSEX**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-memorystatusex)。**ullTotalPageFile**                                         | 無                                                                                                              | 無                                                                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Memory 物件](/previous-versions/windows/it-pro/windows-server-2003/cc778082(v=ws.10))
</dt> <dt>

[Objects 物件](/previous-versions/windows/it-pro/windows-server-2003/cc785200(v=ws.10))
</dt> <dt>

[處理物件](/previous-versions/windows/it-pro/windows-server-2003/cc780836(v=ws.10))
</dt> <dt>

[Process Explorer 工具](/previous-versions/windows/it-pro/windows-xp/bb490960(v=technet.10))
</dt> </dl>

 

 
