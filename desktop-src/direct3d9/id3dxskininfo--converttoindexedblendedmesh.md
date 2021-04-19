---
description: 使用網格，並傳回具有個別頂點 blend 加權、索引和骨骼組合表的新網格。 表格描述哪些骨骼調色板會影響網格的哪些子集。
ms.assetid: e4758a3b-8a45-4ed3-aa62-9713d12afc56
title: 'ID3DXSkinInfo：： ConvertToIndexedBlendedMesh 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToIndexedBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87c8a4b943a647e52d7260f1ff53b32b40756761
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000616"
---
# <a name="id3dxskininfoconverttoindexedblendedmesh-method"></a><span data-ttu-id="0952a-104">ID3DXSkinInfo：： ConvertToIndexedBlendedMesh 方法</span><span class="sxs-lookup"><span data-stu-id="0952a-104">ID3DXSkinInfo::ConvertToIndexedBlendedMesh method</span></span>

<span data-ttu-id="0952a-105">使用網格，並傳回具有個別頂點 blend 加權、索引和骨骼組合表的新網格。</span><span class="sxs-lookup"><span data-stu-id="0952a-105">Takes a mesh and returns a new mesh with per-vertex blend weights, indices, and a bone combination table.</span></span> <span data-ttu-id="0952a-106">表格描述哪些骨骼調色板會影響網格的哪些子集。</span><span class="sxs-lookup"><span data-stu-id="0952a-106">The table describes which bone palettes affect which subsets of the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="0952a-107">語法</span><span class="sxs-lookup"><span data-stu-id="0952a-107">Syntax</span></span>


```C++
HRESULT ConvertToIndexedBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
  [in]        DWORD        paletteSize,
  [in]  const DWORD        *pAdjacencyIn,
  [in]        LPDWORD      pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap,
  [out]       DWORD        *pMaxVertexInfl,
  [out]       DWORD        *pNumBoneCombinations,
  [out]       LPD3DXBUFFER *ppBoneCombinationTable,
  [out]       LPD3DXMESH   *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="0952a-108">參數</span><span class="sxs-lookup"><span data-stu-id="0952a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0952a-109">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0952a-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0952a-110">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="0952a-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="0952a-111">輸入網格。</span><span class="sxs-lookup"><span data-stu-id="0952a-111">The input mesh.</span></span> <span data-ttu-id="0952a-112">請參閱 [**ID3DXMesh**](id3dxmesh.md)。</span><span class="sxs-lookup"><span data-stu-id="0952a-112">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="0952a-113">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0952a-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0952a-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0952a-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0952a-115">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="0952a-115">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="0952a-116">*paletteSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0952a-116">*paletteSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0952a-117">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0952a-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0952a-118">適用于矩陣調色板外觀的骨骼矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="0952a-118">Number of bone matrices available for matrix palette skinning.</span></span>

</dd> <dt>

<span data-ttu-id="0952a-119">*pAdjacencyIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0952a-119">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0952a-120">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="0952a-120">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0952a-121">輸入網格相鄰資訊。</span><span class="sxs-lookup"><span data-stu-id="0952a-121">Input mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="0952a-122">*pAdjacencyOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0952a-122">*pAdjacencyOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0952a-123">類型： **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0952a-123">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0952a-124">輸出網格相鄰資訊。</span><span class="sxs-lookup"><span data-stu-id="0952a-124">Output mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="0952a-125">*pFaceRemap* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0952a-125">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0952a-126">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0952a-126">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0952a-127">Dword 的陣列，每個臉部各一個，用來識別對應至混合網格中各臉部的原始網格臉部。</span><span class="sxs-lookup"><span data-stu-id="0952a-127">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the blended mesh.</span></span> <span data-ttu-id="0952a-128">如果提供給此引數的值為 **Null**，則不會傳回臉部重新對應資料。</span><span class="sxs-lookup"><span data-stu-id="0952a-128">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="0952a-129">*ppVertexRemap* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0952a-129">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0952a-130">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0952a-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0952a-131">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址，其中包含每個頂點的 DWORD，以指定新頂點如何對應至舊頂點。</span><span class="sxs-lookup"><span data-stu-id="0952a-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="0952a-132">如果您需要根據新的頂點對應來改變外部資料，這個重新對應會很有用。</span><span class="sxs-lookup"><span data-stu-id="0952a-132">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="0952a-133">這個參數是選擇性的;可以使用 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="0952a-133">This parameter is optional; **NULL** may be used.</span></span>

</dd> <dt>

<span data-ttu-id="0952a-134">*pMaxVertexInfl* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0952a-134">*pMaxVertexInfl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0952a-135">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0952a-135">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0952a-136">DWORD 的指標，其中將包含此外觀方法的每個頂點所需的最大骨骼數目。</span><span class="sxs-lookup"><span data-stu-id="0952a-136">Pointer to a DWORD that will contain the maximum number of bone influences required per vertex for this skinning method.</span></span>

</dd> <dt>

<span data-ttu-id="0952a-137">*pNumBoneCombinations* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0952a-137">*pNumBoneCombinations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0952a-138">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0952a-138">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0952a-139">骨骼組合表中的骨骼數目指標。</span><span class="sxs-lookup"><span data-stu-id="0952a-139">Pointer to the number of bones in the bone combination table.</span></span>

</dd> <dt>

<span data-ttu-id="0952a-140">*ppBoneCombinationTable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0952a-140">*ppBoneCombinationTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0952a-141">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0952a-141">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0952a-142">骨骼組合表的指標。</span><span class="sxs-lookup"><span data-stu-id="0952a-142">Pointer to the bone combination table.</span></span> <span data-ttu-id="0952a-143">資料會組織成 [**D3DXBONECOMBINATION**](d3dxbonecombination.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="0952a-143">The data is organized in a [**D3DXBONECOMBINATION**](d3dxbonecombination.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0952a-144">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0952a-144">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0952a-145">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="0952a-145">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="0952a-146">新網格的指標。</span><span class="sxs-lookup"><span data-stu-id="0952a-146">Pointer to the new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0952a-147">傳回值</span><span class="sxs-lookup"><span data-stu-id="0952a-147">Return value</span></span>

<span data-ttu-id="0952a-148">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0952a-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0952a-149">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="0952a-149">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0952a-150">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="0952a-150">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0952a-151">備註</span><span class="sxs-lookup"><span data-stu-id="0952a-151">Remarks</span></span>

<span data-ttu-id="0952a-152">重新對應陣列中的每個專案都會指定該位置的前一個索引。</span><span class="sxs-lookup"><span data-stu-id="0952a-152">Each element in the remap arrays specifies the previous index for that position.</span></span> <span data-ttu-id="0952a-153">例如，如果頂點位於位置3，但已重新對應到位置5，則 pVertexRemap 的第五個元素將包含3個。</span><span class="sxs-lookup"><span data-stu-id="0952a-153">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap will contain 3.</span></span>

<span data-ttu-id="0952a-154">這個方法不會在不支援固定函式頂點混合的硬體上執行。</span><span class="sxs-lookup"><span data-stu-id="0952a-154">This method does not run on hardware that does not support fixed-function vertex blending.</span></span>

## <a name="requirements"></a><span data-ttu-id="0952a-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="0952a-155">Requirements</span></span>



| <span data-ttu-id="0952a-156">需求</span><span class="sxs-lookup"><span data-stu-id="0952a-156">Requirement</span></span> | <span data-ttu-id="0952a-157">值</span><span class="sxs-lookup"><span data-stu-id="0952a-157">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0952a-158">標頭</span><span class="sxs-lookup"><span data-stu-id="0952a-158">Header</span></span><br/>  | <dl> <span data-ttu-id="0952a-159"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="0952a-159"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0952a-160">程式庫</span><span class="sxs-lookup"><span data-stu-id="0952a-160">Library</span></span><br/> | <dl> <span data-ttu-id="0952a-161"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0952a-161"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0952a-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0952a-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0952a-163">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="0952a-163">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
