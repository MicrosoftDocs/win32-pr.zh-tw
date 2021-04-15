---
description: 檔案對應是檔案內容與進程虛擬位址空間之一部分的關聯。
ms.assetid: 86a8bc81-914d-46a2-99fd-65dfd03bbcdd
title: 檔案對應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f49162a4545d0e087e6b291e429d89049dbf57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511573"
---
# <a name="file-mapping"></a><span data-ttu-id="28f03-103">檔案對應</span><span class="sxs-lookup"><span data-stu-id="28f03-103">File Mapping</span></span>

<span data-ttu-id="28f03-104">檔案 *對應* 是檔案內容與進程虛擬位址空間之一部分的關聯。</span><span class="sxs-lookup"><span data-stu-id="28f03-104">*File mapping* is the association of a file's contents with a portion of the virtual address space of a process.</span></span> <span data-ttu-id="28f03-105">系統會建立檔案 *對應物件* (也稱為 *區段物件*) 來維護此關聯。</span><span class="sxs-lookup"><span data-stu-id="28f03-105">The system creates a *file mapping object* (also known as a *section object*) to maintain this association.</span></span> <span data-ttu-id="28f03-106">檔案 *視圖* 是進程用來存取檔案內容的虛擬位址空間部分。</span><span class="sxs-lookup"><span data-stu-id="28f03-106">A *file view* is the portion of virtual address space that a process uses to access the file's contents.</span></span> <span data-ttu-id="28f03-107">檔案對應可讓進程同時使用隨機輸入和輸出 (i/o) 和連續 i/o。</span><span class="sxs-lookup"><span data-stu-id="28f03-107">File mapping allows the process to use both random input and output (I/O) and sequential I/O.</span></span> <span data-ttu-id="28f03-108">它也可讓程式有效率地處理大型資料檔案（例如資料庫），而不需要將整個檔案對應到記憶體。</span><span class="sxs-lookup"><span data-stu-id="28f03-108">It also allows the process to work efficiently with a large data file, such as a database, without having to map the whole file into memory.</span></span> <span data-ttu-id="28f03-109">多個進程也可以使用記憶體對應檔案來共用資料。</span><span class="sxs-lookup"><span data-stu-id="28f03-109">Multiple processes can also use memory-mapped files to share data.</span></span>

<span data-ttu-id="28f03-110">進程會使用指標來讀取和寫入檔案視圖，就像使用動態配置的記憶體一樣。</span><span class="sxs-lookup"><span data-stu-id="28f03-110">Processes read from and write to the file view using pointers, just as they would with dynamically allocated memory.</span></span> <span data-ttu-id="28f03-111">使用檔案對應可提升效率，因為檔案位於磁片上，但是檔案視圖位於記憶體中。</span><span class="sxs-lookup"><span data-stu-id="28f03-111">The use of file mapping improves efficiency because the file resides on disk, but the file view resides in memory.</span></span> <span data-ttu-id="28f03-112">處理常式也可以使用 [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) 函式來操作檔案視圖。</span><span class="sxs-lookup"><span data-stu-id="28f03-112">Processes can also manipulate the file view with the [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) function.</span></span>

<span data-ttu-id="28f03-113">下圖顯示磁片上的檔案、檔案對應物件和檔案視圖之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="28f03-113">The following illustration shows the relationship between the file on disk, a file mapping object, and a file view.</span></span>

![磁片上的檔案、檔案對應物件和檔案視圖之間的關聯性。](images/fmap.png)

<span data-ttu-id="28f03-115">磁片上的檔案可以是您想要對應到記憶體中的任何檔案，也可以是系統分頁檔案。</span><span class="sxs-lookup"><span data-stu-id="28f03-115">The file on disk can be any file that you want to map into memory, or it can be the system page file.</span></span> <span data-ttu-id="28f03-116">檔案對應物件可以包含全部或只包含部分檔案。</span><span class="sxs-lookup"><span data-stu-id="28f03-116">The file mapping object can consist of all or only part of the file.</span></span> <span data-ttu-id="28f03-117">它是由磁片上的檔案所支援。</span><span class="sxs-lookup"><span data-stu-id="28f03-117">It is backed by the file on disk.</span></span> <span data-ttu-id="28f03-118">這表示當系統交換檔案對應物件的頁面時，對檔案對應物件所做的任何變更都會寫入至檔案。</span><span class="sxs-lookup"><span data-stu-id="28f03-118">This means that when the system swaps out pages of the file mapping object, any changes made to the file mapping object are written to the file.</span></span> <span data-ttu-id="28f03-119">當檔案對應物件的頁面換回時，會從檔案還原它們。</span><span class="sxs-lookup"><span data-stu-id="28f03-119">When the pages of the file mapping object are swapped back in, they are restored from the file.</span></span>

<span data-ttu-id="28f03-120">檔案視圖可以包含全部或只包含檔案對應物件的一部分。</span><span class="sxs-lookup"><span data-stu-id="28f03-120">A file view can consist of all or only part of the file mapping object.</span></span> <span data-ttu-id="28f03-121">程式會透過檔案視圖來操作檔案。</span><span class="sxs-lookup"><span data-stu-id="28f03-121">A process manipulates the file through the file views.</span></span> <span data-ttu-id="28f03-122">進程可以建立檔案對應物件的多個視圖。</span><span class="sxs-lookup"><span data-stu-id="28f03-122">A process can create multiple views for a file mapping object.</span></span> <span data-ttu-id="28f03-123">每個處理常式所建立的檔案視圖都位於該進程的虛擬位址空間中。</span><span class="sxs-lookup"><span data-stu-id="28f03-123">The file views created by each process reside in the virtual address space of that process.</span></span> <span data-ttu-id="28f03-124">當進程需要來自檔案一部分以外的資料，而不是目前檔案視圖中的資料時，它可以取消目前的檔案視圖的對應，然後建立新的檔案視圖。</span><span class="sxs-lookup"><span data-stu-id="28f03-124">When the process needs data from a portion of the file other than what is in the current file view, it can unmap the current file view, then create a new file view.</span></span>

<span data-ttu-id="28f03-125">當多個進程使用相同的檔案對應物件來建立本機檔案的視圖時，資料是一致的。</span><span class="sxs-lookup"><span data-stu-id="28f03-125">When multiple processes use the same file mapping object to create views for a local file, the data is coherent.</span></span> <span data-ttu-id="28f03-126">也就是，這些視圖包含磁片上相同的檔案複本。</span><span class="sxs-lookup"><span data-stu-id="28f03-126">That is, the views contain identical copies of the file on disk.</span></span> <span data-ttu-id="28f03-127">如果您想要在多個進程之間共用記憶體，檔案不能位於遠端電腦上。</span><span class="sxs-lookup"><span data-stu-id="28f03-127">The file cannot reside on a remote computer if you want to share memory between multiple processes.</span></span>

<span data-ttu-id="28f03-128">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="28f03-128">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="28f03-129">建立檔案對應物件</span><span class="sxs-lookup"><span data-stu-id="28f03-129">Creating a File Mapping Object</span></span>](creating-a-file-mapping-object.md)
-   [<span data-ttu-id="28f03-130">建立檔案視圖</span><span class="sxs-lookup"><span data-stu-id="28f03-130">Creating a File View</span></span>](creating-a-file-view.md)
-   [<span data-ttu-id="28f03-131">共用檔案和記憶體</span><span class="sxs-lookup"><span data-stu-id="28f03-131">Sharing Files and Memory</span></span>](sharing-files-and-memory.md)
-   [<span data-ttu-id="28f03-132">從檔案視圖讀取和寫入</span><span class="sxs-lookup"><span data-stu-id="28f03-132">Reading and Writing From a File View</span></span>](reading-and-writing-from-a-file-view.md)
-   [<span data-ttu-id="28f03-133">關閉檔案對應物件</span><span class="sxs-lookup"><span data-stu-id="28f03-133">Closing a File Mapping Object</span></span>](closing-a-file-mapping-object.md)
-   [<span data-ttu-id="28f03-134">檔案對應安全性和存取權限</span><span class="sxs-lookup"><span data-stu-id="28f03-134">File Mapping Security and Access Rights</span></span>](file-mapping-security-and-access-rights.md)
-   [<span data-ttu-id="28f03-135">使用檔案對應</span><span class="sxs-lookup"><span data-stu-id="28f03-135">Using File Mapping</span></span>](using-file-mapping.md)

 

 
