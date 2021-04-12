---
description: 此資料表會將 D3DVERTEXELEMENT9 宣告的成員對應至 FVF 碼。
ms.assetid: be4357b5-5b92-44ca-9100-ec9473930446
title: 'Direct3D 宣告與 FVF 碼之間的對應 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4831af7b8c03ae4abd5ac2847351d2a6c921fb97
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109153"
---
# <a name="mapping-between-a-direct3d-declaration-and-fvf-codes-direct3d-9"></a><span data-ttu-id="4738e-103">Direct3D 宣告與 FVF 碼之間的對應 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="4738e-103">Mapping between a Direct3D Declaration and FVF Codes (Direct3D 9)</span></span>

<span data-ttu-id="4738e-104">此資料表會將 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) 宣告的成員對應至 FVF 碼。</span><span class="sxs-lookup"><span data-stu-id="4738e-104">This table maps members of a [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) declaration to a FVF code.</span></span>



| <span data-ttu-id="4738e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="4738e-105">Data type</span></span>             | <span data-ttu-id="4738e-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="4738e-106">Usage</span></span>                      | <span data-ttu-id="4738e-107">使用方式索引</span><span class="sxs-lookup"><span data-stu-id="4738e-107">Usage index</span></span> | <span data-ttu-id="4738e-108">FVF</span><span class="sxs-lookup"><span data-stu-id="4738e-108">FVF</span></span>                       |
|-----------------------|----------------------------|-------------|---------------------------|
| <span data-ttu-id="4738e-109">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="4738e-109">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="4738e-110">D3DDECLUSAGE \_ 位置</span><span class="sxs-lookup"><span data-stu-id="4738e-110">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="4738e-111">0</span><span class="sxs-lookup"><span data-stu-id="4738e-111">0</span></span>           | <span data-ttu-id="4738e-112">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="4738e-112">D3DFVF\_XYZ</span></span>               |
| <span data-ttu-id="4738e-113">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="4738e-113">D3DDECLTYPE\_FLOAT4</span></span>   | <span data-ttu-id="4738e-114">D3DDECLUSAGE \_ POSITIONT</span><span class="sxs-lookup"><span data-stu-id="4738e-114">D3DDECLUSAGE\_POSITIONT</span></span>    | <span data-ttu-id="4738e-115">0</span><span class="sxs-lookup"><span data-stu-id="4738e-115">0</span></span>           | <span data-ttu-id="4738e-116">D3DFVF \_ XYZRHW</span><span class="sxs-lookup"><span data-stu-id="4738e-116">D3DFVF\_XYZRHW</span></span>            |
| <span data-ttu-id="4738e-117">D3DDECLTYPE \_ FLOATn</span><span class="sxs-lookup"><span data-stu-id="4738e-117">D3DDECLTYPE\_FLOATn</span></span>   | <span data-ttu-id="4738e-118">D3DDECLUSAGE \_ BLENDWEIGHT</span><span class="sxs-lookup"><span data-stu-id="4738e-118">D3DDECLUSAGE\_BLENDWEIGHT</span></span>  | <span data-ttu-id="4738e-119">0</span><span class="sxs-lookup"><span data-stu-id="4738e-119">0</span></span>           | <span data-ttu-id="4738e-120">D3DFVF \_ XYZBn</span><span class="sxs-lookup"><span data-stu-id="4738e-120">D3DFVF\_XYZBn</span></span>             |
| <span data-ttu-id="4738e-121">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="4738e-121">D3DDECLTYPE\_UBYTE4</span></span>   | <span data-ttu-id="4738e-122">D3DDECLUSAGE \_ BLENDINDICES</span><span class="sxs-lookup"><span data-stu-id="4738e-122">D3DDECLUSAGE\_BLENDINDICES</span></span> | <span data-ttu-id="4738e-123">0</span><span class="sxs-lookup"><span data-stu-id="4738e-123">0</span></span>           | <span data-ttu-id="4738e-124">D3DFVF \_ XYZB (nWeights + 1) </span><span class="sxs-lookup"><span data-stu-id="4738e-124">D3DFVF\_XYZB (nWeights+1)</span></span> |
| <span data-ttu-id="4738e-125">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="4738e-125">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="4738e-126">D3DDECLUSAGE \_ 正常</span><span class="sxs-lookup"><span data-stu-id="4738e-126">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="4738e-127">0</span><span class="sxs-lookup"><span data-stu-id="4738e-127">0</span></span>           | <span data-ttu-id="4738e-128">D3DFVF \_ 正常</span><span class="sxs-lookup"><span data-stu-id="4738e-128">D3DFVF\_NORMAL</span></span>            |
| <span data-ttu-id="4738e-129">D3DDECLTYPE \_ FLOAT1</span><span class="sxs-lookup"><span data-stu-id="4738e-129">D3DDECLTYPE\_FLOAT1</span></span>   | <span data-ttu-id="4738e-130">D3DDECLUSAGE \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="4738e-130">D3DDECLUSAGE\_PSIZE</span></span>        | <span data-ttu-id="4738e-131">0</span><span class="sxs-lookup"><span data-stu-id="4738e-131">0</span></span>           | <span data-ttu-id="4738e-132">D3DFVF \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="4738e-132">D3DFVF\_PSIZE</span></span>             |
| <span data-ttu-id="4738e-133">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="4738e-133">D3DDECLTYPE\_D3DCOLOR</span></span> | <span data-ttu-id="4738e-134">D3DDECLUSAGE \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="4738e-134">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="4738e-135">0</span><span class="sxs-lookup"><span data-stu-id="4738e-135">0</span></span>           | <span data-ttu-id="4738e-136">D3DFVF \_ 擴散</span><span class="sxs-lookup"><span data-stu-id="4738e-136">D3DFVF\_DIFFUSE</span></span>           |
| <span data-ttu-id="4738e-137">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="4738e-137">D3DDECLTYPE\_D3DCOLOR</span></span> | <span data-ttu-id="4738e-138">D3DDECLUSAGE \_ 色彩</span><span class="sxs-lookup"><span data-stu-id="4738e-138">D3DDECLUSAGE\_COLOR</span></span>        | <span data-ttu-id="4738e-139">1</span><span class="sxs-lookup"><span data-stu-id="4738e-139">1</span></span>           | <span data-ttu-id="4738e-140">D3DFVF \_ 反光</span><span class="sxs-lookup"><span data-stu-id="4738e-140">D3DFVF\_SPECULAR</span></span>          |
| <span data-ttu-id="4738e-141">D3DDECLTYPE \_ FLOATm</span><span class="sxs-lookup"><span data-stu-id="4738e-141">D3DDECLTYPE\_FLOATm</span></span>   | <span data-ttu-id="4738e-142">D3DDECLUSAGE \_ TEXCOORD</span><span class="sxs-lookup"><span data-stu-id="4738e-142">D3DDECLUSAGE\_TEXCOORD</span></span>     | <span data-ttu-id="4738e-143">n</span><span class="sxs-lookup"><span data-stu-id="4738e-143">n</span></span>           | <span data-ttu-id="4738e-144">D3DFVF \_ TEXCOORDSIZEm (n) </span><span class="sxs-lookup"><span data-stu-id="4738e-144">D3DFVF\_TEXCOORDSIZEm(n)</span></span>  |
| <span data-ttu-id="4738e-145">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="4738e-145">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="4738e-146">D3DDECLUSAGE \_ 位置</span><span class="sxs-lookup"><span data-stu-id="4738e-146">D3DDECLUSAGE\_POSITION</span></span>     | <span data-ttu-id="4738e-147">1</span><span class="sxs-lookup"><span data-stu-id="4738e-147">1</span></span>           | <span data-ttu-id="4738e-148">N/A</span><span class="sxs-lookup"><span data-stu-id="4738e-148">N/A</span></span>                       |
| <span data-ttu-id="4738e-149">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="4738e-149">D3DDECLTYPE\_FLOAT3</span></span>   | <span data-ttu-id="4738e-150">D3DDECLUSAGE \_ 正常</span><span class="sxs-lookup"><span data-stu-id="4738e-150">D3DDECLUSAGE\_NORMAL</span></span>       | <span data-ttu-id="4738e-151">1</span><span class="sxs-lookup"><span data-stu-id="4738e-151">1</span></span>           | <span data-ttu-id="4738e-152">N/A</span><span class="sxs-lookup"><span data-stu-id="4738e-152">N/A</span></span>                       |



 

## <a name="related-topics"></a><span data-ttu-id="4738e-153">相關主題</span><span class="sxs-lookup"><span data-stu-id="4738e-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4738e-154">頂點宣告</span><span class="sxs-lookup"><span data-stu-id="4738e-154">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 



