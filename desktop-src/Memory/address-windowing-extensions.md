---
description: 位址視窗擴充 (AWE) 是一組延伸模組，可讓應用程式快速操作大於4GB 的實體記憶體。
ms.assetid: 48a29922-8130-4540-86b0-0faa120566a6
title: 位址視窗擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5f0c68e9609834a9065a919d12c23c40521e99ede94feb96889050b6873654
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764408"
---
# <a name="address-windowing-extensions"></a>位址視窗擴充功能

位址視窗擴充 (AWE) 是一組延伸模組，可讓應用程式快速操作大於4GB 的實體記憶體。 某些需要大量資料的應用程式（例如資料庫管理系統、科學和工程軟體）需要存取非常大量的資料快取。 在非常大型的資料集的情況下，限制快取以容納在應用程式的使用者位址空間的2GB 內，是一項嚴重的限制。 在這些情況下，快取太小，無法正確支援應用程式。

AWE 可讓應用程式直接處理海量儲存體，同時繼續使用32位指標，藉此解決這個問題。 AWE 可讓應用程式在有足夠實體記憶體的情況下，將資料快取到大於4GB 的 () 。 AWE 會在32位虛擬位址空間內，針對此實體記憶體的各個部分，使用物理非分頁式記憶體和視窗視圖。

AWE 對此記憶體的使用方式有一些限制，主要是因為這些限制可讓您以極快速的方式對應、重新對應和釋放。 快速記憶體管理對於這些可能的大量位址空間而言很重要。

-   配置給 AWE 的虛擬位址範圍不能與其他進程共用 (因此無法繼承) 。 事實上，相同進程內的兩個不同 AWE 虛擬位址不允許對應相同的實體頁面。 這些限制可在釋放記憶體時，提供快速重新對應和清除。
-   可以針對 AWE 區域配置的實體頁面會受限於機器中的實體頁面數目，因為此記憶體從未分頁過，所以會被鎖定，直到應用程式明確釋出或結束為止。 針對給定進程配置的實體頁面可以對應到相同進程內的任何 AWE 虛擬區域。 使用 AWE 的應用程式必須小心，不要佔用太多實體記憶體，讓其他應用程式過度分頁，或防止建立新的進程或執行緒，因為資源不足。 使用 [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) 函式來監視實體記憶體的使用方式。
-   AWE 虛擬位址一律是讀取/寫入，而且無法透過呼叫 ([**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) 進行保護，也就是沒有唯讀的記憶體、noaccess 記憶體、防護頁面，而且可以指定) 的 like。
-   AWE 位址範圍不能用來緩衝處理圖形或影片呼叫的資料。
-   無法分割 AWE 記憶體範圍，也無法刪除它的片段。 相反地，必須刪除整個虛擬位址範圍，以作為需要刪除的單位。 這表示在呼叫 [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree)時，您必須指定 **MEM \_ 釋放**。
-   應用程式可以同時對應多個區域，但前提是它們不會重迭。
-   模擬模式不支援使用 AWE 的應用程式。 也就是說，使用 AWE 函式的 x86 應用程式必須重新編譯，才能在另一個處理器上執行，而大部分的應用程式都可以在不需要重新編譯的情況下，于其他平臺的模擬器下執行。

此解決方案以非常普遍、普遍適用的方式解決實體記憶體問題。 AWE 的一些優點如下：

-   定義一小部分的新函數，以操作 AWE 記憶體。
-   AWE 提供非常快速的重新對應功能。 重新對應是藉由操作虛擬記憶體資料表來完成，而不是在實體記憶體中移動資料。
-   AWE 提供適用于處理器 (的頁面大小細微性，例如在 x86) 上為 4 KB，這對應用程式比大型頁面更有用 (例如，x86) 上的2MB 或4MB。

應用程式必須具有 [鎖定記憶體中的分頁] 許可權，才能使用 AWE。 若要取得此許可權，系統管理員必須 **在記憶體中將鎖定頁面** 新增至使用者的 **使用者權限指派**。 如需如何進行這項操作的詳細資訊，請參閱作業系統說明中的「使用者權限」。

下列函式會組成 (AWE) API 的位址視窗擴充功能。



| 函式                                                                          | 描述                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)和 [ **VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | 使用 **記憶體 \_ 實體**，保留要用於 AWE 的部分虛擬位址空間。                                                                                                                                                                       |
| [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)                    | 配置要搭配 AWE 使用的實體記憶體。                                                                                                                                                                                                                |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages)                              | 將) AWE 虛擬位址對應 (或使其失效，並放到以 [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)取得的任何實體頁面上。                                                                                                    |
| [**MapUserPhysicalPagesScatter**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter)                | 將) AWE 虛擬位址對應 (或使其在以 [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)取得的任何實體頁面上失效，但使用 [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages)所提供的更細微控制。 |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages)                            | 用於 AWE 的可用實體記憶體。                                                                                                                                                                                                               |



 

 

 
