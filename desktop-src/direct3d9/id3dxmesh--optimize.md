---
description: ID3DXMesh：： Optimize 方法-產生具有重新排列臉部和頂點的新網格，以將繪製效能優化。
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: 'ID3DXMesh：： Optimize 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: debec1c0ee54e612ab0de832dbc5c2481dcefad8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093306"
---
# <a name="id3dxmeshoptimize-method"></a><span data-ttu-id="2b999-103">ID3DXMesh：： Optimize 方法</span><span class="sxs-lookup"><span data-stu-id="2b999-103">ID3DXMesh::Optimize method</span></span>

<span data-ttu-id="2b999-104">產生具有重新排序臉部和頂點的新網格，以將繪製效能優化。</span><span class="sxs-lookup"><span data-stu-id="2b999-104">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b999-105">語法</span><span class="sxs-lookup"><span data-stu-id="2b999-105">Syntax</span></span>


```C++
HRESULT Optimize(
  [in]            DWORD        Flags,
  [in]      const DWORD        *pAdjacencyIn,
  [in, out]       DWORD        *pAdjacencyOut,
  [in, out]       DWORD        *pFaceRemap,
  [out]           LPD3DXBUFFER *ppVertexRemap,
  [out]           LPD3DXMESH   *ppOptMesh
);
```



## <a name="parameters"></a><span data-ttu-id="2b999-106">參數</span><span class="sxs-lookup"><span data-stu-id="2b999-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b999-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="2b999-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b999-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b999-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b999-109">指定要執行的優化類型。</span><span class="sxs-lookup"><span data-stu-id="2b999-109">Specifies the type of optimization to perform.</span></span> <span data-ttu-id="2b999-110">這個參數可以設定為 [**D3DXMESHOPT**](./d3dxmeshopt.md) 和 [**D3DXMESH**](./d3dxmesh.md) (的一或多個旗標的組合，除了 D3DXMESH \_ 32 位、D3DXMESH \_ IB \_ WRITEONLY 和 D3DXMESH \_ WRITEONLY) 之外。</span><span class="sxs-lookup"><span data-stu-id="2b999-110">This parameter can be set to a combination of one or more flags from [**D3DXMESHOPT**](./d3dxmeshopt.md) and [**D3DXMESH**](./d3dxmesh.md) (except D3DXMESH\_32BIT, D3DXMESH\_IB\_WRITEONLY, and D3DXMESH\_WRITEONLY).</span></span>

</dd> <dt>

<span data-ttu-id="2b999-111">*pAdjacencyIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b999-111">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b999-112">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b999-112">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2b999-113">指標，指向每個臉部的三個 Dword 陣列，其會為來源網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="2b999-113">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="2b999-114">如果邊緣沒有連續的臉部，則值為0xffffffff。</span><span class="sxs-lookup"><span data-stu-id="2b999-114">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="2b999-115">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="2b999-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2b999-116">*pAdjacencyOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2b999-116">*pAdjacencyOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b999-117">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b999-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2b999-118">指標，指向每個臉部的三個 Dword 陣列，以指定優化網格中每個臉部的三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="2b999-118">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="2b999-119">如果邊緣沒有連續的臉部，則值為0xffffffff。</span><span class="sxs-lookup"><span data-stu-id="2b999-119">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="2b999-120">*pFaceRemap* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2b999-120">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b999-121">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b999-121">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="2b999-122">Dword 的陣列，每個臉部各一個，用來識別對應至優化網格中各臉部的原始網格臉部。</span><span class="sxs-lookup"><span data-stu-id="2b999-122">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="2b999-123">如果提供給此引數的值為 **Null**，則不會傳回臉部重新對應資料。</span><span class="sxs-lookup"><span data-stu-id="2b999-123">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="2b999-124">*ppVertexRemap* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2b999-124">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b999-125">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b999-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="2b999-126">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址，其中包含每個頂點的 DWORD，以指定新頂點如何對應至舊頂點。</span><span class="sxs-lookup"><span data-stu-id="2b999-126">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="2b999-127">如果您需要根據新的頂點對應來改變外部資料，這個重新對應會很有用。</span><span class="sxs-lookup"><span data-stu-id="2b999-127">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> <dt>

<span data-ttu-id="2b999-128">*ppOptMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2b999-128">*ppOptMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b999-129">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b999-129">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="2b999-130">[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示優化的網格。</span><span class="sxs-lookup"><span data-stu-id="2b999-130">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the optimized mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b999-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b999-131">Return value</span></span>

<span data-ttu-id="2b999-132">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b999-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b999-133">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2b999-133">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2b999-134">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="2b999-134">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b999-135">備註</span><span class="sxs-lookup"><span data-stu-id="2b999-135">Remarks</span></span>

<span data-ttu-id="2b999-136">這個方法會產生新的網格。</span><span class="sxs-lookup"><span data-stu-id="2b999-136">This method generates a new mesh.</span></span> <span data-ttu-id="2b999-137">執行 Optimize 之前，應用程式必須藉由呼叫 [**ID3DXBaseMesh：： GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)來產生連續的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2b999-137">Before running Optimize, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span></span> <span data-ttu-id="2b999-138">鄰接緩衝區包含連續的資料，例如邊緣清單和彼此連續的臉部。</span><span class="sxs-lookup"><span data-stu-id="2b999-138">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

<span data-ttu-id="2b999-139">這個方法與 [**ID3DXBaseMesh：： CloneMesh**](id3dxbasemesh--clonemesh.md) 方法非常類似，不同之處在于它可以在產生新的網格複製時執行優化。</span><span class="sxs-lookup"><span data-stu-id="2b999-139">This method is very similar to the [**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) method, except that it can perform optimization while generating the new clone of the mesh.</span></span> <span data-ttu-id="2b999-140">輸出網格會繼承輸入網格的所有建立參數。</span><span class="sxs-lookup"><span data-stu-id="2b999-140">The output mesh inherits all of the creation parameters of the input mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b999-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b999-141">Requirements</span></span>



| <span data-ttu-id="2b999-142">需求</span><span class="sxs-lookup"><span data-stu-id="2b999-142">Requirement</span></span> | <span data-ttu-id="2b999-143">值</span><span class="sxs-lookup"><span data-stu-id="2b999-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b999-144">標頭</span><span class="sxs-lookup"><span data-stu-id="2b999-144">Header</span></span><br/>  | <dl> <span data-ttu-id="2b999-145"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b999-145"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2b999-146">程式庫</span><span class="sxs-lookup"><span data-stu-id="2b999-146">Library</span></span><br/> | <dl> <span data-ttu-id="2b999-147"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b999-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2b999-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b999-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b999-149">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="2b999-149">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="2b999-150">**ID3DXMesh::OptimizeInplace**</span><span class="sxs-lookup"><span data-stu-id="2b999-150">**ID3DXMesh::OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
