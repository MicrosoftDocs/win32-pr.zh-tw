---
description: 當處理常式完成檔案對應物件時，應該使用每個檔案視圖的 UnmapViewOfFile 函式，以終結其位址空間中的所有檔案視圖。
ms.assetid: d62d068c-9b1d-4dbf-8b21-31a636a41456
title: 關閉檔案對應物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ab35152bd90d401ca7f30a7497d1f0b06263539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849164"
---
# <a name="closing-a-file-mapping-object"></a><span data-ttu-id="397ad-103">關閉檔案對應物件</span><span class="sxs-lookup"><span data-stu-id="397ad-103">Closing a File Mapping Object</span></span>

<span data-ttu-id="397ad-104">當處理常式完成檔案對應物件時，應該使用每個檔案視圖的 [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) 函式，以終結其位址空間中的所有檔案視圖。</span><span class="sxs-lookup"><span data-stu-id="397ad-104">When a process has finished with the file mapping object, it should destroy all file views in its address space by using the [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) function for each file view.</span></span>

<span data-ttu-id="397ad-105">取消對應檔案的對應視圖會使此進程的位址空間中的視圖所佔用的範圍失效，並讓範圍可供其他配置使用。</span><span class="sxs-lookup"><span data-stu-id="397ad-105">Unmapping a mapped view of a file invalidates the range occupied by the view in the address space of the process and makes the range available for other allocations.</span></span> <span data-ttu-id="397ad-106">它會移除每個未對應的虛擬頁面的工作集專案，這是處理常式的工作集一部分，並減少進程的工作集大小。</span><span class="sxs-lookup"><span data-stu-id="397ad-106">It removes the working set entry for each unmapped virtual page that was part of the working set of the process and reduces the working set size of the process.</span></span> <span data-ttu-id="397ad-107">它也會減少對應實體頁面的共用計數。</span><span class="sxs-lookup"><span data-stu-id="397ad-107">It also decrements the share count of the corresponding physical page.</span></span>

<span data-ttu-id="397ad-108">未對應的視圖中修改過的頁面不會寫入至磁片，直到其共用計數到達零為止，或者也就是從共用頁面的所有進程的工作集取消對應或修剪為止。</span><span class="sxs-lookup"><span data-stu-id="397ad-108">Modified pages in the unmapped view are not written to disk until their share count reaches zero, or in other words, until they are unmapped or trimmed from the working sets of all processes that share the pages.</span></span> <span data-ttu-id="397ad-109">就算如此，修改過的頁面也會「延遲」寫入磁片;也就是說，修改可能會快取在記憶體中，並于稍後寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="397ad-109">Even then, the modified pages are written "lazily" to disk; that is, modifications may be cached in memory and written to disk at a later time.</span></span> <span data-ttu-id="397ad-110">為了將發生電源中斷或系統損毀時資料遺失的風險降至最低，應用程式應該使用 [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) 函式明確地排清修改過的頁面。</span><span class="sxs-lookup"><span data-stu-id="397ad-110">To minimize the risk of data loss in the event of a power failure or a system crash, applications should explicitly flush modified pages using the [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) function.</span></span>

<span data-ttu-id="397ad-111">當每個程式使用檔案對應物件完成，而且已將所有視圖都未對應時，它必須藉由呼叫 [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle)來關閉檔案對應物件的控制碼和磁片上的檔案。</span><span class="sxs-lookup"><span data-stu-id="397ad-111">When each process finishes using the file mapping object and has unmapped all views, it must close the file mapping object's handle and the file on disk by calling [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle).</span></span> <span data-ttu-id="397ad-112">即使有檔案視圖仍處於開啟狀態，這些 **CloseHandle** 的呼叫還是會成功。</span><span class="sxs-lookup"><span data-stu-id="397ad-112">These calls to **CloseHandle** succeed even when there are file views that are still open.</span></span> <span data-ttu-id="397ad-113">不過，保留檔案視圖會導致記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="397ad-113">However, leaving file views mapped causes memory leaks.</span></span>

 

 
