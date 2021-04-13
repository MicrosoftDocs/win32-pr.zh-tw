---
description: 結構，其中包含 patch 網狀架構的屬性。
ms.assetid: aaea69c9-2d33-46e8-bc26-95daf65abf50
title: 'D3DXPATCHINFO 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPATCHINFO
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 8628cc27a0223580aa1f8072750f4c31a176533e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322635"
---
# <a name="d3dxpatchinfo-structure"></a><span data-ttu-id="da467-103">D3DXPATCHINFO 結構</span><span class="sxs-lookup"><span data-stu-id="da467-103">D3DXPATCHINFO structure</span></span>

<span data-ttu-id="da467-104">結構，其中包含 patch 網狀架構的屬性。</span><span class="sxs-lookup"><span data-stu-id="da467-104">Structure that contains the attributes of a patch mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="da467-105">語法</span><span class="sxs-lookup"><span data-stu-id="da467-105">Syntax</span></span>


```C++
typedef struct D3DXPATCHINFO {
  D3DXPATCHMESHTYPE PatchType;
  D3DDEGREETYPE     Degree;
  D3DBASISTYPE      Basis;
} D3DXPATCHINFO, *LPD3DXPATCHINFO;
```



## <a name="members"></a><span data-ttu-id="da467-106">成員</span><span class="sxs-lookup"><span data-stu-id="da467-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="da467-107">**PatchType**</span><span class="sxs-lookup"><span data-stu-id="da467-107">**PatchType**</span></span>
</dt> <dd>

<span data-ttu-id="da467-108">類型： **[ **D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**</span><span class="sxs-lookup"><span data-stu-id="da467-108">Type: **[**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="da467-109">修補類型。</span><span class="sxs-lookup"><span data-stu-id="da467-109">The patch type.</span></span> <span data-ttu-id="da467-110">如需修補程式類型的詳細資訊，請參閱 [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md)。</span><span class="sxs-lookup"><span data-stu-id="da467-110">For information about patch types, see [**D3DXPATCHMESHTYPE**](./d3dxpatchmeshtype.md).</span></span>

</dd> <dt>

<span data-ttu-id="da467-111">**角度**</span><span class="sxs-lookup"><span data-stu-id="da467-111">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="da467-112">類型： **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="da467-112">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="da467-113">用來建立修補程式的曲線程度。</span><span class="sxs-lookup"><span data-stu-id="da467-113">Degree of the curves used to construct the patch.</span></span> <span data-ttu-id="da467-114">如需所支援之度數的詳細資訊，請參閱 [**D3DDEGREETYPE**](./d3ddegreetype.md)。</span><span class="sxs-lookup"><span data-stu-id="da467-114">For information about the degrees supported, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="da467-115">**Basis**</span><span class="sxs-lookup"><span data-stu-id="da467-115">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="da467-116">類型： **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="da467-116">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="da467-117">用來建立修補程式的曲線類型。</span><span class="sxs-lookup"><span data-stu-id="da467-117">Type of curve used to construct the patch.</span></span> <span data-ttu-id="da467-118">如需支援之基礎類型的詳細資訊，請參閱 [**D3DBASISTYPE**](./d3dbasistype.md)。</span><span class="sxs-lookup"><span data-stu-id="da467-118">For information about the basis types supported, see [**D3DBASISTYPE**](./d3dbasistype.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da467-119">備註</span><span class="sxs-lookup"><span data-stu-id="da467-119">Remarks</span></span>

<span data-ttu-id="da467-120">網格是一組臉部，每個臉部都由一個簡單的多邊形描述。</span><span class="sxs-lookup"><span data-stu-id="da467-120">A mesh is a set of faces, each of which is described by a simple polygon.</span></span> <span data-ttu-id="da467-121">您可以將數個網格連接在一起來建立物件。</span><span class="sxs-lookup"><span data-stu-id="da467-121">Objects can be created by connecting several meshes together.</span></span> <span data-ttu-id="da467-122">修補程式網格是由修補程式所構成。</span><span class="sxs-lookup"><span data-stu-id="da467-122">A patch mesh is constructed from patches.</span></span> <span data-ttu-id="da467-123">Patch 是從曲線構成的四側幾何。</span><span class="sxs-lookup"><span data-stu-id="da467-123">A patch is a four-sided piece of geometry constructed from curves.</span></span> <span data-ttu-id="da467-124">使用的曲線類型和曲線的順序可能會不同，因此 patch 介面幾乎可以容納任何介面圖形。</span><span class="sxs-lookup"><span data-stu-id="da467-124">The type of curve used and the order of the curve can be varied so that the patch surface will fit almost any surface shape.</span></span>

<span data-ttu-id="da467-125">支援下列類型的 patch 組合：</span><span class="sxs-lookup"><span data-stu-id="da467-125">The following types of patch combinations are supported:</span></span>



| <span data-ttu-id="da467-126">修補類型</span><span class="sxs-lookup"><span data-stu-id="da467-126">Patch Type</span></span> | <span data-ttu-id="da467-127">基礎</span><span class="sxs-lookup"><span data-stu-id="da467-127">Basis</span></span>       | <span data-ttu-id="da467-128">角度</span><span class="sxs-lookup"><span data-stu-id="da467-128">Degree</span></span> |
|------------|-------------|--------|
| <span data-ttu-id="da467-129">矩形</span><span class="sxs-lookup"><span data-stu-id="da467-129">Rectangle</span></span>  | <span data-ttu-id="da467-130">貝茲</span><span class="sxs-lookup"><span data-stu-id="da467-130">Bezier</span></span>      | <span data-ttu-id="da467-131">2，3，5</span><span class="sxs-lookup"><span data-stu-id="da467-131">2,3,5</span></span>  |
| <span data-ttu-id="da467-132">矩形</span><span class="sxs-lookup"><span data-stu-id="da467-132">Rectangle</span></span>  | <span data-ttu-id="da467-133">B-曲線</span><span class="sxs-lookup"><span data-stu-id="da467-133">B-Spline</span></span>    | <span data-ttu-id="da467-134">2，3，5</span><span class="sxs-lookup"><span data-stu-id="da467-134">2,3,5</span></span>  |
| <span data-ttu-id="da467-135">矩形</span><span class="sxs-lookup"><span data-stu-id="da467-135">Rectangle</span></span>  | <span data-ttu-id="da467-136">Catmull-Rom</span><span class="sxs-lookup"><span data-stu-id="da467-136">Catmull-Rom</span></span> | <span data-ttu-id="da467-137">3</span><span class="sxs-lookup"><span data-stu-id="da467-137">3</span></span>      |
| <span data-ttu-id="da467-138">Triangle</span><span class="sxs-lookup"><span data-stu-id="da467-138">Triangle</span></span>   | <span data-ttu-id="da467-139">貝茲</span><span class="sxs-lookup"><span data-stu-id="da467-139">Bezier</span></span>      | <span data-ttu-id="da467-140">2，3，5</span><span class="sxs-lookup"><span data-stu-id="da467-140">2,3,5</span></span>  |
| <span data-ttu-id="da467-141">N-修補程式</span><span class="sxs-lookup"><span data-stu-id="da467-141">N-patch</span></span>    | <span data-ttu-id="da467-142">N/A</span><span class="sxs-lookup"><span data-stu-id="da467-142">N/A</span></span>         | <span data-ttu-id="da467-143">3</span><span class="sxs-lookup"><span data-stu-id="da467-143">3</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="da467-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="da467-144">Requirements</span></span>



| <span data-ttu-id="da467-145">需求</span><span class="sxs-lookup"><span data-stu-id="da467-145">Requirement</span></span> | <span data-ttu-id="da467-146">值</span><span class="sxs-lookup"><span data-stu-id="da467-146">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da467-147">標頭</span><span class="sxs-lookup"><span data-stu-id="da467-147">Header</span></span><br/> | <dl> <span data-ttu-id="da467-148"><dt>D3dx9mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="da467-148"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da467-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da467-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da467-150">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="da467-150">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="da467-151">**D3DRECTPATCH \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="da467-151">**D3DRECTPATCH\_INFO**</span></span>](d3drectpatch-info.md)
</dt> <dt>

[<span data-ttu-id="da467-152">**D3DTRIPATCH \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="da467-152">**D3DTRIPATCH\_INFO**</span></span>](d3dtripatch-info.md)
</dt> <dt>

[<span data-ttu-id="da467-153">**D3DXCreatePatchMesh**</span><span class="sxs-lookup"><span data-stu-id="da467-153">**D3DXCreatePatchMesh**</span></span>](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
