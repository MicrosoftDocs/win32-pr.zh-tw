---
title: 系統的快照集
description: 快照集是工具說明功能的核心。 快照集是一或多個位於系統記憶體進程、執行緒、模組和堆積中的下列一或多個清單之目前狀態的唯讀複本。
ms.assetid: a8122960-f078-4efb-8e01-bf6fb69ee0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30dde3a4383bf56bdef46c59c55611ffe9b22a7a201abb4f0f11af85594c4f0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137411"
---
# <a name="snapshots-of-the-system"></a>系統的快照集

快照集是工具說明功能的核心。 快照集是一或多個位於系統記憶體：進程、執行緒、模組和堆積之下列清單的目前狀態的唯讀複本。

使用工具說明函式的進程會從快照集（而不是直接從作業系統）存取這些清單。 當處理常式啟動和結束時，系統記憶體中的清單會變更、建立和終結執行緒、從系統記憶體載入和卸載可執行模組，以及建立和終結堆積。 從快照集使用資訊可防止不一致的情況。 否則，對清單所做的變更可能會導致執行緒不正確地進行清單或造成 (GP 錯誤) 的存取違規。 例如，如果應用程式在建立或終止其他執行緒時，會線上程清單中進行，則應用程式用來跨越執行緒清單的資訊可能會變成過時，而且可能會導致應用程式發生錯誤。

若要取得系統記憶體的快照，請使用 [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) 函數。 您可以在呼叫此函式時指定下列一或多個值，以控制快照集的內容：

-   **TH32CS \_ SNAPHEAPLIST**
-   **TH32CS \_ SNAPMODULE**
-   **TH32CS \_ SNAPPROCESS**
-   **TH32CS \_ SNAPTHREAD**

**TH32CS \_ SNAPHEAPLIST** 和 **TH32CS \_ SNAPMODULE** 值是進程特定的。 當指定這些值時，快照集會包含指定進程的堆積和模組清單。 如果您指定零做為處理常式識別碼，則會使用目前的進程。 即使將進程識別碼傳遞給 [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)， **TH32CS \_ SNAPTHREAD** 值一律會建立全系統的快照集。

若要列舉所有進程的堆積或模組狀態，請指定 **TH32CS \_ SNAPALL** 值和目前進程的處理序識別碼。 然後，針對快照中的每個額外進程，再次呼叫 [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) ，指定其處理序識別碼和 **TH32CS \_ SNAPHEAPLIST** 或 **TH32CS \_ SNAPMODULE** 值。

您可以使用 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)函式來取得 [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)的擴充錯誤狀態碼。

當您的進程使用快照集完成時，請使用 [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) 函式將它終結。 如果您沒有終結快照集，進程將會流失記憶體，直到它結束為止，此時系統會回收記憶體。

> [!Note]  
> 快照集控制碼的運作方式就像是檔案控制代碼，並且受限於可使用它之進程和執行緒的相同規則。 若要指定控制碼是可繼承的，請使用 **TH32CS \_ INHERIT** 值來建立快照集。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[拍攝快照集和觀看進程](taking-a-snapshot-and-viewing-processes.md)
</dt> </dl>

 

 