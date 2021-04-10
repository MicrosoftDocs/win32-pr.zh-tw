---
title: D3D9 和 D3D8 宣告之間的對應
description: 此資料表會將 D3DVERTEXELEMENT9 宣告的成員對應至 Direct3D 8 宣告。
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c52bd804907f201916386ef5fa5776a32a046b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687452"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a><span data-ttu-id="3e47f-103">D3D9 和 D3D8 宣告之間的對應</span><span class="sxs-lookup"><span data-stu-id="3e47f-103">Map between D3D9 and D3D8 declarations</span></span>

<span data-ttu-id="3e47f-104">此資料表會將 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) 宣告的成員對應至 Direct3D 8 宣告。</span><span class="sxs-lookup"><span data-stu-id="3e47f-104">This table maps members of a [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) declaration to a Direct3D 8 declaration.</span></span>



| <span data-ttu-id="3e47f-105">Direct3D 9 使用量</span><span class="sxs-lookup"><span data-stu-id="3e47f-105">Direct3D 9 Usage</span></span>           | <span data-ttu-id="3e47f-106">Direct3D 9 使用方式索引</span><span class="sxs-lookup"><span data-stu-id="3e47f-106">Direct3D 9 Usage index</span></span> | <span data-ttu-id="3e47f-107">Direct3D 8</span><span class="sxs-lookup"><span data-stu-id="3e47f-107">Direct3D 8</span></span>            |
|----------------------------|------------------------|-----------------------|
| <span data-ttu-id="3e47f-108">D3DDECLUSAGE \_ 位置</span><span class="sxs-lookup"><span data-stu-id="3e47f-108">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="3e47f-109">0</span><span class="sxs-lookup"><span data-stu-id="3e47f-109">0</span></span>                      | <span data-ttu-id="3e47f-110">D3DVSDE \_ 位置</span><span class="sxs-lookup"><span data-stu-id="3e47f-110">D3DVSDE\_POSITION</span></span>     |
| <span data-ttu-id="3e47f-111">D3DDECLUSAGE \_ 位置</span><span class="sxs-lookup"><span data-stu-id="3e47f-111">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="3e47f-112">1</span><span class="sxs-lookup"><span data-stu-id="3e47f-112">1</span></span>                      | <span data-ttu-id="3e47f-113">D3DVSDE \_ POSITION2</span><span class="sxs-lookup"><span data-stu-id="3e47f-113">D3DVSDE\_POSITION2</span></span>    |
| <span data-ttu-id="3e47f-114">D3DDECLUSAGE \_ 正常</span><span class="sxs-lookup"><span data-stu-id="3e47f-114">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="3e47f-115">0</span><span class="sxs-lookup"><span data-stu-id="3e47f-115">0</span></span>                      | <span data-ttu-id="3e47f-116">D3DVSDE \_ 正常</span><span class="sxs-lookup"><span data-stu-id="3e47f-116">D3DVSDE\_NORMAL</span></span>       |
| <span data-ttu-id="3e47f-117">D3DDECLUSAGE \_ 正常</span><span class="sxs-lookup"><span data-stu-id="3e47f-117">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="3e47f-118">1</span><span class="sxs-lookup"><span data-stu-id="3e47f-118">1</span></span>                      | <span data-ttu-id="3e47f-119">D3DVSDE \_ NORMAL2</span><span class="sxs-lookup"><span data-stu-id="3e47f-119">D3DVSDE\_NORMAL2</span></span>      |
| <span data-ttu-id="3e47f-120">D3DDECLUSAGE \_ BLENDWEIGHT</span><span class="sxs-lookup"><span data-stu-id="3e47f-120">D3DDECLUSAGE\_BLENDWEIGHT</span></span>  | <span data-ttu-id="3e47f-121">0</span><span class="sxs-lookup"><span data-stu-id="3e47f-121">0</span></span>                      | <span data-ttu-id="3e47f-122">D3DVSDE \_ BLENDWEIGHT</span><span class="sxs-lookup"><span data-stu-id="3e47f-122">D3DVSDE\_BLENDWEIGHT</span></span>  |
| <span data-ttu-id="3e47f-123">D3DDECLUSAGE \_ BLENDINDICES</span><span class="sxs-lookup"><span data-stu-id="3e47f-123">D3DDECLUSAGE\_BLENDINDICES</span></span> | <span data-ttu-id="3e47f-124">0</span><span class="sxs-lookup"><span data-stu-id="3e47f-124">0</span></span>                      | <span data-ttu-id="3e47f-125">D3DVSDE \_ BLENDINDICES</span><span class="sxs-lookup"><span data-stu-id="3e47f-125">D3DVSDE\_BLENDINDICES</span></span> |
| <span data-ttu-id="3e47f-126">D3DDECLUSAGE \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="3e47f-126">D3DDECLUSAGE\_PSIZE</span></span>        | <span data-ttu-id="3e47f-127">0</span><span class="sxs-lookup"><span data-stu-id="3e47f-127">0</span></span>                      | <span data-ttu-id="3e47f-128">D3DVSDE \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="3e47f-128">D3DVSDE\_PSIZE</span></span>        |
| <span data-ttu-id="3e47f-129">D3DDECLUSAGE \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="3e47f-129">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="3e47f-130">0</span><span class="sxs-lookup"><span data-stu-id="3e47f-130">0</span></span>                      | <span data-ttu-id="3e47f-131">D3DVSDE \_ 擴散</span><span class="sxs-lookup"><span data-stu-id="3e47f-131">D3DVSDE\_DIFFUSE</span></span>      |
| <span data-ttu-id="3e47f-132">D3DDECLUSAGE \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="3e47f-132">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="3e47f-133">1</span><span class="sxs-lookup"><span data-stu-id="3e47f-133">1</span></span>                      | <span data-ttu-id="3e47f-134">D3DVSDE \_ 反光</span><span class="sxs-lookup"><span data-stu-id="3e47f-134">D3DVSDE\_SPECULAR</span></span>     |
| <span data-ttu-id="3e47f-135">D3DDECLUSAGE \_ TEXCOORD</span><span class="sxs-lookup"><span data-stu-id="3e47f-135">D3DDECLUSAGE\_TEXCOORD</span></span>     | <span data-ttu-id="3e47f-136">n</span><span class="sxs-lookup"><span data-stu-id="3e47f-136">n</span></span>                      | <span data-ttu-id="3e47f-137">D3DVSDE \_ TEXCOORDn</span><span class="sxs-lookup"><span data-stu-id="3e47f-137">D3DVSDE\_TEXCOORDn</span></span>    |



 

<span data-ttu-id="3e47f-138">當搭配 Direct3D 7 驅動程式上的硬體頂點處理使用宣告時，Direct3D runtime 會將它轉換為具有下列規則的 FVF：</span><span class="sxs-lookup"><span data-stu-id="3e47f-138">When a declaration is used with hardware vertex processing on a Direct3D 7 driver, the Direct3D runtime converts it to a FVF with the following rules:</span></span>

-   <span data-ttu-id="3e47f-139"> (從 MaxStreams cap) 看出，只應使用串流0。</span><span class="sxs-lookup"><span data-stu-id="3e47f-139">Only stream 0 should be used (evident from the MaxStreams cap).</span></span>
-   <span data-ttu-id="3e47f-140">頂點元素的順序應該與 FVF 位的順序相同。</span><span class="sxs-lookup"><span data-stu-id="3e47f-140">The order of vertex elements should be the same as order of FVF bits.</span></span>
-   <span data-ttu-id="3e47f-141">不允許材質座標中的間隙。</span><span class="sxs-lookup"><span data-stu-id="3e47f-141">Gaps in texture coordinates are not allowed.</span></span>
-   <span data-ttu-id="3e47f-142">未描述資料表的任何頂點元素都無法轉換成所有預先 DirectX 8 驅動程式的有效 FVF，因此無法用於這些驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3e47f-142">Any vertex element not described the table cannot be converted into a valid FVF for all pre-DirectX 8 drivers and, hence, cannot be used on those drivers.</span></span>
-   <span data-ttu-id="3e47f-143">\_ \_ 如果裝置未設定 D3DPTEXTURECAPS \_ 投射或 D3DPTEXTURECAPS 立方體貼圖 caps，則只有 D3DDECLTYPE FLOAT2 可供具有 D3DDECLUSAGE TEXCOORD 的頂點元素使用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="3e47f-143">Only D3DDECLTYPE\_FLOAT2 is allowed for vertex elements with D3DDECLUSAGE\_TEXCOORD if device does not set either of the D3DPTEXTURECAPS\_PROJECTED or D3DPTEXTURECAPS\_CUBEMAP caps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e47f-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e47f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e47f-145">頂點宣告</span><span class="sxs-lookup"><span data-stu-id="3e47f-145">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 



