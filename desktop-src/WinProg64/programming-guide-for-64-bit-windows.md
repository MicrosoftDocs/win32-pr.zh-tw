---
title: 64 位元 Windows 程式設計手冊
description: Microsoft 已發行64位版本的 Windows 作業系統。
ms.assetid: eb31408a-549d-427e-9f8e-9ae96bf6f854
keywords:
- 64位 Windows 程式設計指南64位 Windows 程式設計
- 64位 Windows 程式設計指南64位 Windows 程式設計，首頁
- 64位 Windows 64 位 Windows 程式設計的程式設計指南，請參閱64位 Windows 程式設計指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb1fa906510d3d9909c5cf888b562deaccb3496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372287"
---
# <a name="programming-guide-for-64-bit-windows"></a><span data-ttu-id="22c1a-106">64 位元 Windows 程式設計手冊</span><span class="sxs-lookup"><span data-stu-id="22c1a-106">Programming Guide for 64-bit Windows</span></span>

<span data-ttu-id="22c1a-107">Microsoft 已發行64位版本的 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="22c1a-107">Microsoft has released 64-bit versions of the Windows operating system.</span></span> <span data-ttu-id="22c1a-108">64位 Windows 的設計是以相容性為考慮。</span><span class="sxs-lookup"><span data-stu-id="22c1a-108">64-bit Windows was designed with compatibility in mind.</span></span> <span data-ttu-id="22c1a-109">開發人員可以藉由遷移應用程式，確保其現有的32位應用程式在64位 Windows 下正常執行，或利用64位 Windows 的優點。</span><span class="sxs-lookup"><span data-stu-id="22c1a-109">Developers can ensure that their existing 32-bit applications run well under 64-bit Windows or take advantage of the benefits of 64-bit Windows by migrating their applications.</span></span>

## <a name="benefits-of-64-bit-windows"></a><span data-ttu-id="22c1a-110">64位 Windows 的優點</span><span class="sxs-lookup"><span data-stu-id="22c1a-110">Benefits of 64-bit Windows</span></span>

<span data-ttu-id="22c1a-111">64位作業系統支援的實體記憶體遠高於32位作業系統。</span><span class="sxs-lookup"><span data-stu-id="22c1a-111">A 64-bit operating system supports far more physical memory than a 32-bit operating system.</span></span> <span data-ttu-id="22c1a-112">例如，大部分的32位 Windows 系統最多可支援 4 gb 的實體記憶體，每個進程最多可有 3 gb 的位址空間，而64位 Windows 最多可支援 2 tb 的實體記憶體，而且每個進程都有 8 tb 的位址空間。</span><span class="sxs-lookup"><span data-stu-id="22c1a-112">For example, most 32-bit Windows systems support a maximum of 4 gigabytes of physical memory, with up to 3 gigabytes of address space for each process, while 64-bit Windows supports up to 2 terabytes of physical memory with 8 terabytes of address space for each process.</span></span> <span data-ttu-id="22c1a-113">增加的實體記憶體包含應用程式的下列優點：</span><span class="sxs-lookup"><span data-stu-id="22c1a-113">The increased physical memory includes the following benefits for applications:</span></span>

-   <span data-ttu-id="22c1a-114">每個應用程式都可以支援更多使用者。</span><span class="sxs-lookup"><span data-stu-id="22c1a-114">Each application can support more users.</span></span> <span data-ttu-id="22c1a-115">每個使用者都必須複寫每個應用程式的所有或部分，而這需要額外的記憶體。</span><span class="sxs-lookup"><span data-stu-id="22c1a-115">All or part of each application must be replicated for each user, which requires additional memory.</span></span>
-   <span data-ttu-id="22c1a-116">每個應用程式都有更好的效能。</span><span class="sxs-lookup"><span data-stu-id="22c1a-116">Each application has better performance.</span></span> <span data-ttu-id="22c1a-117">增加的實體記憶體可讓更多的應用程式同時執行，並保持在系統的主要記憶體中。</span><span class="sxs-lookup"><span data-stu-id="22c1a-117">Increased physical memory allows more applications to run simultaneously and remain completely resident in the system's main memory.</span></span> <span data-ttu-id="22c1a-118">這可減少或消除在磁片之間交換頁面的效能負面影響。</span><span class="sxs-lookup"><span data-stu-id="22c1a-118">This reduces or eliminates the performance penalty of swapping pages to and from disk.</span></span>
-   <span data-ttu-id="22c1a-119">每個應用程式都有更多記憶體來儲存及運算元據。</span><span class="sxs-lookup"><span data-stu-id="22c1a-119">Each application has more memory for data storage and manipulation.</span></span> <span data-ttu-id="22c1a-120">資料庫可以在系統的實體記憶體中儲存更多的資料。</span><span class="sxs-lookup"><span data-stu-id="22c1a-120">Databases can store more of their data in the physical memory of the system.</span></span> <span data-ttu-id="22c1a-121">資料存取速度較快，因為不需要磁片讀取。</span><span class="sxs-lookup"><span data-stu-id="22c1a-121">Data access is faster because disk reads are not necessary.</span></span>
-   <span data-ttu-id="22c1a-122">應用程式可以輕鬆且更可靠地處理大量資料。</span><span class="sxs-lookup"><span data-stu-id="22c1a-122">Applications can manipulate large amounts of data easily and more reliably.</span></span> <span data-ttu-id="22c1a-123">移動圖片工作的影片組合需要64位的 Windows，因為這個原因。</span><span class="sxs-lookup"><span data-stu-id="22c1a-123">Video composition for motion picture work requires 64-bit Windows for this reason.</span></span> <span data-ttu-id="22c1a-124">科學和財務應用程式的模型化，可從不可能在32位 Windows 上的記憶體常駐資料結構獲益。</span><span class="sxs-lookup"><span data-stu-id="22c1a-124">Modeling for scientific and financial applications benefits greatly from memory-resident data structures that are not possible on 32-bit Windows.</span></span>

<span data-ttu-id="22c1a-125">企業也有很重要的優點：</span><span class="sxs-lookup"><span data-stu-id="22c1a-125">There are also important benefits for businesses:</span></span>

-   <span data-ttu-id="22c1a-126">提高生產力。</span><span class="sxs-lookup"><span data-stu-id="22c1a-126">Increased productivity.</span></span> <span data-ttu-id="22c1a-127">知識工作者可以花時間思考和產生，而不是等待軟體完成其工作。</span><span class="sxs-lookup"><span data-stu-id="22c1a-127">Knowledge workers can spend their time thinking and producing, rather than waiting for the software to finish its tasks.</span></span>
-   <span data-ttu-id="22c1a-128">降低所有權的成本。</span><span class="sxs-lookup"><span data-stu-id="22c1a-128">Lower cost of ownership.</span></span> <span data-ttu-id="22c1a-129">每部伺服器可以支援更大量的使用者和應用程式，因此您的企業需要較少的伺服器。</span><span class="sxs-lookup"><span data-stu-id="22c1a-129">Each server can support larger numbers of users and applications, so your business will require fewer servers.</span></span> <span data-ttu-id="22c1a-130">這會直接轉譯為較少的管理額外負荷，也就是任何運算環境中最高的成本之一。</span><span class="sxs-lookup"><span data-stu-id="22c1a-130">This translates directly into less management overhead—one of the highest costs in any computing environment.</span></span>
-   <span data-ttu-id="22c1a-131">新的應用程式機會。</span><span class="sxs-lookup"><span data-stu-id="22c1a-131">New application opportunities.</span></span> <span data-ttu-id="22c1a-132">您可以設計新的應用程式，而不會有32位 Windows 所加諸的阻礙。</span><span class="sxs-lookup"><span data-stu-id="22c1a-132">New applications can be designed without the barriers imposed by 32-bit Windows.</span></span> <span data-ttu-id="22c1a-133">新的圖形應用程式可讓工作變得更簡單且更愉快。</span><span class="sxs-lookup"><span data-stu-id="22c1a-133">New graphics applications will make work easier and more enjoyable.</span></span> <span data-ttu-id="22c1a-134">目前無法使用的資料密集工作，可透過64位 Windows 來完成。</span><span class="sxs-lookup"><span data-stu-id="22c1a-134">Data-intensive tasks that are impossible today can be done with 64-bit Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="22c1a-135">本章節內容</span><span class="sxs-lookup"><span data-stu-id="22c1a-135">In this Section</span></span>

-   [<span data-ttu-id="22c1a-136">準備開始64位 Windows</span><span class="sxs-lookup"><span data-stu-id="22c1a-136">Getting Ready for 64-bit Windows</span></span>](getting-ready-for-64-bit-windows.md)
-   [<span data-ttu-id="22c1a-137">設計64位相容介面</span><span class="sxs-lookup"><span data-stu-id="22c1a-137">Designing 64-bit Compatible Interfaces</span></span>](designing-64-bit-compatible-interfaces.md)
-   [<span data-ttu-id="22c1a-138">執行32位應用程式</span><span class="sxs-lookup"><span data-stu-id="22c1a-138">Running 32-bit Applications</span></span>](running-32-bit-applications.md)
-   [<span data-ttu-id="22c1a-139">移轉提示</span><span class="sxs-lookup"><span data-stu-id="22c1a-139">Migration Tips</span></span>](migration-tips.md)

 

 




