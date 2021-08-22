---
description: 若要判斷目前電腦上的頁面大小，請使用 GetSystemInfo 函數。
ms.assetid: 953ddfc4-6126-41fb-81a3-0ce1f0fb223f
title: 使用頁面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e47e8a352b13c12b38acca1a93f12886d83d24c4d43faa213a88cf5855b18c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067658"
---
# <a name="working-with-pages"></a>使用頁面

若要判斷目前電腦上的頁面大小，請使用 [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) 函數。

[**VirtualQuery**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery)和 [**VirtualQueryEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex)函式會從進程位址空間中的指定位址開始，傳回連續頁面區域的相關資訊。 **VirtualQuery** 會傳回呼叫進程中記憶體的相關資訊。 **VirtualQueryEx** 會傳回指定進程中的記憶體相關資訊，並且用來支援需要所進行之進程相關資訊的偵錯工具。 頁面區域會依指定的位址（四捨五入至最接近的頁面界限）來限定。 它會透過下列常見的屬性，延伸至所有後續頁面：

-   所有頁面的狀態都相同：「已認可」、「保留」或「免費」。
-   如果初始頁面不是可用的，則該區域中的所有頁面都屬於相同初始配置頁面的一部分，這些頁面是由呼叫 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)所保留的頁面。
-   所有頁面的存取保護都相同 (也就是， **page \_ READONLY**、 **page \_ READWRITE** 或 **page \_ NOACCESS**) 。

[**VirtualLock**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock)函式可讓進程將一或多個已認可記憶體頁面鎖定 (RAM) 的實體記憶體中，以防止系統將頁面交換到分頁檔案。 可以用來確保在沒有磁片存取的情況下可存取重要資料。 將分頁鎖在記憶體中是危險的，因為它會限制系統管理記憶體的能力。 過度使用 **VirtualLock** 可能會導致可執行程式碼交換到分頁檔案，進而降低系統效能。 [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock)函數會解除鎖定由 **VirtualLock** 鎖定的記憶體。

[**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)函式可讓進程修改進程位址空間中任何已認可頁面的存取保護。 例如，處理常式可以配置讀取/寫入頁面來儲存敏感性資料，然後將存取權變更為唯讀或無存取，以防止意外覆寫。 **VirtualProtect** 通常用於 [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)所配置的頁面，但也適用于任何其他配置函數所認可的頁面。 不過， **VirtualProtect** 會變更整個頁面的保護，而且其他函式所傳回的指標不一定會在頁面界限上對齊。 [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex)函式類似于 **VirtualProtect**，但它會變更指定進程中的記憶體保護。 變更保護對於存取正在進行的進程之記憶體中的偵錯工具很有用。

 

 
