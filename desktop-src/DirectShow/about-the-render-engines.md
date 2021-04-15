---
description: 關於轉譯引擎
ms.assetid: 80299b1a-09bf-4660-95d3-41a2b0074745
title: 關於轉譯引擎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fe3a9956bee0d167de9e6618187bfd1f2a6e39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510220"
---
# <a name="about-the-render-engines"></a><span data-ttu-id="0c576-103">關於轉譯引擎</span><span class="sxs-lookup"><span data-stu-id="0c576-103">About the Render Engines</span></span>

<span data-ttu-id="0c576-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="0c576-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="0c576-105">本文說明 [DirectShow 編輯服務](directshow-editing-services.md) (DES) 如何呈現影片編輯專案。</span><span class="sxs-lookup"><span data-stu-id="0c576-105">This article describes how [DirectShow Editing Services](directshow-editing-services.md) (DES) renders a video editing project.</span></span>

<span data-ttu-id="0c576-106">在 DES 中，專案會以時間軸表示。</span><span class="sxs-lookup"><span data-stu-id="0c576-106">In DES, a project is represented as a timeline.</span></span> <span data-ttu-id="0c576-107">時間軸會很有用，因為它可簡化影片編輯中最常見的工作，例如重新排列來源剪輯以及新增影片效果。</span><span class="sxs-lookup"><span data-stu-id="0c576-107">The timeline is useful because it simplifies the most common tasks in video editing, such as rearranging source clips and adding video effects.</span></span> <span data-ttu-id="0c576-108">另一方面，DirectShow 資料流程架構需要篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="0c576-108">The DirectShow stream architecture, on the other hand, requires a filter graph.</span></span> <span data-ttu-id="0c576-109">因此，若要轉譯您的專案，您必須將時間軸轉譯為篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="0c576-109">Thus, to render your project, you must translate a timeline into a filter graph.</span></span> <span data-ttu-id="0c576-110">執行這項工作的元件稱為轉譯 *引擎*。</span><span class="sxs-lookup"><span data-stu-id="0c576-110">The component that does this is called a *render engine*.</span></span> <span data-ttu-id="0c576-111">DirectShow 提供兩種轉譯引擎：</span><span class="sxs-lookup"><span data-stu-id="0c576-111">DirectShow provides two render engines:</span></span>

-   <span data-ttu-id="0c576-112">基本轉譯引擎：建立可傳遞未壓縮輸出的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="0c576-112">Basic render engine: Builds a filter graph that delivers uncompressed output.</span></span>
-   <span data-ttu-id="0c576-113">智慧型轉譯引擎：建立可傳遞壓縮輸出的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="0c576-113">Smart render engine: Builds a filter graph that delivers compressed output.</span></span>

<span data-ttu-id="0c576-114">智慧型轉譯引擎會使用智慧型 recompression 來改善效能。</span><span class="sxs-lookup"><span data-stu-id="0c576-114">The smart render engine uses smart recompression to improve performance.</span></span> <span data-ttu-id="0c576-115">使用智慧型 recompression 時，只有在原始檔案格式與最終輸出格式不同時，才會 recompressed 來源檔案。</span><span class="sxs-lookup"><span data-stu-id="0c576-115">With smart recompression, source files are recompressed only when the original file format differs from the final output format.</span></span> <span data-ttu-id="0c576-116">如果格式相符，則永遠不會解壓縮來源。</span><span class="sxs-lookup"><span data-stu-id="0c576-116">If the formats match, the source is never decompressed.</span></span> <span data-ttu-id="0c576-117">只有視訊壓縮支援 Smart recompression，不適用於音訊壓縮。</span><span class="sxs-lookup"><span data-stu-id="0c576-117">Smart recompression is supported only for video compression, not for audio compression.</span></span>

<span data-ttu-id="0c576-118">若為預覽版本，請使用基本轉譯引擎。</span><span class="sxs-lookup"><span data-stu-id="0c576-118">For preview, use the basic render engine.</span></span> <span data-ttu-id="0c576-119">智慧型轉譯引擎也可以預覽，但效率較低，因為它必須解壓縮壓縮的資料流程。</span><span class="sxs-lookup"><span data-stu-id="0c576-119">The smart render engine can also preview, but less efficiently because it has to decompress the compressed stream.</span></span> <span data-ttu-id="0c576-120">針對寫入檔案，如果您想要 smart recompression，請使用智慧型轉譯引擎。</span><span class="sxs-lookup"><span data-stu-id="0c576-120">For writing files, use the smart render engine if you want smart recompression.</span></span> <span data-ttu-id="0c576-121">否則，請使用基本轉譯引擎。</span><span class="sxs-lookup"><span data-stu-id="0c576-121">Otherwise, use the basic render engine.</span></span> <span data-ttu-id="0c576-122">Smart recompression 可以大幅減少寫入檔案所花費的時間。</span><span class="sxs-lookup"><span data-stu-id="0c576-122">Smart recompression can greatly reduce the time it takes to write the file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c576-123">請勿使用智慧型轉譯引擎來讀取或寫入 Windows Media 檔案。</span><span class="sxs-lookup"><span data-stu-id="0c576-123">Do not use the smart render engine to read or write Windows Media files.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="0c576-124">這兩種轉譯引擎都會建立一個不可見的視窗來處理訊息。</span><span class="sxs-lookup"><span data-stu-id="0c576-124">Both render engines create an invisible window that processes messages.</span></span> <span data-ttu-id="0c576-125">建立轉譯引擎的執行緒必須有訊息迴圈，才能分派訊息。</span><span class="sxs-lookup"><span data-stu-id="0c576-125">The thread that creates the render engine must have a message loop, to dispatch messages.</span></span> <span data-ttu-id="0c576-126">此外，必須等到轉譯引擎和篩選圖形管理員釋出之後，該執行緒才能結束。</span><span class="sxs-lookup"><span data-stu-id="0c576-126">Also, that thread must not exit until the Render Engine and the Filter Graph Manager are released.</span></span> <span data-ttu-id="0c576-127">否則，應用程式可能會鎖死。</span><span class="sxs-lookup"><span data-stu-id="0c576-127">Otherwise, the application might deadlock.</span></span>

 

<span data-ttu-id="0c576-128">建立篩選圖形</span><span class="sxs-lookup"><span data-stu-id="0c576-128">Constructing the Filter Graph</span></span>

<span data-ttu-id="0c576-129">篩選圖形的建立方式有兩個階段。</span><span class="sxs-lookup"><span data-stu-id="0c576-129">The filter graph is built in two stages.</span></span> <span data-ttu-id="0c576-130">在第一個階段中，轉譯引擎會構造「前端」，這是部分篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="0c576-130">In the first stage, the render engine constructs a "front end," which is a partial filter graph.</span></span> <span data-ttu-id="0c576-131">下圖說明典型的前端：</span><span class="sxs-lookup"><span data-stu-id="0c576-131">The following diagram illustrates a typical front end:</span></span>

![篩選圖形前端](images/rendeng1.png)

<span data-ttu-id="0c576-133">子系統包含各種不同的特殊篩選準則，轉譯引擎會自動組合這些篩選器。</span><span class="sxs-lookup"><span data-stu-id="0c576-133">The subsystems contain various specialized filters, which the render engine assembles automatically.</span></span> <span data-ttu-id="0c576-134">前端在時間軸中包含每個群組的一個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="0c576-134">The front end contains one output pin for each group in the timeline.</span></span> <span data-ttu-id="0c576-135">如果您使用基本轉譯引擎，輸出圖釘會傳遞未壓縮的資料，如果您使用智慧型轉譯引擎，則會傳遞壓縮的資料。</span><span class="sxs-lookup"><span data-stu-id="0c576-135">The output pins deliver uncompressed data if you use the basic render engine, or compressed data if you use the smart render engine.</span></span>

<span data-ttu-id="0c576-136">在第二個步驟中，輸出圖釘會連接到轉譯篩選。</span><span class="sxs-lookup"><span data-stu-id="0c576-136">In the second step, the output pins are connected to rendering filters.</span></span> <span data-ttu-id="0c576-137">針對預覽，轉譯篩選器為影片和音訊轉譯器。</span><span class="sxs-lookup"><span data-stu-id="0c576-137">For preview, the rendering filters are video and audio renderers.</span></span> <span data-ttu-id="0c576-138">針對檔案寫入，轉譯篩選器是 (mux) 篩選器和檔案寫入器篩選器的多工器。</span><span class="sxs-lookup"><span data-stu-id="0c576-138">For file writing, the rendering filters are multiplexer (mux) filters and file-writer filters.</span></span>

![完成篩選圖形](images/rendeng2.png)

## <a name="related-topics"></a><span data-ttu-id="0c576-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="0c576-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c576-141">預覽專案</span><span class="sxs-lookup"><span data-stu-id="0c576-141">Previewing a Project</span></span>](previewing-a-project.md)
</dt> <dt>

[<span data-ttu-id="0c576-142">將專案寫入檔案</span><span class="sxs-lookup"><span data-stu-id="0c576-142">Writing a Project to a File</span></span>](writing-a-project-to-a-file.md)
</dt> </dl>

 

 



