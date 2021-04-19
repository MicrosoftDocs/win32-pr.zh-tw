---
description: 建立網格的 UV 塔。
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: 'D3DXUVAtlasCreate 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasCreate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 814f213b0195b0922270d0548d8b5fd4c48fb3e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997380"
---
# <a name="d3dxuvatlascreate-function"></a><span data-ttu-id="99b64-103">D3DXUVAtlasCreate 函式</span><span class="sxs-lookup"><span data-stu-id="99b64-103">D3DXUVAtlasCreate function</span></span>

<span data-ttu-id="99b64-104">建立網格的 UV 塔。</span><span class="sxs-lookup"><span data-stu-id="99b64-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="99b64-105">語法</span><span class="sxs-lookup"><span data-stu-id="99b64-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasCreate(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        UINT            dwWidth,
  _In_        UINT            dwHeight,
  _In_        FLOAT           fGutter,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContext,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    *ppFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a><span data-ttu-id="99b64-106">參數</span><span class="sxs-lookup"><span data-stu-id="99b64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b64-107">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b64-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-108">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="99b64-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="99b64-109">輸入網格 (的指標，請參閱 [**ID3DXMesh**](id3dxmesh.md)) ，其中包含用來計算塔的物件幾何。</span><span class="sxs-lookup"><span data-stu-id="99b64-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="99b64-110">網格至少必須包含位置資料和2D 材質座標。</span><span class="sxs-lookup"><span data-stu-id="99b64-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="99b64-111">*dwMaxChartNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b64-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99b64-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99b64-113">要分割網格的圖表數目上限。</span><span class="sxs-lookup"><span data-stu-id="99b64-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="99b64-114">請參閱有關資料分割模式的備註。</span><span class="sxs-lookup"><span data-stu-id="99b64-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="99b64-115">使用0可告訴 D3DX，應該根據 stretch 將塔參數化。</span><span class="sxs-lookup"><span data-stu-id="99b64-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="99b64-116">*fMaxStretch* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b64-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99b64-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99b64-118">允許的延展量。</span><span class="sxs-lookup"><span data-stu-id="99b64-118">The amount of stretching allowed.</span></span> <span data-ttu-id="99b64-119">0表示不允許延展，1表示可以使用任何數量的延展。</span><span class="sxs-lookup"><span data-stu-id="99b64-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="99b64-120">*dwWidth* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b64-120">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-121">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99b64-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99b64-122">材質寬度。</span><span class="sxs-lookup"><span data-stu-id="99b64-122">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="99b64-123">*dwHeight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b64-123">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-124">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99b64-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99b64-125">材質高度。</span><span class="sxs-lookup"><span data-stu-id="99b64-125">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="99b64-126">*fGutter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b64-126">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-127">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99b64-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99b64-128">塔上兩個圖表之間的最小距離（以材質）。</span><span class="sxs-lookup"><span data-stu-id="99b64-128">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="99b64-129">裝訂邊一律會以寬度調整;因此，如果在512x512 材質上使用2.5 的裝訂邊，則兩個圖表之間的最小距離為 2.5/512.0 材質。</span><span class="sxs-lookup"><span data-stu-id="99b64-129">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="99b64-130">*dwTextureIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b64-130">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-131">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99b64-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99b64-132">以零為基礎的材質座標索引，識別要使用的材質座標集。</span><span class="sxs-lookup"><span data-stu-id="99b64-132">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="99b64-133">*pdwAdjacency* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b64-133">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-134">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="99b64-134">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="99b64-135">相鄰資料陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="99b64-135">A pointer to an array of adjacency data.</span></span> <span data-ttu-id="99b64-136">每個臉部有3個 Dword，指出哪些三角形彼此相鄰 (請參閱 [**ID3DXBaseMesh：： GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)) 。</span><span class="sxs-lookup"><span data-stu-id="99b64-136">with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="99b64-137">*pdwFalseEdges*</span><span class="sxs-lookup"><span data-stu-id="99b64-137">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="99b64-138">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="99b64-138">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="99b64-139">每個臉部有3個 DWORD 的陣列。</span><span class="sxs-lookup"><span data-stu-id="99b64-139">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="99b64-140">每個臉部都會指出邊緣是否為 false。</span><span class="sxs-lookup"><span data-stu-id="99b64-140">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="99b64-141">非 false 的邊緣會以-1 表示，錯誤的邊緣會以任何其他值表示。</span><span class="sxs-lookup"><span data-stu-id="99b64-141">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="99b64-142">這會啟用四邊形網格的參數化，其中每個四條中間的邊緣將不會被剪下。</span><span class="sxs-lookup"><span data-stu-id="99b64-142">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="99b64-143">*pfIMTArray* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b64-143">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-144">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="99b64-144">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="99b64-145">整合式計量張量陣列的指標，描述如何延展三角形 (查看 [IntegratedMetricTensor](using-uvatlas.md)) 。</span><span class="sxs-lookup"><span data-stu-id="99b64-145">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="99b64-146">*pCallback* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b64-146">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-147">類型： **[LPD3DXU加值稅LASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="99b64-147">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="99b64-148">回呼函式的指標 (查看適用于監視進度的 [LPD3DXU加值稅LASCB](lpd3dxuvatlascb.md)) 。</span><span class="sxs-lookup"><span data-stu-id="99b64-148">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="99b64-149">*fCallbackFrequency* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b64-149">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-150">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99b64-150">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99b64-151">指定 D3DX 將呼叫回呼的頻率;合理的預設值是 0.0001 f。</span><span class="sxs-lookup"><span data-stu-id="99b64-151">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="99b64-152">*pUserContent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b64-152">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-153">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99b64-153">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99b64-154">傳遞給回呼函式的使用者定義值指標。通常由應用程式用來傳遞資料結構的指標，以提供回呼函數的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="99b64-154">Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="99b64-155">*>dwoptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b64-155">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-156">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99b64-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99b64-157">指定產生的圖表品質。</span><span class="sxs-lookup"><span data-stu-id="99b64-157">Specify the quality of the charts generated.</span></span> <span data-ttu-id="99b64-158">請參閱 [**D3DXU加值稅LAS**](./d3dxuvatlas.md)。</span><span class="sxs-lookup"><span data-stu-id="99b64-158">See [**D3DXUVATLAS**](./d3dxuvatlas.md).</span></span>

</dd> <dt>

<span data-ttu-id="99b64-159">*ppMeshOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b64-159">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-160">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="99b64-160">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="99b64-161">使用塔 (的已建立網格指標，請參閱 [**ID3DXMesh**](id3dxmesh.md)) 。</span><span class="sxs-lookup"><span data-stu-id="99b64-161">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="99b64-162">*ppFacePartitioning* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="99b64-162">*ppFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-163">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="99b64-163">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="99b64-164">最終臉部資料分割資料的陣列指標。</span><span class="sxs-lookup"><span data-stu-id="99b64-164">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="99b64-165">每個元素都包含每個臉部一個 DWORD (請參閱 [**ID3DXBuffer**](id3dxbuffer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="99b64-165">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="99b64-166">*ppVertexRemapArray* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="99b64-166">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-167">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="99b64-167">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="99b64-168">重新對應頂點陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="99b64-168">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="99b64-169">每個陣列元素都會識別當頂點在重新對應) 期間分割時，每個最終頂點都來自 (的原始頂點。</span><span class="sxs-lookup"><span data-stu-id="99b64-169">Each array element identifies the original vertex that each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="99b64-170">每個陣列元素都包含每個頂點一個 DWORD。</span><span class="sxs-lookup"><span data-stu-id="99b64-170">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="99b64-171">*pfMaxStretchOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="99b64-171">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-172">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="99b64-172">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="99b64-173">由塔演算法產生的最大延展值指標。</span><span class="sxs-lookup"><span data-stu-id="99b64-173">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="99b64-174">範圍介於0.0 到1.0 之間。</span><span class="sxs-lookup"><span data-stu-id="99b64-174">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="99b64-175">*pdwNumChartsOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="99b64-175">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99b64-176">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="99b64-176">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="99b64-177">塔演算法所建立的圖表數目指標。</span><span class="sxs-lookup"><span data-stu-id="99b64-177">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="99b64-178">如果 dwMaxChartNumber 太低，此參數將會傳回建立塔所需的最小圖表數目。</span><span class="sxs-lookup"><span data-stu-id="99b64-178">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99b64-179">傳回值</span><span class="sxs-lookup"><span data-stu-id="99b64-179">Return value</span></span>

<span data-ttu-id="99b64-180">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99b64-180">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99b64-181">如果函式成功，則傳回值為「D3D 正常」， \_ 否則值為 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="99b64-181">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="99b64-182">備註</span><span class="sxs-lookup"><span data-stu-id="99b64-182">Remarks</span></span>

<span data-ttu-id="99b64-183">D3DXUVAtlasCreate 可以透過兩種方式分割網格幾何：</span><span class="sxs-lookup"><span data-stu-id="99b64-183">D3DXUVAtlasCreate can partition mesh geometry two ways:</span></span>

-   <span data-ttu-id="99b64-184">根據圖表數目</span><span class="sxs-lookup"><span data-stu-id="99b64-184">Based on the number of charts</span></span>
-   <span data-ttu-id="99b64-185">根據允許的最大延展。</span><span class="sxs-lookup"><span data-stu-id="99b64-185">Based on the maximum allowed stretch.</span></span> <span data-ttu-id="99b64-186">如果允許的最大延展值為0，則每個三角形可能會在自己的圖表中。</span><span class="sxs-lookup"><span data-stu-id="99b64-186">If the maximum allowed stretch is 0, each triangle will likely be in its own chart.</span></span>

## <a name="requirements"></a><span data-ttu-id="99b64-187">規格需求</span><span class="sxs-lookup"><span data-stu-id="99b64-187">Requirements</span></span>



| <span data-ttu-id="99b64-188">需求</span><span class="sxs-lookup"><span data-stu-id="99b64-188">Requirement</span></span> | <span data-ttu-id="99b64-189">值</span><span class="sxs-lookup"><span data-stu-id="99b64-189">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99b64-190">標頭</span><span class="sxs-lookup"><span data-stu-id="99b64-190">Header</span></span><br/>  | <dl> <span data-ttu-id="99b64-191"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="99b64-191"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="99b64-192">程式庫</span><span class="sxs-lookup"><span data-stu-id="99b64-192">Library</span></span><br/> | <dl> <span data-ttu-id="99b64-193"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="99b64-193"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="99b64-194">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99b64-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b64-195">UVAtlas 函式</span><span class="sxs-lookup"><span data-stu-id="99b64-195">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="99b64-196">[UV Command-Line 工具 (uvatlas.exe) ](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="99b64-196">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
