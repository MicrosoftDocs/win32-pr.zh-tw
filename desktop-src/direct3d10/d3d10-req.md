---
description: 資源限制常數。
ms.assetid: a6bfba45-7a0c-4894-a0a6-ee468002175d
title: D3D10_REQ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1d6bf4f72c4ef09eafba3ee50659e5e6ffc682
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317884"
---
# <a name="d3d10_req"></a><span data-ttu-id="ad6c7-103">D3D10 \_ 需求</span><span class="sxs-lookup"><span data-stu-id="ad6c7-103">D3D10\_REQ</span></span>

<span data-ttu-id="ad6c7-104">資源限制常數。</span><span class="sxs-lookup"><span data-stu-id="ad6c7-104">Resource limitation constants.</span></span>



| <span data-ttu-id="ad6c7-105">\#定義</span><span class="sxs-lookup"><span data-stu-id="ad6c7-105">\#define</span></span>                                      | <span data-ttu-id="ad6c7-106">值</span><span class="sxs-lookup"><span data-stu-id="ad6c7-106">Value</span></span> | <span data-ttu-id="ad6c7-107">描述</span><span class="sxs-lookup"><span data-stu-id="ad6c7-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad6c7-108">D3D10 \_ 需求 \_ MIP \_ 層級</span><span class="sxs-lookup"><span data-stu-id="ad6c7-108">D3D10\_REQ\_MIP\_LEVELS</span></span>                       | <span data-ttu-id="ad6c7-109">14</span><span class="sxs-lookup"><span data-stu-id="ad6c7-109">14</span></span>    | <span data-ttu-id="ad6c7-110">材質資源可能擁有的最大 mipmap 層級數目。</span><span class="sxs-lookup"><span data-stu-id="ad6c7-110">Maximum number of mipmap levels a texture resource may have.</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ad6c7-111">D3D10 \_ 需求 \_ 資源 \_ 大小 \_ \_ （以 mb 為單位）</span><span class="sxs-lookup"><span data-stu-id="ad6c7-111">D3D10\_REQ\_RESOURCE\_SIZE\_IN\_MEGABYTES</span></span>     | <span data-ttu-id="ad6c7-112">128</span><span class="sxs-lookup"><span data-stu-id="ad6c7-112">128</span></span>   | <span data-ttu-id="ad6c7-113">資源的最大可能大小（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="ad6c7-113">Maximum possible size of a resource in megabytes.</span></span> <span data-ttu-id="ad6c7-114">應用程式可以建立大於某些圖形硬體上資源大小上限的資源。</span><span class="sxs-lookup"><span data-stu-id="ad6c7-114">Apps can create resources bigger than the maximum resource size on some graphics hardware.</span></span> <span data-ttu-id="ad6c7-115">不過，建議應用程式將資源保留在資源大小上限的範圍內，以取得圖形廠商之間的最大相容性數量。</span><span class="sxs-lookup"><span data-stu-id="ad6c7-115">However, we recommend that apps keep resources smaller than the maximum resource size to get the maximum amount of compatibility across graphics vendors.</span></span> <span data-ttu-id="ad6c7-116">執行時間只會保證所有 Direct3D 10 硬體都支援資源大小上限內的配置。</span><span class="sxs-lookup"><span data-stu-id="ad6c7-116">The runtime only guarantees that allocations within the maximum resource size are supported by all Direct3D 10 hardware.</span></span> |
| <span data-ttu-id="ad6c7-117">D3D10 \_ 需求 \_ TEXTURE1D \_ 陣列 \_ 軸 \_ 維度</span><span class="sxs-lookup"><span data-stu-id="ad6c7-117">D3D10\_REQ\_TEXTURE1D\_ARRAY\_AXIS\_DIMENSION</span></span> | <span data-ttu-id="ad6c7-118">512</span><span class="sxs-lookup"><span data-stu-id="ad6c7-118">512</span></span>   | <span data-ttu-id="ad6c7-119">1D 材質陣列的陣列大小上限。</span><span class="sxs-lookup"><span data-stu-id="ad6c7-119">Maximum array size of a 1D texture array.</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ad6c7-120">D3D10 \_ 需求 \_ TEXTURE2D \_ 陣列 \_ 軸 \_ 維度</span><span class="sxs-lookup"><span data-stu-id="ad6c7-120">D3D10\_REQ\_TEXTURE2D\_ARRAY\_AXIS\_DIMENSION</span></span> | <span data-ttu-id="ad6c7-121">512</span><span class="sxs-lookup"><span data-stu-id="ad6c7-121">512</span></span>   | <span data-ttu-id="ad6c7-122">2D 材質陣列的陣列大小上限。</span><span class="sxs-lookup"><span data-stu-id="ad6c7-122">Maximum array size of a 2D texture array.</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ad6c7-123">D3D10 \_ 需求 \_ TEXTURE1D \_ U \_ 維度</span><span class="sxs-lookup"><span data-stu-id="ad6c7-123">D3D10\_REQ\_TEXTURE1D\_U\_DIMENSION</span></span>           | <span data-ttu-id="ad6c7-124">8192</span><span class="sxs-lookup"><span data-stu-id="ad6c7-124">8192</span></span>  | <span data-ttu-id="ad6c7-125">1D 材質的最大寬度。</span><span class="sxs-lookup"><span data-stu-id="ad6c7-125">Maximum width of a 1D texture.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ad6c7-126">D3D10 \_ 需求 \_ TEXTURE2D \_ U \_ 或 \_ V \_ 維度</span><span class="sxs-lookup"><span data-stu-id="ad6c7-126">D3D10\_REQ\_TEXTURE2D\_U\_OR\_V\_DIMENSION</span></span>    | <span data-ttu-id="ad6c7-127">8192</span><span class="sxs-lookup"><span data-stu-id="ad6c7-127">8192</span></span>  | <span data-ttu-id="ad6c7-128">2D 材質的最大寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="ad6c7-128">Maximum width and height of a 2D texture.</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ad6c7-129">D3D10 \_ 需求 \_ TEXTURE3D \_ U \_ V \_ 或 \_ W \_ 維度</span><span class="sxs-lookup"><span data-stu-id="ad6c7-129">D3D10\_REQ\_TEXTURE3D\_U\_V\_OR\_W\_DIMENSION</span></span> | <span data-ttu-id="ad6c7-130">2048</span><span class="sxs-lookup"><span data-stu-id="ad6c7-130">2048</span></span>  | <span data-ttu-id="ad6c7-131">3D 紋理的最大寬度、高度和深度。</span><span class="sxs-lookup"><span data-stu-id="ad6c7-131">Maximum width, height, and depth of a 3D texture.</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ad6c7-132">D3D10 \_ 需求 \_ TEXTURECUBE \_ 維度</span><span class="sxs-lookup"><span data-stu-id="ad6c7-132">D3D10\_REQ\_TEXTURECUBE\_DIMENSION</span></span>            | <span data-ttu-id="ad6c7-133">8192</span><span class="sxs-lookup"><span data-stu-id="ad6c7-133">8192</span></span>  | <span data-ttu-id="ad6c7-134">Cube 材質的大小上限。</span><span class="sxs-lookup"><span data-stu-id="ad6c7-134">Maximum size of a cube texture.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="ad6c7-135">常數定義于 D3D10 中。</span><span class="sxs-lookup"><span data-stu-id="ad6c7-135">The constants are defined in D3D10.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad6c7-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad6c7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad6c7-137">資源常數</span><span class="sxs-lookup"><span data-stu-id="ad6c7-137">Resource Constants</span></span>](d3d10-graphics-reference-resource-constants.md)
</dt> <dt>

[<span data-ttu-id="ad6c7-138">Direct3D 參考</span><span class="sxs-lookup"><span data-stu-id="ad6c7-138">Direct3D Reference</span></span>](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 



