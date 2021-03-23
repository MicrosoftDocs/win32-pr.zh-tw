---
title: 根簽章總覽
description: 根簽章是由應用程式設定，並將命令清單連結至著色器所需的資源。
ms.assetid: 2E649DA2-6CAC-4C2A-A420-D4EC0DD6EA73
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85eb5882e4a893c2933c55281f21c49f2d7d50d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548419"
---
# <a name="root-signatures-overview"></a><span data-ttu-id="11d64-103">根簽章總覽</span><span class="sxs-lookup"><span data-stu-id="11d64-103">Root Signatures Overview</span></span>

<span data-ttu-id="11d64-104">根簽章是由應用程式設定，並將命令清單連結至著色器所需的資源。</span><span class="sxs-lookup"><span data-stu-id="11d64-104">A root signature is configured by the app and links command lists to the resources the shaders require.</span></span> <span data-ttu-id="11d64-105">圖形命令清單同時具有圖形和計算根簽章。</span><span class="sxs-lookup"><span data-stu-id="11d64-105">The graphics command list has both a graphics and compute root signature.</span></span> <span data-ttu-id="11d64-106">計算命令清單只會有一個計算根簽章。</span><span class="sxs-lookup"><span data-stu-id="11d64-106">A compute command list will simply have one compute root signature.</span></span> <span data-ttu-id="11d64-107">這些根簽章彼此獨立。</span><span class="sxs-lookup"><span data-stu-id="11d64-107">These root signatures are independent of each other.</span></span>

-   [<span data-ttu-id="11d64-108">根參數和引數</span><span class="sxs-lookup"><span data-stu-id="11d64-108">Root parameters and arguments</span></span>](#root-parameters-and-arguments)
-   [<span data-ttu-id="11d64-109">根常數、描述元和資料表</span><span class="sxs-lookup"><span data-stu-id="11d64-109">Root constants, descriptors and tables</span></span>](#root-constants-descriptors-and-tables)
-   [<span data-ttu-id="11d64-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="11d64-110">Related topics</span></span>](#related-topics)

## <a name="root-parameters-and-arguments"></a><span data-ttu-id="11d64-111">根參數和引數</span><span class="sxs-lookup"><span data-stu-id="11d64-111">Root parameters and arguments</span></span>

<span data-ttu-id="11d64-112">**根** 簽章類似于 API 函式簽章，它會決定著色器應該預期的資料類型，但不會定義實際的記憶體或資料。</span><span class="sxs-lookup"><span data-stu-id="11d64-112">A **root signature** is similar to an API function signature, it determines the types of data the shaders should expect, but does not define the actual memory or data.</span></span> <span data-ttu-id="11d64-113">**根參數** 是根簽章中的一個專案。</span><span class="sxs-lookup"><span data-stu-id="11d64-113">A **root parameter** is one entry in the root signature.</span></span> <span data-ttu-id="11d64-114">在執行時間設定和變更之根參數的實際值稱為 **根引數**。</span><span class="sxs-lookup"><span data-stu-id="11d64-114">The actual values of root parameters set and changed at runtime are called **root arguments**.</span></span> <span data-ttu-id="11d64-115">變更根引數會變更著色器讀取的資料。</span><span class="sxs-lookup"><span data-stu-id="11d64-115">Changing the root arguments changes the data that the shaders read.</span></span>

## <a name="root-constants-descriptors-and-tables"></a><span data-ttu-id="11d64-116">根常數、描述元和資料表</span><span class="sxs-lookup"><span data-stu-id="11d64-116">Root constants, descriptors and tables</span></span>

<span data-ttu-id="11d64-117">根簽章可以包含三種類型的參數;根常數 (常數內嵌于根引數) 、根引數 (描述項內嵌于根引數) ，以及描述項資料表 (描述項堆積中的描述項範圍) 指標。</span><span class="sxs-lookup"><span data-stu-id="11d64-117">The root signature can contain three types of parameters; root constants (constants inlined in the root arguments), root descriptors (descriptors inlined in the root arguments), and descriptor tables (pointers to a range of descriptors in the descriptor heap).</span></span>

<span data-ttu-id="11d64-118">根常數是內嵌的32位值，在著色器中會顯示為常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="11d64-118">The root constants are inline 32-bit values that show up in the shader as a constant buffer.</span></span>

<span data-ttu-id="11d64-119">內嵌的根目錄描述項應該包含最常存取的描述元，但限制為 CBVs，以及原始或結構化 UAV 或 SRV 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="11d64-119">The inlined root descriptors should contain descriptors that are accessed most often, though is limited to CBVs, and raw or structured UAV or SRV buffers.</span></span> <span data-ttu-id="11d64-120">較複雜的類型（例如2D 材質 SRV）不能用來做為根描述項。</span><span class="sxs-lookup"><span data-stu-id="11d64-120">A more complex type, such as a 2D texture SRV, cannot be used as a root descriptor.</span></span> <span data-ttu-id="11d64-121">根描述項不包含大小限制，因此不會有超出界限的檢查，與描述項堆積中的描述項不同，它包含大小。</span><span class="sxs-lookup"><span data-stu-id="11d64-121">Root descriptors do not include a size limit, so there can be no out-of-bounds checking, unlike descriptors in descriptor heaps, which do include a size.</span></span>

<span data-ttu-id="11d64-122">根簽章內的描述項資料表專案包含描述元、HLSL 著色器系結名稱和可見度旗標。</span><span class="sxs-lookup"><span data-stu-id="11d64-122">Descriptor table entries within root signatures contain the descriptor, HLSL shader bind name and visibility flag.</span></span> <span data-ttu-id="11d64-123">請參閱 [著色器模型 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) ，以取得著色器名稱的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="11d64-123">Refer to [Shader Model 5.1](/windows/desktop/direct3dhlsl/shader-model-5-1) for details of shader names.</span></span> <span data-ttu-id="11d64-124">在某些硬體上，只有在需要它們的著色器階段可以看見描述項時，才會有效能提升 (參考 [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)) 。</span><span class="sxs-lookup"><span data-stu-id="11d64-124">On some hardware, there can be a performance gain from only making descriptors visible to the shader stages that require them (refer to [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)).</span></span>

![根描述中繼資料表專案](images/root-descriptor-table.png)

<span data-ttu-id="11d64-126">根簽章的配置相當有彈性，而某些條件約束會強加于較少的可用硬體。</span><span class="sxs-lookup"><span data-stu-id="11d64-126">The layout of the root signature is quite flexible, with some constraints imposed on less capable hardware.</span></span> <span data-ttu-id="11d64-127">無論硬體層級為何，應用程式一律會盡可能地嘗試使根簽章盡可能小，以達到最高效率。</span><span class="sxs-lookup"><span data-stu-id="11d64-127">Regardless of the level of hardware, applications should always try to make the root signature as small as needed for maximum efficiency.</span></span> <span data-ttu-id="11d64-128">應用程式可以權衡根簽章中有更多描述中繼資料表，但不包含根常數的空間，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="11d64-128">Applications can trade off having more descriptor tables in the root signature but less room for root constants, or vice versa.</span></span>

<span data-ttu-id="11d64-129">根簽章的內容 (描述中繼資料表、根常數和根描述元，) 當繪圖 (圖形) /dispatch (計算) 呼叫之間的任何內容變更時，D3D12 驅動程式會自動取得該應用程式的版本。</span><span class="sxs-lookup"><span data-stu-id="11d64-129">The contents of the root signature (the descriptor tables, root constants and root descriptors) that the application has bound automatically get versioned by the D3D12 driver whenever any part of the contents change between draw (graphics)/dispatch (compute) calls.</span></span> <span data-ttu-id="11d64-130">因此每個 draw/分派都會取得一組獨特的完整根簽章狀態。</span><span class="sxs-lookup"><span data-stu-id="11d64-130">So each draw/dispatch gets a unique full set of root signature state.</span></span>

<span data-ttu-id="11d64-131">在理想的情況下，會有 (Pso) 共用相同根簽章的管線狀態物件群組。</span><span class="sxs-lookup"><span data-stu-id="11d64-131">Ideally, there are groups of Pipeline State Objects (PSOs) that share the same root signature.</span></span> <span data-ttu-id="11d64-132">在管線上設定根簽章之後，它定義 (描述中繼資料表、描述元、常數) 的所有系結都可以個別設定或變更，包括對組合的繼承。</span><span class="sxs-lookup"><span data-stu-id="11d64-132">After a root signature is set on the pipeline, all the bindings that it defines (descriptor tables, descriptors, constants) can each be individually set or changed, including inheritance into bundles.</span></span>

<span data-ttu-id="11d64-133">應用程式可以在其所需的兩個描述中繼資料表之間進行取捨，以取得更多空間，但會移除間接) 的內嵌常數 (，在根簽章中沒有間接) 的 (。</span><span class="sxs-lookup"><span data-stu-id="11d64-133">An app can make its own tradeoff between how many descriptor tables it wants verses inline descriptors (which take more space but remove an indirection) verses inline constants (which have no indirection) they want in the root signature.</span></span> <span data-ttu-id="11d64-134">應用程式應該盡可能謹慎地使用根簽章，依賴應用程式控制的記憶體，例如指向它們的堆積和描述元，以代表大量資料。</span><span class="sxs-lookup"><span data-stu-id="11d64-134">Applications should use the root signature as sparingly as possible, relying on application controlled memory such as heaps and descriptor heaps pointing into them to represent bulk data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11d64-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="11d64-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11d64-136">根簽章</span><span class="sxs-lookup"><span data-stu-id="11d64-136">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 