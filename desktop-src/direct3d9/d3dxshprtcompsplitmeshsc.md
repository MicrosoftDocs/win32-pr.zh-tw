---
description: D3DXSHPRTCompSplitMeshSC 函式-搭配預先計算 radiance 傳輸 (PRT) 模擬器的頂點版本壓縮結果使用。
ms.assetid: 10d81920-2a1b-42fa-aabe-7d6b504f4d36
title: 'D3DXSHPRTCompSplitMeshSC 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSplitMeshSC
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e51a86ec9b12992d49364d3a7c614751dacafac3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093896"
---
# <a name="d3dxshprtcompsplitmeshsc-function"></a><span data-ttu-id="009be-103">D3DXSHPRTCompSplitMeshSC 函式</span><span class="sxs-lookup"><span data-stu-id="009be-103">D3DXSHPRTCompSplitMeshSC function</span></span>

<span data-ttu-id="009be-104">搭配預先計算 radiance transfer 的頂點版本壓縮結果使用 (PRT) 模擬器。</span><span class="sxs-lookup"><span data-stu-id="009be-104">Used with compressed results of the vertex version of the precomputed radiance transfer (PRT) simulator.</span></span> <span data-ttu-id="009be-105">呼叫 [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) 之後，可以使用此函式將網格分割成每個超級叢集的臉部/頂點群組。</span><span class="sxs-lookup"><span data-stu-id="009be-105">After [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md) has been called, this function can be used to split the mesh into a group of faces/vertices per super cluster.</span></span> <span data-ttu-id="009be-106">每個超級叢集都包含所有包含分類于其中一個叢集中之頂點的臉部。</span><span class="sxs-lookup"><span data-stu-id="009be-106">Each super cluster contains all of the faces that contain any vertex classified in one of its clusters.</span></span> <span data-ttu-id="009be-107">連接到這組臉部的所有頂點也會包含在傳回的陣列 ppVertStatus 中，指出頂點是否屬於超級叢集。</span><span class="sxs-lookup"><span data-stu-id="009be-107">All of the vertices connected to this set of faces are also included with the returned array ppVertStatus indicating whether or not the vertex belongs to the super cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="009be-108">語法</span><span class="sxs-lookup"><span data-stu-id="009be-108">Syntax</span></span>


```C++
HRESULT D3DXSHPRTCompSplitMeshSC(
  _In_    UINT                          *pClusterIDs,
  _In_    UINT                          NumVertices,
  _In_    UINT                          NumCs,
  _In_    UINT                          *pSClusterIDs,
  _In_    UINT                          NumSCs,
  _In_    LPVOID                        pInputIB,
  _In_    BOOL                          InputIBIs32Bit,
  _In_    UINT                          NumFaces,
  _Inout_ LPD3DXBUFFER                  *ppIBData,
  _Inout_ UINT                          *pIBDataLength,
  _Inout_ BOOL                          OutputIBIs32Bit,
  _Inout_ LPD3DXBUFFER                  *ppFaceRemap,
  _Inout_ LPD3DXBUFFER                  *ppVertData,
  _Inout_ UINT                          *pVertDataLength,
  _Inout_ UINT                          *pSCClusterList,
  _Inout_ D3DXSHPRTSPLITMESHCLUSTERDATA *pSCData
);
```



## <a name="parameters"></a><span data-ttu-id="009be-109">參數</span><span class="sxs-lookup"><span data-stu-id="009be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="009be-110">*pClusterIDs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="009be-110">*pClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="009be-111">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="009be-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="009be-112">*NumVertices* 叢集識別碼 (從壓縮的緩衝區解壓縮。 ) </span><span class="sxs-lookup"><span data-stu-id="009be-112">*NumVertices* cluster IDs (extracted from a compressed buffer.)</span></span>

</dd> <dt>

<span data-ttu-id="009be-113">*NumVertices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="009be-113">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="009be-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="009be-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="009be-115">原始網格中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="009be-115">Number of vertices in original mesh.</span></span>

</dd> <dt>

<span data-ttu-id="009be-116">*NumCs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="009be-116">*NumCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="009be-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="009be-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="009be-118"> (輸入參數壓縮的叢集數目。 ) </span><span class="sxs-lookup"><span data-stu-id="009be-118">Number of clusters (input parameter to compression.)</span></span>

</dd> <dt>

<span data-ttu-id="009be-119">*pSClusterIDs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="009be-119">*pSClusterIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="009be-120">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="009be-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="009be-121">將包含超級叢集識別碼的大小 *NumCs* 陣列。</span><span class="sxs-lookup"><span data-stu-id="009be-121">Array of size *NumCs* that will contain super cluster IDs.</span></span>

</dd> <dt>

<span data-ttu-id="009be-122">*NumSCs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="009be-122">*NumSCs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="009be-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="009be-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="009be-124">配置在 [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md)中的超級叢集數目。</span><span class="sxs-lookup"><span data-stu-id="009be-124">Number of super clusters allocated in [**D3DXSHPRTCompSuperCluster**](d3dxshprtcompsupercluster.md).</span></span>

</dd> <dt>

<span data-ttu-id="009be-125">*pInputIB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="009be-125">*pInputIB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="009be-126">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="009be-126">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="009be-127">網格的原始索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="009be-127">Raw index buffer for mesh.</span></span> <span data-ttu-id="009be-128">格式取決於 *InputIBIs32Bit*。</span><span class="sxs-lookup"><span data-stu-id="009be-128">The format depends on *InputIBIs32Bit*.</span></span>

</dd> <dt>

<span data-ttu-id="009be-129">*InputIBIs32Bit* \[在\]</span><span class="sxs-lookup"><span data-stu-id="009be-129">*InputIBIs32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="009be-130">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="009be-130">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="009be-131">若 **為 TRUE**，則索引緩衝區設定為32位;否則為16位。</span><span class="sxs-lookup"><span data-stu-id="009be-131">If **TRUE**, the index buffer is set to 32 bit; otherwise, 16 bit.</span></span>

</dd> <dt>

<span data-ttu-id="009be-132">*NumFaces* \[在\]</span><span class="sxs-lookup"><span data-stu-id="009be-132">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="009be-133">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="009be-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="009be-134">原始網格 (*pInputIB* 的臉部數目是此長度的3倍。 ) </span><span class="sxs-lookup"><span data-stu-id="009be-134">Number of faces in the original mesh (*pInputIB* is 3 times this length.)</span></span>

</dd> <dt>

<span data-ttu-id="009be-135">*ppIBData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="009be-135">*ppIBData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="009be-136">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="009be-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="009be-137">將包含所產生之分割臉部的原始索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="009be-137">Raw index buffer that will contain the resulting split faces.</span></span> <span data-ttu-id="009be-138">由 *InputIBIs32Bit* 決定的格式。</span><span class="sxs-lookup"><span data-stu-id="009be-138">Format determined by *InputIBIs32Bit*.</span></span> <span data-ttu-id="009be-139">由函數配置。</span><span class="sxs-lookup"><span data-stu-id="009be-139">Allocated by function.</span></span>

</dd> <dt>

<span data-ttu-id="009be-140">*pIBDataLength* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="009be-140">*pIBDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="009be-141">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="009be-141">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="009be-142">在函數中指派的 *ppIBData* 長度。</span><span class="sxs-lookup"><span data-stu-id="009be-142">Length of *ppIBData*, assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="009be-143">*OutputIBIs32Bit* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="009be-143">*OutputIBIs32Bit* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="009be-144">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="009be-144">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="009be-145">若 **為 TRUE**，則配置不帶正負號的整數陣列;否則，會配置不帶正負號的簡短陣列。</span><span class="sxs-lookup"><span data-stu-id="009be-145">If **TRUE**, allocates an unsigned integer array; otherwise, allocates an unsigned short array.</span></span>

</dd> <dt>

<span data-ttu-id="009be-146">*ppFaceRemap* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="009be-146">*ppFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="009be-147">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="009be-147">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="009be-148">將 *ppIBData* 中的每個臉部對應至原始臉部。</span><span class="sxs-lookup"><span data-stu-id="009be-148">Mapping of each face in *ppIBData* to original faces.</span></span> <span data-ttu-id="009be-149">長度為 \* *pIBDataLength*/3。</span><span class="sxs-lookup"><span data-stu-id="009be-149">Length is \**pIBDataLength*/3.</span></span>

</dd> <dt>

<span data-ttu-id="009be-150">*ppVertData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="009be-150">*ppVertData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="009be-151">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="009be-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="009be-152">新的頂點資料結構。</span><span class="sxs-lookup"><span data-stu-id="009be-152">New vertex data structure.</span></span> <span data-ttu-id="009be-153">*PVertDataLength* 的大小。</span><span class="sxs-lookup"><span data-stu-id="009be-153">Size of *pVertDataLength*.</span></span>

</dd> <dt>

<span data-ttu-id="009be-154">*pVertDataLength* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="009be-154">*pVertDataLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="009be-155">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="009be-155">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="009be-156">分割網格中的新頂點數目。</span><span class="sxs-lookup"><span data-stu-id="009be-156">Number of new vertices in split mesh.</span></span> <span data-ttu-id="009be-157">在函數中指派。</span><span class="sxs-lookup"><span data-stu-id="009be-157">Assigned in function.</span></span>

</dd> <dt>

<span data-ttu-id="009be-158">*pSCClusterList* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="009be-158">*pSCClusterList* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="009be-159">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="009be-159">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="009be-160">長度 *NumCs* 的陣列，可針對每個 supercluster *pSCData* (*pClusterIDs* \*) 欄位中的索引，其中包含依 supercluster 排序的群集。</span><span class="sxs-lookup"><span data-stu-id="009be-160">Array of length *NumCs* which *pSCData* indexes into (*pClusterIDs*\* fields) for each supercluster, contains clusters sorted by supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="009be-161">*pSCData* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="009be-161">*pSCData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="009be-162">類型： **[ **D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span><span class="sxs-lookup"><span data-stu-id="009be-162">Type: **[**D3DXSHPRTSPLITMESHCLUSTERDATA**](d3dxshprtsplitmeshclusterdata.md)\***</span></span>

<span data-ttu-id="009be-163">每個超級叢集的結構。</span><span class="sxs-lookup"><span data-stu-id="009be-163">Structure per super cluster.</span></span> <span data-ttu-id="009be-164">包含 *ppIBData*、 *pSCClusterList* 和 *ppVertData* 的索引。</span><span class="sxs-lookup"><span data-stu-id="009be-164">Contains indices into *ppIBData*, *pSCClusterList*, and *ppVertData*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="009be-165">傳回值</span><span class="sxs-lookup"><span data-stu-id="009be-165">Return value</span></span>

<span data-ttu-id="009be-166">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="009be-166">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="009be-167">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="009be-167">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="009be-168">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="009be-168">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="009be-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="009be-169">Requirements</span></span>



| <span data-ttu-id="009be-170">需求</span><span class="sxs-lookup"><span data-stu-id="009be-170">Requirement</span></span> | <span data-ttu-id="009be-171">值</span><span class="sxs-lookup"><span data-stu-id="009be-171">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="009be-172">標頭</span><span class="sxs-lookup"><span data-stu-id="009be-172">Header</span></span><br/>  | <dl> <span data-ttu-id="009be-173"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="009be-173"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="009be-174">程式庫</span><span class="sxs-lookup"><span data-stu-id="009be-174">Library</span></span><br/> | <dl> <span data-ttu-id="009be-175"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="009be-175"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="009be-176">另請參閱</span><span class="sxs-lookup"><span data-stu-id="009be-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="009be-177">預先計算 Radiance 傳送函式</span><span class="sxs-lookup"><span data-stu-id="009be-177">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
