---
description: 屬於進程的記憶體是由其私用虛擬位址空間隱含保護。
ms.assetid: 70ded07a-7be6-4189-a1ae-281917f42a1e
title: 記憶體保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd30df8084c91a62c28414f4a8142397ee777e52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115920"
---
# <a name="memory-protection"></a><span data-ttu-id="58883-103">記憶體保護</span><span class="sxs-lookup"><span data-stu-id="58883-103">Memory Protection</span></span>

<span data-ttu-id="58883-104">屬於進程的記憶體是由其私用虛擬位址空間隱含保護。</span><span class="sxs-lookup"><span data-stu-id="58883-104">Memory that belongs to a process is implicitly protected by its private virtual address space.</span></span> <span data-ttu-id="58883-105">此外，Windows 還使用虛擬記憶體硬體來提供記憶體保護。</span><span class="sxs-lookup"><span data-stu-id="58883-105">In addition, Windows provides memory protection by using the virtual memory hardware.</span></span> <span data-ttu-id="58883-106">這項保護的執行會因處理器而異，例如，進程位址空間中的字碼頁可以標示為唯讀，而不受使用者模式執行緒修改。</span><span class="sxs-lookup"><span data-stu-id="58883-106">The implementation of this protection varies with the processor, for example, code pages in the address space of a process can be marked read-only and protected from modification by user-mode threads.</span></span>

<span data-ttu-id="58883-107">如需屬性的完整清單，請參閱 [記憶體保護常數](memory-protection-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="58883-107">For the complete list of attributes, see [Memory Protection Constants](memory-protection-constants.md).</span></span>

## <a name="copy-on-write-protection"></a><span data-ttu-id="58883-108">複製時寫入保護</span><span class="sxs-lookup"><span data-stu-id="58883-108">Copy-on-Write Protection</span></span>

<span data-ttu-id="58883-109">「複製時禁止複製」是一項優化功能，可讓多個進程對應其虛擬位址空間，使其共用實體頁面，直到其中一個進程修改頁面為止。</span><span class="sxs-lookup"><span data-stu-id="58883-109">Copy-on-write protection is an optimization that allows multiple processes to map their virtual address spaces such that they share a physical page until one of the processes modifies the page.</span></span> <span data-ttu-id="58883-110">這是稱為「 *延遲評估*」之技術的一部分，可讓系統在絕對必要的情況下，不執行作業來節省實體記憶體和時間。</span><span class="sxs-lookup"><span data-stu-id="58883-110">This is part of a technique called *lazy evaluation*, which allows the system to conserve physical memory and time by not performing an operation until absolutely necessary.</span></span>

<span data-ttu-id="58883-111">例如，假設有兩個處理常式會將來自相同 DLL 的頁面載入至它們的虛擬記憶體空間。</span><span class="sxs-lookup"><span data-stu-id="58883-111">For example, suppose two processes load pages from the same DLL into their virtual memory spaces.</span></span> <span data-ttu-id="58883-112">這些虛擬記憶體頁面會對應到相同的實體記憶體頁面，以用於這兩個處理常式。</span><span class="sxs-lookup"><span data-stu-id="58883-112">These virtual memory pages are mapped to the same physical memory pages for both processes.</span></span> <span data-ttu-id="58883-113">只要兩個程式都不會寫入這些頁面，它們就可以對應到和共用相同的實體頁面，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="58883-113">As long as neither process writes to these pages, they can map to and share, the same physical pages, as shown in the following diagram.</span></span>

![進程1和2頁的方塊和箭號對應到相同的實體記憶體](images/mem1.png)

<span data-ttu-id="58883-115">如果處理常式1寫入這些頁面的其中一個，實體頁面的內容會複製到另一個實體頁面，而且會針對進程1更新虛擬記憶體對應。</span><span class="sxs-lookup"><span data-stu-id="58883-115">If Process 1 writes to one of these pages, the contents of the physical page are copied to another physical page and the virtual memory map is updated for Process 1.</span></span> <span data-ttu-id="58883-116">這兩個處理常式現在會在實體記憶體中有自己的頁面實例。</span><span class="sxs-lookup"><span data-stu-id="58883-116">Both processes now have their own instance of the page in physical memory.</span></span> <span data-ttu-id="58883-117">因此，一個進程不可能寫入共用實體頁面，而另一個進程也無法看到變更。</span><span class="sxs-lookup"><span data-stu-id="58883-117">Therefore, it is not possible for one process to write to a shared physical page and for the other process to see the changes.</span></span>

![進程和實體記憶體重新對應的方塊和箭號](images/mem2.png)

## <a name="loading-applications-and-dlls"></a><span data-ttu-id="58883-119">載入應用程式和 Dll</span><span class="sxs-lookup"><span data-stu-id="58883-119">Loading Applications and DLLs</span></span>

<span data-ttu-id="58883-120">載入相同 Windows 架構應用程式的多個實例時，每個實例都會在它自己的受保護虛擬位址空間中執行。</span><span class="sxs-lookup"><span data-stu-id="58883-120">When multiple instances of the same Windows-based application are loaded, each instance is run in its own protected virtual address space.</span></span> <span data-ttu-id="58883-121">不過，其實例會處理 (*hInstance*) 通常具有相同的值。</span><span class="sxs-lookup"><span data-stu-id="58883-121">However, their instance handles (*hInstance*) typically have the same value.</span></span> <span data-ttu-id="58883-122">此值代表應用程式在其虛擬位址空間中的基底位址。</span><span class="sxs-lookup"><span data-stu-id="58883-122">This value represents the base address of the application in its virtual address space.</span></span> <span data-ttu-id="58883-123">如果每個實例都可以載入至其預設基底位址，則可以使用「寫入時複製」保護，將相同的實體頁面對應至其他實例，並與其他實例共用。</span><span class="sxs-lookup"><span data-stu-id="58883-123">If each instance can be loaded into its default base address, it can map to and share the same physical pages with the other instances, using copy-on-write protection.</span></span> <span data-ttu-id="58883-124">系統可讓這些實例共用相同的實體頁面，直到其中一個修改頁面為止。</span><span class="sxs-lookup"><span data-stu-id="58883-124">The system allows these instances to share the same physical pages until one of them modifies a page.</span></span> <span data-ttu-id="58883-125">如果基於某些原因而無法在所需的基底位址中載入其中一個實例，它會收到自己的實體頁面。</span><span class="sxs-lookup"><span data-stu-id="58883-125">If for some reason one of these instances cannot be loaded in the desired base address, it receives its own physical pages.</span></span>

<span data-ttu-id="58883-126">Dll 是以預設基底位址建立。</span><span class="sxs-lookup"><span data-stu-id="58883-126">DLLs are created with a default base address.</span></span> <span data-ttu-id="58883-127">每個使用 DLL 的進程會嘗試在其本身的位址空間內（DLL 的預設虛擬位址）載入 DLL。</span><span class="sxs-lookup"><span data-stu-id="58883-127">Every process that uses a DLL will try to load the DLL within its own address space at the default virtual address for the DLL.</span></span> <span data-ttu-id="58883-128">如果多個應用程式可以在其預設虛擬位址上載入 DLL，它們可以與 DLL 共用相同的實體頁面。</span><span class="sxs-lookup"><span data-stu-id="58883-128">If multiple applications can load a DLL at its default virtual address, they can share the same physical pages for the DLL.</span></span> <span data-ttu-id="58883-129">如果基於某些原因，進程無法在預設位址載入 DLL，它就會在其他位置載入 DLL。</span><span class="sxs-lookup"><span data-stu-id="58883-129">If for some reason a process cannot load the DLL at the default address, it loads the DLL elsewhere.</span></span> <span data-ttu-id="58883-130">複製時禁止複製會強制將部分 DLL 的頁面複製到不同的實體頁面以進行此程式，因為跳躍指示的修正程式是在 DLL 的頁面中撰寫，而這項處理常式將會不同。</span><span class="sxs-lookup"><span data-stu-id="58883-130">Copy-on-write protection forces some of the DLL's pages to be copied into different physical pages for this process, because the fixes for jump instructions are written within the DLL's pages, and they will be different for this process.</span></span> <span data-ttu-id="58883-131">如果程式碼區段包含許多對 data 區段的參考，這可能會導致整個程式碼區段複製到新的實體頁面。</span><span class="sxs-lookup"><span data-stu-id="58883-131">If the code section contains many references to the data section, this can cause the entire code section to be copied to new physical pages.</span></span>

 

 



