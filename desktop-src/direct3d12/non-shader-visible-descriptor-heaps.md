---
title: 非著色器可見描述元堆積
description: 部分描述元堆積無法透過描述項資料表來參考著色器，但存在於記錄命令清單之前，或因為不需要著色器可見的堆積，以協助應用程式暫存描述項。
ms.assetid: 85934873-8889-4564-A717-28A00614B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 894640cde142f1241b088518ba7140ffb9405152
ms.sourcegitcommit: 015fb35e736a235d3c9becff1f6832a0965b4303
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548377"
---
# <a name="non-shader-visible-descriptor-heaps"></a><span data-ttu-id="b2bb3-103">非著色器可見描述元堆積</span><span class="sxs-lookup"><span data-stu-id="b2bb3-103">Non Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="b2bb3-104">部分描述元堆積無法透過描述項資料表來參考著色器，但存在於記錄命令清單之前，或因為不需要著色器可見的堆積，以協助應用程式暫存描述項。</span><span class="sxs-lookup"><span data-stu-id="b2bb3-104">Some descriptor heaps cannot be referenced by shaders through descriptor tables, but exist either to assist the app in staging the descriptors prior to recording a command list or because no shader-visible heap is required.</span></span>

-   [<span data-ttu-id="b2bb3-105">非可見的視圖</span><span class="sxs-lookup"><span data-stu-id="b2bb3-105">Non-visible views</span></span>](#non-visible-views)
-   [<span data-ttu-id="b2bb3-106">總結</span><span class="sxs-lookup"><span data-stu-id="b2bb3-106">Summary</span></span>](#summary)
-   [<span data-ttu-id="b2bb3-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2bb3-107">Related topics</span></span>](#related-topics)

## <a name="non-visible-views"></a><span data-ttu-id="b2bb3-108">非可見的視圖</span><span class="sxs-lookup"><span data-stu-id="b2bb3-108">Non-visible views</span></span>

<span data-ttu-id="b2bb3-109">所有描述元堆積（包括先前所述的著色器可存取描述元），都可以由 CPU 和/或命令清單操作，這取決於應用程式針對描述項堆積所選取的記憶體集區和 CPU 存取屬性。</span><span class="sxs-lookup"><span data-stu-id="b2bb3-109">All descriptor heaps, including the shader accessible descriptor heaps described previously, can be manipulated by the CPU and/or command lists depending on the memory pool and CPU access properties the application selects for a descriptor heap.</span></span>

<span data-ttu-id="b2bb3-110">若為 [著色器可見的描述](shader-visible-descriptor-heaps.md)項堆積，則在暫存這些描述元時拒絕著色器存取的明顯原因。</span><span class="sxs-lookup"><span data-stu-id="b2bb3-110">For [Shader Visible Descriptor Heaps](shader-visible-descriptor-heaps.md), the obvious reason to deny shader access to these descriptor heaps is while they are being staged.</span></span> <span data-ttu-id="b2bb3-111">然後，這些堆積會顯示為著色器，並在命令清單執行時透過描述項資料表來存取。</span><span class="sxs-lookup"><span data-stu-id="b2bb3-111">Then these heaps are made shader-visible, and accessed via descriptor tables at command list execution.</span></span> <span data-ttu-id="b2bb3-112">但是，不需要暫存著色器可見的堆積，而是可以直接填入。</span><span class="sxs-lookup"><span data-stu-id="b2bb3-112">However, there is no requirement to stage shader-visible heaps, they can be populated directly.</span></span>

<span data-ttu-id="b2bb3-113">其他描述元會將其內容直接記錄到命令清單中，以系結至管線。</span><span class="sxs-lookup"><span data-stu-id="b2bb3-113">Other descriptors get bound to the pipeline by having their contents recorded directly into the command list.</span></span> <span data-ttu-id="b2bb3-114">這些描述項只提供在命令清單記錄時間轉譯 view 參數。</span><span class="sxs-lookup"><span data-stu-id="b2bb3-114">These descriptors only serve to translate the view parameters at command list record time.</span></span> <span data-ttu-id="b2bb3-115">這些堆積一律為非著色器的可見度，並包含下列各項。</span><span class="sxs-lookup"><span data-stu-id="b2bb3-115">These heaps are always non-shader visible and contain the following.</span></span>

-   <span data-ttu-id="b2bb3-116"> (RTVs) 呈現目標視圖</span><span class="sxs-lookup"><span data-stu-id="b2bb3-116">Render Target Views (RTVs)</span></span>
-   <span data-ttu-id="b2bb3-117">深度樣板視圖 (Dsv) </span><span class="sxs-lookup"><span data-stu-id="b2bb3-117">Depth Stencil Views (DSVs)</span></span>

<span data-ttu-id="b2bb3-118">索引緩衝區視圖 (IBVs) 、頂點緩衝區視圖 (VBVs) ，以及串流輸出視圖 (SOVs) 直接傳遞給 API 方法，所以沒有特定的堆積類型。</span><span class="sxs-lookup"><span data-stu-id="b2bb3-118">Index Buffer Views (IBVs), Vertex Buffer Views (VBVs), and Stream Output Views (SOVs) are passed directly to API methods, are do not have specific heap types.</span></span>

<span data-ttu-id="b2bb3-119">在記錄至命令清單之後 (呼叫（例如 [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)），例如) 用來保存此呼叫之描述項的記憶體可立即在呼叫後重複使用。</span><span class="sxs-lookup"><span data-stu-id="b2bb3-119">After recording into the command list (with a call such as [**OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets), for example) the memory used to hold the descriptors for this call is immediately available for re-use after the call.</span></span>

<span data-ttu-id="b2bb3-120">即使是描述中繼資料表，也有一些選項可讓應用程式選擇在命令清單記錄中記錄資料表內容 (而不是在執行) 時對資料表指標進行取值。</span><span class="sxs-lookup"><span data-stu-id="b2bb3-120">Even descriptor tables have options where an app can allow the implementation to choose to record the table contents at command list recording (rather than dereference the table pointer at execution).</span></span>

## <a name="summary"></a><span data-ttu-id="b2bb3-121">總結</span><span class="sxs-lookup"><span data-stu-id="b2bb3-121">Summary</span></span>



|                   |                                    |                                        |
|-------------------|------------------------------------|----------------------------------------|
|                   | <span data-ttu-id="b2bb3-122">**著色器可見、僅限 CPU 寫入**</span><span class="sxs-lookup"><span data-stu-id="b2bb3-122">**shader visible, CPU write only**</span></span> | <span data-ttu-id="b2bb3-123">**非著色器可見、CPU 讀取/寫入**</span><span class="sxs-lookup"><span data-stu-id="b2bb3-123">**non-shader visible, CPU read/write**</span></span> |
| <span data-ttu-id="b2bb3-124">**CBV，SRV，UAV**</span><span class="sxs-lookup"><span data-stu-id="b2bb3-124">**CBV, SRV, UAV**</span></span> | <span data-ttu-id="b2bb3-125">是</span><span class="sxs-lookup"><span data-stu-id="b2bb3-125">yes</span></span>                                | <span data-ttu-id="b2bb3-126">是</span><span class="sxs-lookup"><span data-stu-id="b2bb3-126">yes</span></span>                                    |
| <span data-ttu-id="b2bb3-127">**採樣**</span><span class="sxs-lookup"><span data-stu-id="b2bb3-127">**SAMPLER**</span></span>       | <span data-ttu-id="b2bb3-128">是</span><span class="sxs-lookup"><span data-stu-id="b2bb3-128">yes</span></span>                                | <span data-ttu-id="b2bb3-129">是</span><span class="sxs-lookup"><span data-stu-id="b2bb3-129">yes</span></span>                                    |
| <span data-ttu-id="b2bb3-130">**RTV**</span><span class="sxs-lookup"><span data-stu-id="b2bb3-130">**RTV**</span></span>           | <span data-ttu-id="b2bb3-131">不可以</span><span class="sxs-lookup"><span data-stu-id="b2bb3-131">no</span></span>                                 | <span data-ttu-id="b2bb3-132">是</span><span class="sxs-lookup"><span data-stu-id="b2bb3-132">yes</span></span>                                    |
| <span data-ttu-id="b2bb3-133">**DSV**</span><span class="sxs-lookup"><span data-stu-id="b2bb3-133">**DSV**</span></span>           | <span data-ttu-id="b2bb3-134">不可以</span><span class="sxs-lookup"><span data-stu-id="b2bb3-134">no</span></span>                                 | <span data-ttu-id="b2bb3-135">是</span><span class="sxs-lookup"><span data-stu-id="b2bb3-135">yes</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="b2bb3-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2bb3-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2bb3-137">描述元堆積</span><span class="sxs-lookup"><span data-stu-id="b2bb3-137">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




