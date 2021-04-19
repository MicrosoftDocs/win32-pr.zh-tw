---
description: 使用網格，並傳回具有個別頂點 blend 加權和骨骼組合表的新網格。 此表描述哪些骨骼會影響網格的哪些子集。
ms.assetid: c26a9e84-5731-4394-a047-5f1ffe7688d9
title: 'ID3DXSkinInfo：： ConvertToBlendedMesh 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 051c51291416dd7e190c83433a9bf84baeb92957
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986125"
---
# <a name="id3dxskininfoconverttoblendedmesh-method"></a><span data-ttu-id="7ebcd-104">ID3DXSkinInfo：： ConvertToBlendedMesh 方法</span><span class="sxs-lookup"><span data-stu-id="7ebcd-104">ID3DXSkinInfo::ConvertToBlendedMesh method</span></span>

<span data-ttu-id="7ebcd-105">使用網格，並傳回具有個別頂點 blend 加權和骨骼組合表的新網格。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-105">Takes a mesh and returns a new mesh with per-vertex blend weights and a bone combination table.</span></span> <span data-ttu-id="7ebcd-106">此表描述哪些骨骼會影響網格的哪些子集。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-106">The table describes which bones affect which subsets of the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ebcd-107">語法</span><span class="sxs-lookup"><span data-stu-id="7ebcd-107">Syntax</span></span>


```C++
HRESULT ConvertToBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
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



## <a name="parameters"></a><span data-ttu-id="7ebcd-108">參數</span><span class="sxs-lookup"><span data-stu-id="7ebcd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ebcd-109">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ebcd-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebcd-110">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="7ebcd-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="7ebcd-111">輸入網格。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-111">Input mesh.</span></span> <span data-ttu-id="7ebcd-112">請參閱 [**ID3DXMesh**](id3dxmesh.md)。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-112">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ebcd-113">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ebcd-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebcd-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ebcd-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ebcd-115">目前未使用。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-115">Currently unused.</span></span>

</dd> <dt>

<span data-ttu-id="7ebcd-116">*pAdjacencyIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ebcd-116">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebcd-117">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="7ebcd-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7ebcd-118">輸入網格相鄰資訊。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-118">Input mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="7ebcd-119">*pAdjacencyOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7ebcd-119">*pAdjacencyOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebcd-120">類型： **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ebcd-120">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ebcd-121">輸出網格相鄰資訊。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-121">Output mesh adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="7ebcd-122">*pFaceRemap* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7ebcd-122">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebcd-123">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ebcd-123">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7ebcd-124">Dword 的陣列，每個臉部各一個，用來識別對應至混合網格中各臉部的原始網格臉部。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-124">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the blended mesh.</span></span> <span data-ttu-id="7ebcd-125">如果提供給此引數的值為 **Null**，則不會傳回臉部重新對應資料。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-125">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="7ebcd-126">*ppVertexRemap* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7ebcd-126">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebcd-127">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ebcd-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7ebcd-128">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址，其中包含每個頂點的 DWORD，以指定新頂點如何對應至舊頂點。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-128">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="7ebcd-129">如果您需要根據新的頂點對應來改變外部資料，這個重新對應會很有用。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-129">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="7ebcd-130">這個參數是選擇性的;可以使用 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-130">This parameter is optional; **NULL** may be used.</span></span>

</dd> <dt>

<span data-ttu-id="7ebcd-131">*pMaxVertexInfl* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7ebcd-131">*pMaxVertexInfl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebcd-132">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ebcd-132">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7ebcd-133">DWORD 的指標，其中將包含此外觀方法的每個頂點所需的最大骨骼數目。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-133">Pointer to a DWORD that will contain the maximum number of bone influences required per vertex for this skinning method.</span></span>

</dd> <dt>

<span data-ttu-id="7ebcd-134">*pNumBoneCombinations* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7ebcd-134">*pNumBoneCombinations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebcd-135">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ebcd-135">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7ebcd-136">骨骼組合表中的骨骼數目指標。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-136">Pointer to the number of bones in the bone combination table.</span></span>

</dd> <dt>

<span data-ttu-id="7ebcd-137">*ppBoneCombinationTable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7ebcd-137">*ppBoneCombinationTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebcd-138">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ebcd-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7ebcd-139">骨骼組合表的指標。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-139">Pointer to the bone combination table.</span></span> <span data-ttu-id="7ebcd-140">資料會組織成 [**D3DXBONECOMBINATION**](d3dxbonecombination.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-140">The data is organized in a [**D3DXBONECOMBINATION**](d3dxbonecombination.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="7ebcd-141">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7ebcd-141">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ebcd-142">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ebcd-142">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="7ebcd-143">新網格的指標。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-143">Pointer to the new mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ebcd-144">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ebcd-144">Return value</span></span>

<span data-ttu-id="7ebcd-145">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ebcd-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ebcd-146">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-146">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7ebcd-147">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-147">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ebcd-148">備註</span><span class="sxs-lookup"><span data-stu-id="7ebcd-148">Remarks</span></span>

<span data-ttu-id="7ebcd-149">重新對應陣列中的每個專案都會指定該位置的前一個索引。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-149">Each element in the remap array specifies the previous index for that position.</span></span> <span data-ttu-id="7ebcd-150">例如，如果頂點位於位置3，但已重新對應到位置5，則 pVertexRemap 的第五個元素將包含3個。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-150">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap will contain 3.</span></span>

<span data-ttu-id="7ebcd-151">這個方法不會在不支援固定函式頂點混合的硬體上執行。</span><span class="sxs-lookup"><span data-stu-id="7ebcd-151">This method does not run on hardware that does not support fixed-function vertex blending.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ebcd-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ebcd-152">Requirements</span></span>



| <span data-ttu-id="7ebcd-153">需求</span><span class="sxs-lookup"><span data-stu-id="7ebcd-153">Requirement</span></span> | <span data-ttu-id="7ebcd-154">值</span><span class="sxs-lookup"><span data-stu-id="7ebcd-154">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ebcd-155">標頭</span><span class="sxs-lookup"><span data-stu-id="7ebcd-155">Header</span></span><br/>  | <dl> <span data-ttu-id="7ebcd-156"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ebcd-156"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7ebcd-157">程式庫</span><span class="sxs-lookup"><span data-stu-id="7ebcd-157">Library</span></span><br/> | <dl> <span data-ttu-id="7ebcd-158"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ebcd-158"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7ebcd-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ebcd-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ebcd-160">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="7ebcd-160">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
