---
description: D3DXUVAtlasPartition 函式-建立網格的 UV 塔。
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: 'D3DXUVAtlasPartition 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPartition
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 63df6bbcc1b811b9617796bc6e7e51af2dfdca56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117796"
---
# <a name="d3dxuvatlaspartition-function"></a><span data-ttu-id="6f43b-103">D3DXUVAtlasPartition 函式</span><span class="sxs-lookup"><span data-stu-id="6f43b-103">D3DXUVAtlasPartition function</span></span>

<span data-ttu-id="6f43b-104">建立網格的 UV 塔。</span><span class="sxs-lookup"><span data-stu-id="6f43b-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f43b-105">語法</span><span class="sxs-lookup"><span data-stu-id="6f43b-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasPartition(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContent,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    pFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
              LPD3DXBUFFER    *ppPartitionResultAdjacency,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a><span data-ttu-id="6f43b-106">參數</span><span class="sxs-lookup"><span data-stu-id="6f43b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f43b-107">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f43b-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f43b-108">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="6f43b-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="6f43b-109">輸入網格 (的指標，請參閱 [**ID3DXMesh**](id3dxmesh.md)) ，其中包含用來計算塔的物件幾何。</span><span class="sxs-lookup"><span data-stu-id="6f43b-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) that contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="6f43b-110">網格至少必須包含位置資料和2D 材質座標。</span><span class="sxs-lookup"><span data-stu-id="6f43b-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="6f43b-111">*dwMaxChartNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f43b-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f43b-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f43b-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f43b-113">要分割網格的圖表數目上限。</span><span class="sxs-lookup"><span data-stu-id="6f43b-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="6f43b-114">請參閱有關資料分割模式的備註。</span><span class="sxs-lookup"><span data-stu-id="6f43b-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="6f43b-115">使用0可告訴 D3DX，應該根據 stretch 將塔參數化。</span><span class="sxs-lookup"><span data-stu-id="6f43b-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="6f43b-116">*fMaxStretch* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f43b-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f43b-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f43b-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f43b-118">允許的延展量。</span><span class="sxs-lookup"><span data-stu-id="6f43b-118">The amount of stretching allowed.</span></span> <span data-ttu-id="6f43b-119">0表示不允許延展，1表示可以使用任何數量的延展。</span><span class="sxs-lookup"><span data-stu-id="6f43b-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="6f43b-120">*dwTextureIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f43b-120">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f43b-121">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f43b-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f43b-122">以零為基礎的材質座標索引，識別要使用的材質座標集。</span><span class="sxs-lookup"><span data-stu-id="6f43b-122">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="6f43b-123">*pdwAdjacency* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f43b-123">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f43b-124">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6f43b-124">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6f43b-125">相鄰資料陣列的指標，每個臉部有3個 Dword，指出哪些三角形彼此相鄰 (請參閱 [**ID3DXBaseMesh：： GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)) 。</span><span class="sxs-lookup"><span data-stu-id="6f43b-125">A pointer to an array of adjacency data with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6f43b-126">*pdwFalseEdges*</span><span class="sxs-lookup"><span data-stu-id="6f43b-126">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="6f43b-127">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6f43b-127">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6f43b-128">每個臉部有3個 DWORD 的陣列。</span><span class="sxs-lookup"><span data-stu-id="6f43b-128">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="6f43b-129">每個臉部都會指出邊緣是否為 false。</span><span class="sxs-lookup"><span data-stu-id="6f43b-129">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="6f43b-130">非 false 的邊緣會以-1 表示，錯誤的邊緣會以任何其他值表示。</span><span class="sxs-lookup"><span data-stu-id="6f43b-130">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="6f43b-131">這會啟用四邊形網格的參數化，其中每個四條中間的邊緣將不會被剪下。</span><span class="sxs-lookup"><span data-stu-id="6f43b-131">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="6f43b-132">*pfIMTArray* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f43b-132">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f43b-133">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f43b-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6f43b-134">整合式計量張量陣列的指標，描述如何延展三角形 (查看 [IntegratedMetricTensor](using-uvatlas.md)) 。</span><span class="sxs-lookup"><span data-stu-id="6f43b-134">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6f43b-135">*pCallback* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f43b-135">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f43b-136">類型： **[LPD3DXU加值稅LASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="6f43b-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="6f43b-137">回呼函式的指標 (查看適用于監視進度的 [LPD3DXU加值稅LASCB](lpd3dxuvatlascb.md)) 。</span><span class="sxs-lookup"><span data-stu-id="6f43b-137">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="6f43b-138">*fCallbackFrequency* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f43b-138">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f43b-139">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f43b-139">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f43b-140">指定 D3DX 將呼叫回呼的頻率;合理的預設值是 0.0001 f。</span><span class="sxs-lookup"><span data-stu-id="6f43b-140">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="6f43b-141">*pUserContent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f43b-141">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f43b-142">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f43b-142">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f43b-143">傳遞給回呼函式的使用者定義值指標。通常由應用程式用來傳遞資料結構的指標，以提供回呼函數的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="6f43b-143">Pointer to a user-defined value that is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="6f43b-144">*>dwoptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f43b-144">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f43b-145">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f43b-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f43b-146">藉由結合一或多個 [**D3DXU加值稅LAS**](./d3dxuvatlas.md) 旗標來指定所產生的圖表品質。</span><span class="sxs-lookup"><span data-stu-id="6f43b-146">Specify the quality of the charts generated by combining one or more [**D3DXUVATLAS**](./d3dxuvatlas.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="6f43b-147">*ppMeshOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6f43b-147">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f43b-148">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f43b-148">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="6f43b-149">使用塔 (的已建立網格指標，請參閱 [**ID3DXMesh**](id3dxmesh.md)) 。</span><span class="sxs-lookup"><span data-stu-id="6f43b-149">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6f43b-150">*pFacePartitioning* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6f43b-150">*pFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f43b-151">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="6f43b-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="6f43b-152">最終臉部資料分割資料的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="6f43b-152">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="6f43b-153">每個元素都包含每個臉部一個 DWORD (請參閱 [**ID3DXBuffer**](id3dxbuffer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="6f43b-153">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6f43b-154">*ppVertexRemapArray* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6f43b-154">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f43b-155">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f43b-155">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6f43b-156">重新對應頂點陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="6f43b-156">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="6f43b-157">每個陣列元素都會識別原始頂點，也就是當頂點在重新對應) 期間分割時，每個最終頂點的來源 (。</span><span class="sxs-lookup"><span data-stu-id="6f43b-157">Each array element identifies the original vertex each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="6f43b-158">每個陣列元素都包含每個頂點一個 DWORD。</span><span class="sxs-lookup"><span data-stu-id="6f43b-158">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="6f43b-159">*ppPartitionResultAdjacency*</span><span class="sxs-lookup"><span data-stu-id="6f43b-159">*ppPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="6f43b-160">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f43b-160">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6f43b-161">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="6f43b-161">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="6f43b-162">此緩衝區將包含每個臉部的三個 Dword 陣列，以針對輸出網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="6f43b-162">This buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="6f43b-163">這個參數不能是 **Null**，因為後續呼叫 D3DXUVAtlasPack () 需要它。</span><span class="sxs-lookup"><span data-stu-id="6f43b-163">This parameter must not be **NULL**, because the subsequent call to D3DXUVAtlasPack() requires it.</span></span>

</dd> <dt>

<span data-ttu-id="6f43b-164">*pfMaxStretchOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6f43b-164">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f43b-165">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f43b-165">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6f43b-166">由塔演算法產生的最大延展值指標。</span><span class="sxs-lookup"><span data-stu-id="6f43b-166">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="6f43b-167">範圍介於0.0 到1.0 之間。</span><span class="sxs-lookup"><span data-stu-id="6f43b-167">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="6f43b-168">*pdwNumChartsOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6f43b-168">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f43b-169">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f43b-169">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6f43b-170">塔演算法所建立的圖表數目指標。</span><span class="sxs-lookup"><span data-stu-id="6f43b-170">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="6f43b-171">如果 dwMaxChartNumber 太低，此參數將會傳回建立塔所需的最小圖表數目。</span><span class="sxs-lookup"><span data-stu-id="6f43b-171">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f43b-172">傳回值</span><span class="sxs-lookup"><span data-stu-id="6f43b-172">Return value</span></span>

<span data-ttu-id="6f43b-173">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6f43b-173">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6f43b-174">如果函式成功，則傳回值為「D3D 正常」， \_ 否則值為 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="6f43b-174">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f43b-175">備註</span><span class="sxs-lookup"><span data-stu-id="6f43b-175">Remarks</span></span>

<span data-ttu-id="6f43b-176">D3DXUVAtlasPartition 與 [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md)類似，不同之處在于 D3DXUVAtlasPartition 不會執行最終的封裝步驟。</span><span class="sxs-lookup"><span data-stu-id="6f43b-176">D3DXUVAtlasPartition is similar to [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), except that D3DXUVAtlasPartition does not performing the final packing step.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f43b-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f43b-177">Requirements</span></span>



| <span data-ttu-id="6f43b-178">需求</span><span class="sxs-lookup"><span data-stu-id="6f43b-178">Requirement</span></span> | <span data-ttu-id="6f43b-179">值</span><span class="sxs-lookup"><span data-stu-id="6f43b-179">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f43b-180">標頭</span><span class="sxs-lookup"><span data-stu-id="6f43b-180">Header</span></span><br/>  | <dl> <span data-ttu-id="6f43b-181"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="6f43b-181"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6f43b-182">程式庫</span><span class="sxs-lookup"><span data-stu-id="6f43b-182">Library</span></span><br/> | <dl> <span data-ttu-id="6f43b-183"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f43b-183"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6f43b-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f43b-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f43b-185">UVAtlas 函式</span><span class="sxs-lookup"><span data-stu-id="6f43b-185">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="6f43b-186">[UV Command-Line 工具 (uvatlas.exe) ](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="6f43b-186">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
