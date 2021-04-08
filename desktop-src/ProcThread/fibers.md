---
description: 光纖是必須由應用程式手動排程的執行單位。
ms.assetid: 6283f56b-23ae-4840-abd0-2478a50c670c
title: 纖維
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0383e6d207a77c621f00f358c72bb8873ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103693015"
---
# <a name="fibers"></a>纖維

*光纖* 是必須由應用程式手動排程的執行單位。 在排程執行緒的執行緒內容中執行纖程。 每個執行緒都可以排程多個纖維。 一般而言，在設計完善的多執行緒應用程式上，纖維並不提供任何優點。 不過，使用纖維可讓您更輕鬆地移植設計來排程其自有線程的應用程式。

從系統的觀點來看，光纖會假設執行它的執行緒的身分識別。 例如，如果光纖 (TLS) 存取 [執行緒區域儲存區](thread-local-storage.md) ，它就會存取執行它之執行緒的執行緒區域儲存區。 此外，如果光纖呼叫 [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) 函式，則會結束執行它的執行緒。 不過，光纖並沒有與執行緒相關聯的所有相同狀態資訊。 針對光纖維護的唯一狀態資訊是它的堆疊、其暫存器的子集，以及光纖建立期間提供的光纖資料。 儲存的暫存器是一組通常會在函式呼叫中保留的暫存器。

未事先排程的纖維。 您可以從另一個光纖切換至光纖，以排程光纖。 系統仍會排定要執行的執行緒。 當執行纖程的執行緒被優先佔用時，其目前正在執行的光纖會被佔用，但仍保持選取狀態。 選取的光纖會在其執行緒執行時執行。

在排程第一個光纖之前，請先呼叫 [**ConvertThreadToFiber**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber) 函式來建立儲存光纖狀態資訊的區域。 呼叫執行緒現在是目前正在執行的光纖。 這個光纖的儲存狀態資訊包括以引數形式傳遞至 **ConvertThreadToFiber** 的光纖資料。

[**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber)函式是用來從現有的光纖建立新的光纖。呼叫需要堆疊大小、起始位址和光纖資料。 起始位址通常是使用者提供的函式，稱為「光纖函數」（ (光纖資料) 使用一個參數，且不會傳回值。 如果您的光纖函式傳回，則會結束執行光纖的執行緒。 若要執行以 **CreateFiber** 建立的任何光纖，請呼叫 [**SwitchToFiber**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber) 函數。 您可以使用不同執行緒所建立的光纖位址來呼叫 **SwitchToFiber** 。 若要這樣做，您必須在呼叫 **CreateFiber** 時，將位址傳回至另一個執行緒，而且您必須使用適當的同步處理。

光纖可以藉由呼叫 [**GetFiberData**](/windows/win32/api/winnt/nf-winnt-getfiberdata) 宏來取出光纖資料。 光纖可以在任何時間呼叫 [**GetCurrentFiber**](/windows/win32/api/winnt/nf-winnt-getcurrentfiber) 宏來取出光纖位址。

## <a name="fiber-local-storage"></a>光纖本機儲存體

光纖可以使用 *光纖本機儲存體* (FLS) 為每個光纖建立唯一的變數複本。 如果未發生任何光纖切換，FLS 與 [執行緒區域儲存區](thread-local-storage.md)的行為完全相同。 FLS 函式 ([**FlsAlloc**](/windows/win32/api/fibersapi/nf-fibersapi-flsalloc)、 [**FlsFree**](/windows/win32/api/fibersapi/nf-fibersapi-flsfree)、 [**FlsGetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flsgetvalue)和 [**FlsSetValue**](/windows/win32/api/fibersapi/nf-fibersapi-flssetvalue)) 操作與目前線程相關聯的 FLS。 如果執行緒正在執行光纖並切換光纖，FLS 也會一併切換。

若要清除與光纖相關聯的資料，請呼叫 [**DeleteFiber**](/windows/desktop/api/WinBase/nf-winbase-deletefiber) 函數。 這項資料包括堆疊、暫存器的子集，以及光纖資料。 如果目前執行的光纖呼叫 **DeleteFiber**，它的執行緒會呼叫 [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) 並終止。 但是，如果選取的執行緒光纖是由另一個執行緒中執行的光纖所刪除，則具有已刪除之光纖的執行緒可能會異常終止，因為已釋放光纖堆疊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用纖維](using-fibers.md)
</dt> </dl>

 

 
