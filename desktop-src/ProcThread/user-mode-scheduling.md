---
description: 使用者模式排程 (UMS) 是一種輕量的機制，可讓應用程式用來排程自己的執行緒。
ms.assetid: f9dd92fe-6d7a-452c-893e-e6df1757e377
title: User-Mode 排程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a13b30685dbcbfc4d3d502e02bdbfdc10d15ea1f804cc6a8391073c44ce447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074238"
---
# <a name="user-mode-scheduling"></a>User-Mode 排程

使用者模式排程 (UMS) 是一種輕量的機制，可讓應用程式用來排程自己的執行緒。 應用程式可以在使用者模式中的 UMS 執行緒之間切換，而不需要涉及 [系統](scheduling.md) 排程器，而且如果核心中的 ums 執行緒區塊，則會重新取得處理器的控制權。 UMS 執行緒與 [纖維](fibers.md) 不同之處在于，每個 ums 執行緒都有自己的執行緒內容，而不是共用單一執行緒的執行緒內容。 在使用者模式中切換執行緒的能力，讓 UMS 比 [執行緒](thread-pools.md) 集區更有效率，以管理需要少數系統呼叫的大量短時間工作專案。

如果應用程式需要高效能需求，且需要在多處理器或多核心系統上同時執行許多執行緒，則建議使用 UMS。 若要利用 UMS，應用程式必須執行排程器元件來管理應用程式的 UMS 執行緒，並判斷它們應該執行的時機。 開發人員應考慮其應用程式效能需求是否符合開發這類元件的相關工作。 具有中等效能需求的應用程式，可能會因為允許系統排程器排程其執行緒而提供更佳的服務。

UMS 適用于在64位版本的 Windows 7 和 Windows Server 2008 R2 或更新版本的 Windows 之64位版本上執行的64位應用程式。 這項功能不適用於32位版本的 Windows。

如需詳細資訊，請參閱下列各節：

-   [UMS 排程器](#ums-scheduler)
-   [UMS 排程器執行緒](#ums-scheduler-thread)
-   [UMS 背景工作執行緒、執行緒內容和完成清單](#ums-worker-threads-thread-contexts-and-completion-lists)
-   [UMS 排程器進入點函數](#ums-scheduler-entry-point-function)
-   [UMS 執行緒執行](#ums-thread-execution)
-   [UMS 最佳作法](#ums-best-practices)

## <a name="ums-scheduler"></a>UMS 排程器

應用程式的 UMS 排程器負責建立、管理及刪除 UMS 執行緒，以及判斷要執行的 UMS 執行緒。 應用程式的排程器會執行下列工作：

-   為每個處理器建立一個 UMS 排程器執行緒，應用程式將在其中執行 UMS 工作者執行緒。
-   建立 UMS 背景工作執行緒來執行應用程式的工作。
-   會針對已準備好執行的背景工作執行緒，維護自己的就緒執行緒佇列，並根據應用程式的排程原則選取要執行的執行緒。
-   建立並監視一或多個完成清單，其中系統會線上程完成核心處理之後將其排入佇列。 這包括新建立的背景工作執行緒，以及先前在被解除封鎖的系統呼叫上封鎖的執行緒。
-   提供排程器進入點函式，以處理來自系統的通知。 系統會在建立排程器執行緒、當背景工作執行緒在系統呼叫上封鎖，或當背景工作執行緒明確產生控制權時，呼叫進入點函數。
-   針對已完成執行的背景工作執行緒執行清除工作。
-   在應用程式要求時，執行排程器的有條理關機。

## <a name="ums-scheduler-thread"></a>UMS 排程器執行緒

UMS 排程器執行緒是透過呼叫 [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode) 函數，將本身轉換成 UMS 的一般執行緒。 系統排程器會判斷 UMS 排程器執行緒執行的時間，是根據其相對於其他就緒執行緒的優先權。 執行排程器執行緒的處理器會受到執行緒親和性的影響，與非 UMS 執行緒相同。

[**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)的呼叫端會指定完成清單以及與 UMS 排程器執行緒相關聯的 [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)進入點函數。 當系統完成將呼叫執行緒轉換成 UMS 時，系統會呼叫指定的進入點函數。 排程器進入點函數負責判斷指定執行緒的適當下一個動作。 如需詳細資訊，請參閱本主題稍後的 UMS 排程器 [進入點函數](#ums-scheduler-entry-point-function) 。

應用程式可能會為將用來執行 UMS 執行緒的每個處理器建立一個 UMS 排程器執行緒。 應用程式也可能會針對特定邏輯處理器，設定每個 UMS 排程器執行緒的親和性，這通常會排除不相關的執行緒，使其無法在該處理器上執行，並有效地為該排程器執行緒保留該執行緒。 請注意，以這種方式設定執行緒親和性，會 starvation 可能在系統上執行的其他進程，進而影響整體系統效能。 如需執行緒親和性的詳細資訊，請參閱 [多個處理器](multiple-processors.md)。

## <a name="ums-worker-threads-thread-contexts-and-completion-lists"></a>UMS 背景工作執行緒、執行緒內容和完成清單

藉由呼叫 [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) \_ 和 PROC 執行緒 \_ 屬性 \_ UMS \_ 執行緒屬性，並指定 ums 執行緒內容和完成清單來建立 ums 背景工作執行緒。

UMS 執行緒內容代表背景工作執行緒的 UMS 執行緒狀態，用來識別 UMS 函式呼叫中的背景工作執行緒。 它是透過呼叫 [**CreateUmsThreadCoNtext**](/windows/desktop/api/WinBase/nf-winbase-createumsthreadcontext)來建立。

完成清單會藉由呼叫 [**CreateUmsCompletionList**](/windows/desktop/api/WinBase/nf-winbase-createumscompletionlist) 函數來建立。 完成清單會接收在核心中已完成執行的 UMS 工作者執行緒，並準備好在使用者模式中執行。 只有系統可以將背景工作執行緒佇列至完成清單。 新的 UMS 背景工作執行緒會自動排入執行緒建立時指定的完成清單。 先前已封鎖的背景工作執行緒在不再被封鎖時，也會在完成清單中排入佇列。

每個 UMS 排程器執行緒都會與單一完成清單相關聯。 不過，相同的完成清單可以與任何數目的 UMS 排程器執行緒相關聯，而排程器執行緒可以從任何具有指標的完成清單中取得 UMS 內容。

每個完成清單都有相關聯的事件，當系統將一或多個背景工作執行緒排入空的清單時，系統就會發出信號。 [**GetUmsCompletionListEvent**](/windows/desktop/api/WinBase/nf-winbase-getumscompletionlistevent)函式會針對指定的完成清單抓取事件的控制碼。 應用程式可以等候一個以上的完成清單事件，以及對應用程式有意義的其他事件。

## <a name="ums-scheduler-entry-point-function"></a>UMS 排程器進入點函數

應用程式的排程器進入點函數會實作為 [*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point) 函數。 系統會在下列時間呼叫應用程式的排程器進入點函數：

-   當非 UMS 執行緒藉由呼叫 [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)轉換成 ums 排程器執行緒時。
-   當 UMS 工作者執行緒呼叫 [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)時。
-   當 UMS 背景工作執行緒在系統服務上封鎖，例如系統呼叫或分頁錯誤時。

[*UmsSchedulerProc*](/windows/desktop/api/WinNT/nc-winnt-rtl_ums_scheduler_entry_point)函式的 *reason* 參數會指定呼叫進入點函數的原因。 如果因為建立了新的 UMS 排程器執行緒而呼叫進入點函式，則 *SchedulerParam* 參數會包含 [**EnterUmsSchedulingMode**](/windows/desktop/api/WinBase/nf-winbase-enterumsschedulingmode)呼叫端所指定的資料。 如果因為產生 UMS 工作者執行緒而呼叫進入點函式，則 *SchedulerParam* 參數會包含 [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield)呼叫端所指定的資料。 如果因為核心中的 UMS 背景工作執行緒遭到封鎖而呼叫進入點函式，則 *SchedulerParam* 參數為 Null。

排程器進入點函數負責判斷指定執行緒的適當下一個動作。 例如，如果背景工作執行緒遭到封鎖，排程器進入點函數可能會執行下一個可用的 UMS 背景工作執行緒。

呼叫排程器進入點函式時，應用程式的排程器應嘗試呼叫 [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) 函數，以取得其相關聯完成清單中的所有專案。 此函式會取得在核心中已完成處理且已準備好在使用者模式下執行的 UMS 執行緒內容清單。 應用程式的排程器不應直接從此清單執行 UMS 執行緒，因為這可能會導致應用程式中發生無法預期的行為。 相反地，排程器應該針對每個內容呼叫 [**GetNextUmsListItem**](/windows/desktop/api/WinBase/nf-winbase-getnextumslistitem) 函數一次，以抓取所有的 ums 執行緒內容，將 ums 執行緒內容插入排程器的就緒執行緒佇列中，然後只從就緒執行緒佇列執行 ums 執行緒。

如果排程器不需要等待多個事件，則應該使用非零的 timeout 參數來呼叫 [**DequeueUmsCompletionListItems**](/windows/desktop/api/WinBase/nf-winbase-dequeueumscompletionlistitems) ，以便函式在傳回之前等候完成清單事件。 如果排程器需要等候多個完成清單事件，它應該呼叫 **DequeueUmsCompletionListItems** ，並將 timeout 參數設為零，讓函數立即傳回，即使完成清單是空的。 在此情況下，排程器可以明確地在完成清單事件上等候，例如，使用 [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects)。

## <a name="ums-thread-execution"></a>UMS 執行緒執行

新建立的 UMS 背景工作執行緒會排入指定的完成清單佇列中，且在應用程式的 UMS 排程器選取執行之前，不會開始執行。 這與非 UMS 執行緒不同，除非呼叫端明確建立擱置的執行緒，否則系統排程器會自動排程執行。

排程器會藉由呼叫 [**ExecuteUmsThread**](/windows/desktop/api/WinBase/nf-winbase-executeumsthread) 與背景工作執行緒的 UMS 內容來執行背景工作執行緒。 UMS 背景工作執行緒會執行，直到它透過呼叫 [**UmsThreadYield**](/windows/desktop/api/WinBase/nf-winbase-umsthreadyield) 函式、區塊或終止來產生為止。

## <a name="ums-best-practices"></a>UMS 最佳作法

執行 UMS 的應用程式應該遵循下列最佳作法：

-   UMS 執行緒內容的基礎結構是由系統管理，不應該直接修改。 相反地，請使用 [**QueryUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-queryumsthreadinformation) 和 [**SetUmsThreadInformation**](/windows/desktop/api/WinBase/nf-winbase-setumsthreadinformation) 來取得和設定 UMS 工作者執行緒的相關資訊。
-   為了協助防止鎖死，UMS 排程器執行緒不應與 UMS 工作者執行緒共用鎖定。 這包括應用程式建立的鎖定和系統鎖定，這些都是由作業間接取得，例如從堆積配置或載入 Dll。 例如，假設排程器執行會載入 DLL 的 UMS 工作者執行緒。 背景工作執行緒會取得載入器鎖定和區塊。 系統會呼叫排程器進入點函數，然後載入 DLL。 這會造成鎖死，因為已持有載入器鎖定，而且在第一個執行緒解除封鎖之前無法釋出。 若要避免這個問題，請將可能與 UMS 工作者執行緒共用鎖定的工作委派給專用的 UMS 背景工作執行緒或非 UMS 執行緒。
-   當大部分處理都是在使用者模式下完成時，UMS 是最有效率的。 請盡可能避免在 UMS 工作者執行緒中進行系統呼叫。
-   UMS 工作者執行緒不應假設系統排程器正在使用中。 這種假設有很微妙的效果;例如，如果未知程式碼中的執行緒設定執行緒優先順序或親和性，則 UMS 排程器可能仍會覆寫它。 假設使用系統排程器的程式碼可能不會如預期般運作，而且在 UMS 執行緒呼叫時可能會中斷。
-   系統可能需要鎖定 UMS 工作者執行緒的執行緒內容。 例如， (APC) 的核心模式非同步程序呼叫可能會變更 UMS 執行緒的內容，因此必須鎖定執行緒內容。 如果排程器在鎖定時嘗試執行 UMS 執行緒內容，則呼叫會失敗。 這是設計的行為，而且排程器的設計目的是要重試 UMS 執行緒內容的存取。

 

 
