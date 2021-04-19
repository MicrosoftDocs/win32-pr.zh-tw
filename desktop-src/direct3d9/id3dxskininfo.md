---
description: 應用程式會使用 ID3DXSkinInfo 介面的方法來操作骨骼矩陣，這些矩陣會用來為動畫的外觀頂點資料。 這個介面不再與 ID3DXMesh 緊密系結，而且可以用來對任何一組頂點資料進行外觀。
ms.assetid: 4ccf88b0-2cc7-4e91-a0f2-fb8eea66a3ce
title: 'ID3DXSkinInfo 介面 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: afb93a0513bef7de1b0815b8b1f50179e2cba41d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993871"
---
# <a name="id3dxskininfo-interface"></a><span data-ttu-id="c1cbf-104">ID3DXSkinInfo 介面</span><span class="sxs-lookup"><span data-stu-id="c1cbf-104">ID3DXSkinInfo interface</span></span>

<span data-ttu-id="c1cbf-105">應用程式會使用 ID3DXSkinInfo 介面的方法來操作骨骼矩陣，這些矩陣會用來為動畫的外觀頂點資料。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-105">Applications use the methods of the ID3DXSkinInfo interface to manipulate bone matrices, which are used to skin vertex data for animation.</span></span> <span data-ttu-id="c1cbf-106">這個介面不再與 [**ID3DXMesh**](id3dxmesh.md) 緊密系結，而且可以用來對任何一組頂點資料進行外觀。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-106">This interface is no longer strictly tied to [**ID3DXMesh**](id3dxmesh.md) and can be used to skin any set of vertex data.</span></span>

## <a name="members"></a><span data-ttu-id="c1cbf-107">成員</span><span class="sxs-lookup"><span data-stu-id="c1cbf-107">Members</span></span>

<span data-ttu-id="c1cbf-108">**ID3DXSkinInfo** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-108">The **ID3DXSkinInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c1cbf-109">**ID3DXSkinInfo** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c1cbf-109">**ID3DXSkinInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="c1cbf-110">方法</span><span class="sxs-lookup"><span data-stu-id="c1cbf-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c1cbf-111">方法</span><span class="sxs-lookup"><span data-stu-id="c1cbf-111">Methods</span></span>

<span data-ttu-id="c1cbf-112">**ID3DXSkinInfo** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-112">The **ID3DXSkinInfo** interface has these methods.</span></span>



| <span data-ttu-id="c1cbf-113">方法</span><span class="sxs-lookup"><span data-stu-id="c1cbf-113">Method</span></span>                                                                              | <span data-ttu-id="c1cbf-114">描述</span><span class="sxs-lookup"><span data-stu-id="c1cbf-114">Description</span></span>                                                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1cbf-115">**克隆**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-115">**Clone**</span></span>](id3dxskininfo--clone.md)                                               | <span data-ttu-id="c1cbf-116">複製面板資訊物件。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-116">Clones a skin info object.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="c1cbf-117">**ConvertToBlendedMesh**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-117">**ConvertToBlendedMesh**</span></span>](id3dxskininfo--converttoblendedmesh.md)                 | <span data-ttu-id="c1cbf-118">使用網格，並傳回具有個別頂點 blend 加權和骨骼組合表的新網格。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-118">Takes a mesh and returns a new mesh with per-vertex blend weights and a bone combination table.</span></span> <span data-ttu-id="c1cbf-119">此表描述哪些骨骼會影響網格的哪些子集。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-119">The table describes which bones affect which subsets of the mesh.</span></span><br/>                   |
| [<span data-ttu-id="c1cbf-120">**ConvertToIndexedBlendedMesh**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-120">**ConvertToIndexedBlendedMesh**</span></span>](id3dxskininfo--converttoindexedblendedmesh.md)   | <span data-ttu-id="c1cbf-121">使用網格，並傳回具有個別頂點 blend 加權、索引和骨骼組合表的新網格。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-121">Takes a mesh and returns a new mesh with per-vertex blend weights, indices, and a bone combination table.</span></span> <span data-ttu-id="c1cbf-122">表格描述哪些骨骼調色板會影響網格的哪些子集。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-122">The table describes which bone palettes affect which subsets of the mesh.</span></span><br/> |
| [<span data-ttu-id="c1cbf-123">**FindBoneVertexInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-123">**FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md) | <span data-ttu-id="c1cbf-124">捕獲影響單一頂點之骨骼影響的索引。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-124">Retrieves the index of the bone influence affecting a single vertex.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="c1cbf-125">**GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-125">**GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)                         | <span data-ttu-id="c1cbf-126">取得骨骼影響的頂點和加權。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-126">Gets the vertices and weights that a bone influences.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="c1cbf-127">**GetBoneName**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-127">**GetBoneName**</span></span>](id3dxskininfo--getbonename.md)                                   | <span data-ttu-id="c1cbf-128">從骨骼索引取得骨骼名稱。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-128">Gets the bone name, from the bone index.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="c1cbf-129">**GetBoneOffsetMatrix**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-129">**GetBoneOffsetMatrix**</span></span>](id3dxskininfo--getboneoffsetmatrix.md)                   | <span data-ttu-id="c1cbf-130">取得骨骼位移矩陣。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-130">Gets the bone offset matrix.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="c1cbf-131">**GetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-131">**GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)             | <span data-ttu-id="c1cbf-132">抓取受指定之骨骼影響影響的 blend 因數和頂點。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-132">Retrieves the blend factor and vertex affected by a specified bone influence.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="c1cbf-133">**GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-133">**GetDeclaration**</span></span>](id3dxskininfo--getdeclaration.md)                             | <span data-ttu-id="c1cbf-134">取得頂點宣告。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-134">Gets the vertex declaration.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="c1cbf-135">**GetFVF**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-135">**GetFVF**</span></span>](id3dxskininfo--getfvf.md)                                             | <span data-ttu-id="c1cbf-136">取得固定的函式頂點值。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-136">Gets the fixed function vertex value.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="c1cbf-137">**GetMaxFaceInfluences**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-137">**GetMaxFaceInfluences**</span></span>](id3dxskininfo--getmaxfaceinfluences.md)                 | <span data-ttu-id="c1cbf-138">取得具有指定之索引緩衝區的三角形網格中最大臉部影響。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-138">Gets the maximum face influences in a triangle mesh with the specified index buffer.</span></span><br/>                                                                                                |
| [<span data-ttu-id="c1cbf-139">**GetMaxVertexInfluences**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-139">**GetMaxVertexInfluences**</span></span>](id3dxskininfo--getmaxvertexinfluences.md)             | <span data-ttu-id="c1cbf-140">取得網格中任何頂點的最大影響數目。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-140">Gets the maximum number of influences for any vertex in the mesh.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="c1cbf-141">**GetMinBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-141">**GetMinBoneInfluence**</span></span>](id3dxskininfo--getminboneinfluence.md)                   | <span data-ttu-id="c1cbf-142">取得最小的骨骼影響。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-142">Gets the minimum bone influence.</span></span> <span data-ttu-id="c1cbf-143">影響小於此值的值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-143">Influence values smaller than this are ignored.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="c1cbf-144">**GetNumBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-144">**GetNumBoneInfluences**</span></span>](id3dxskininfo--getnumboneinfluences.md)                 | <span data-ttu-id="c1cbf-145">取得骨骼的影響數目。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-145">Gets the number of influences for a bone.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="c1cbf-146">**GetNumBones**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-146">**GetNumBones**</span></span>](id3dxskininfo--getnumbones.md)                                   | <span data-ttu-id="c1cbf-147">取得骨骼數目。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-147">Gets the number of bones.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="c1cbf-148">**重新**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-148">**Remap**</span></span>](id3dxskininfo--remap.md)                                               | <span data-ttu-id="c1cbf-149">更新骨骼影響資訊，使其在重新排序之後符合頂點。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-149">Updates bone influence information to match vertices after they are reordered.</span></span> <span data-ttu-id="c1cbf-150">如果目標頂點緩衝區已從外部重新排序，則應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-150">This method should be called if the target vertex buffer has been reordered externally.</span></span><br/>              |
| [<span data-ttu-id="c1cbf-151">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-151">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)                         | <span data-ttu-id="c1cbf-152">設定骨骼的影響值。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-152">Sets the influence value for a bone.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="c1cbf-153">**SetBoneName**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-153">**SetBoneName**</span></span>](id3dxskininfo--setbonename.md)                                   | <span data-ttu-id="c1cbf-154">設定骨骼名稱。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-154">Sets the bone name.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="c1cbf-155">**SetBoneOffsetMatrix**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-155">**SetBoneOffsetMatrix**</span></span>](id3dxskininfo--setboneoffsetmatrix.md)                   | <span data-ttu-id="c1cbf-156">設定骨骼位移矩陣。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-156">Sets the bone offset matrix.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="c1cbf-157">**SetBoneVertexInfluence**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-157">**SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)             | <span data-ttu-id="c1cbf-158">將骨骼的影響值設定在單一頂點上。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-158">Sets an influence value of a bone on a single vertex.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="c1cbf-159">**SetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-159">**SetDeclaration**</span></span>](id3dxskininfo--setdeclaration.md)                             | <span data-ttu-id="c1cbf-160">設定頂點宣告。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-160">Sets the vertex declaration.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="c1cbf-161">**SetFVF**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-161">**SetFVF**</span></span>](id3dxskininfo--setfvf.md)                                             | <span data-ttu-id="c1cbf-162">設定 (FVF) 類型的彈性頂點格式。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-162">Sets the flexible vertex format (FVF) type.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="c1cbf-163">**SetMinBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-163">**SetMinBoneInfluence**</span></span>](id3dxskininfo--setminboneinfluence.md)                   | <span data-ttu-id="c1cbf-164">設定最小的骨骼影響。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-164">Sets the minimum bone influence.</span></span> <span data-ttu-id="c1cbf-165">影響小於此值的值會被忽略。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-165">Influence values smaller than this are ignored.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="c1cbf-166">**UpdateSkinnedMesh**</span><span class="sxs-lookup"><span data-stu-id="c1cbf-166">**UpdateSkinnedMesh**</span></span>](id3dxskininfo--updateskinnedmesh.md)                       | <span data-ttu-id="c1cbf-167">根據目前的矩陣，將軟體外觀套用至目標頂點。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-167">Applies software skinning to the target vertices based on the current matrices.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="c1cbf-168">備註</span><span class="sxs-lookup"><span data-stu-id="c1cbf-168">Remarks</span></span>

<span data-ttu-id="c1cbf-169">使用 [**D3DXCreateSkinInfo**](d3dxcreateskininfo.md)、 [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md)或 [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md)建立 **ID3DXSkinInfo** 介面。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-169">Create a **ID3DXSkinInfo** interface with [**D3DXCreateSkinInfo**](d3dxcreateskininfo.md), [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md), or [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md).</span></span>

<span data-ttu-id="c1cbf-170">LPD3DXSKININFO 型別定義為 **ID3DXSkinInfo** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c1cbf-170">The LPD3DXSKININFO type is defined as a pointer to the **ID3DXSkinInfo** interface.</span></span>


```
typedef struct ID3DXSkinInfo *LPD3DXSKININFO;
```



## <a name="requirements"></a><span data-ttu-id="c1cbf-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1cbf-171">Requirements</span></span>



| <span data-ttu-id="c1cbf-172">需求</span><span class="sxs-lookup"><span data-stu-id="c1cbf-172">Requirement</span></span> | <span data-ttu-id="c1cbf-173">值</span><span class="sxs-lookup"><span data-stu-id="c1cbf-173">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1cbf-174">標頭</span><span class="sxs-lookup"><span data-stu-id="c1cbf-174">Header</span></span><br/>  | <dl> <span data-ttu-id="c1cbf-175"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="c1cbf-175"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c1cbf-176">程式庫</span><span class="sxs-lookup"><span data-stu-id="c1cbf-176">Library</span></span><br/> | <dl> <span data-ttu-id="c1cbf-177"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1cbf-177"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c1cbf-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1cbf-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1cbf-179">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="c1cbf-179">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
