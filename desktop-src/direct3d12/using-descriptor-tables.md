---
title: 使用描述中繼資料表
description: 描述項資料表中，每個都識別描述元堆積中的範圍，都會系結至命令清單上目前的根簽章所定義的位置。
ms.assetid: 4ECEC07A-7ABC-4C5F-B23C-36F0D92643FE
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e589274fbb93e48e4d65e545a62999e654b7688f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104961"
---
# <a name="using-descriptor-tables"></a><span data-ttu-id="e64d6-103">使用描述中繼資料表</span><span class="sxs-lookup"><span data-stu-id="e64d6-103">Using Descriptor Tables</span></span>

<span data-ttu-id="e64d6-104">描述項資料表中，每個都識別描述元堆積中的範圍，都會系結至命令清單上目前的根簽章所定義的位置。</span><span class="sxs-lookup"><span data-stu-id="e64d6-104">Descriptor tables, each identifying a range in a descriptor heap, are bound at slots defined by the current root signature on a command list.</span></span>

-   [<span data-ttu-id="e64d6-105">索引描述中繼資料表</span><span class="sxs-lookup"><span data-stu-id="e64d6-105">Indexing Descriptor Tables</span></span>](#indexing-descriptor-tables)
-   [<span data-ttu-id="e64d6-106">相關主題</span><span class="sxs-lookup"><span data-stu-id="e64d6-106">Related topics</span></span>](#related-topics)

<span data-ttu-id="e64d6-107">著色器可以找出組成描述中繼資料表的描述項所參考的資源。</span><span class="sxs-lookup"><span data-stu-id="e64d6-107">Shaders can locate resources referenced by the descriptors that make up the descriptor table.</span></span> <span data-ttu-id="e64d6-108">其他資源系結：索引緩衝區、頂點緩衝區、資料流程輸出緩衝區、轉譯目標和深度樣板都是直接在命令清單上完成，而不是透過描述項。</span><span class="sxs-lookup"><span data-stu-id="e64d6-108">Other resource bindings - Index Buffers, Vertex Buffer, Stream Output Buffers, Render Targets, and Depth Stencil are done directly on a command list rather than via descriptors.</span></span> <span data-ttu-id="e64d6-109">總括來說：</span><span class="sxs-lookup"><span data-stu-id="e64d6-109">To summarize:</span></span>

<span data-ttu-id="e64d6-110">下列資源參考可以共用相同的描述中繼資料表和堆積：</span><span class="sxs-lookup"><span data-stu-id="e64d6-110">The following resource references can share the same descriptor table and heap:</span></span>

-   <span data-ttu-id="e64d6-111">著色器資源檢視</span><span class="sxs-lookup"><span data-stu-id="e64d6-111">Shader resource views</span></span>
-   <span data-ttu-id="e64d6-112">未排序的存取權視圖</span><span class="sxs-lookup"><span data-stu-id="e64d6-112">Unordered access views</span></span>
-   <span data-ttu-id="e64d6-113">常數緩衝區查看</span><span class="sxs-lookup"><span data-stu-id="e64d6-113">Constant buffer views</span></span>

<span data-ttu-id="e64d6-114">下列資源參考必須位於自己的描述元堆積中：</span><span class="sxs-lookup"><span data-stu-id="e64d6-114">The following resource references must be in their own descriptor heap:</span></span>

-   <span data-ttu-id="e64d6-115">取樣器</span><span class="sxs-lookup"><span data-stu-id="e64d6-115">Samplers</span></span>

<span data-ttu-id="e64d6-116">下列資源不會放在描述中繼資料表或堆積中，而是直接使用命令清單進行系結：</span><span class="sxs-lookup"><span data-stu-id="e64d6-116">The following resources are not placed in descriptor tables or heaps, but are bound directly using command lists:</span></span>

-   <span data-ttu-id="e64d6-117">索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="e64d6-117">Index buffers</span></span>
-   <span data-ttu-id="e64d6-118">頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="e64d6-118">Vertex buffers</span></span>
-   <span data-ttu-id="e64d6-119">串流輸出緩衝區</span><span class="sxs-lookup"><span data-stu-id="e64d6-119">Stream output buffers</span></span>
-   <span data-ttu-id="e64d6-120">呈現目標</span><span class="sxs-lookup"><span data-stu-id="e64d6-120">Render targets</span></span>
-   <span data-ttu-id="e64d6-121">深度樣板視圖</span><span class="sxs-lookup"><span data-stu-id="e64d6-121">Depth stencil views</span></span>

## <a name="indexing-descriptor-tables"></a><span data-ttu-id="e64d6-122">索引描述中繼資料表</span><span class="sxs-lookup"><span data-stu-id="e64d6-122">Indexing Descriptor Tables</span></span>

<span data-ttu-id="e64d6-123">著色器無法從著色器中給定的呼叫位置，以動態方式從描述項資料表界限進行索引編制。</span><span class="sxs-lookup"><span data-stu-id="e64d6-123">Shaders cannot dynamically index across descriptor table boundaries from a given call-site in the shader.</span></span> <span data-ttu-id="e64d6-124">不過，您可以在描述中繼資料表中選取描述項，以在相同描述元類型範圍內的著色器程式碼中動態編制索引， (例如在 SRVs) 的連續區域中編制索引。</span><span class="sxs-lookup"><span data-stu-id="e64d6-124">However, the selection of a descriptor within a descriptor table is allowed to be dynamically indexed in shader code within ranges of the same descriptor type (such as indexing across a contiguous region of SRVs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e64d6-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="e64d6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e64d6-126">描述中繼資料表</span><span class="sxs-lookup"><span data-stu-id="e64d6-126">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> </dl>

 

 




