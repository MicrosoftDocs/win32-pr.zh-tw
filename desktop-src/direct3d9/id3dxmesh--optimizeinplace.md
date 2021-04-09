---
description: 產生具有重新排序臉部和頂點的網格，以將繪製效能優化。 這個方法會重新排序現有的網格。
ms.assetid: 2cdaf627-d1d3-44f0-a5ae-9023d4b0de45
title: 'ID3DXMesh：： OptimizeInplace 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.OptimizeInplace
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f889e0d3754cc1321ffa59eba294038b87991489
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696812"
---
# <a name="id3dxmeshoptimizeinplace-method"></a><span data-ttu-id="783b8-104">ID3DXMesh：： OptimizeInplace 方法</span><span class="sxs-lookup"><span data-stu-id="783b8-104">ID3DXMesh::OptimizeInplace method</span></span>

<span data-ttu-id="783b8-105">產生具有重新排序臉部和頂點的網格，以將繪製效能優化。</span><span class="sxs-lookup"><span data-stu-id="783b8-105">Generates a mesh with reordered faces and vertices to optimize drawing performance.</span></span> <span data-ttu-id="783b8-106">這個方法會重新排序現有的網格。</span><span class="sxs-lookup"><span data-stu-id="783b8-106">This method reorders the existing mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="783b8-107">語法</span><span class="sxs-lookup"><span data-stu-id="783b8-107">Syntax</span></span>


```C++
HRESULT OptimizeInplace(
  [in]        DWORD        Flags,
  [in]  const DWORD        *pAdjacencyIn,
  [out]       DWORD        *pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="783b8-108">參數</span><span class="sxs-lookup"><span data-stu-id="783b8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="783b8-109">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="783b8-109">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="783b8-110">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="783b8-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="783b8-111">一或多個 [**D3DXMESHOPT**](./d3dxmeshopt.md) 旗標的組合，指定要執行的優化類型。</span><span class="sxs-lookup"><span data-stu-id="783b8-111">Combination of one or more [**D3DXMESHOPT**](./d3dxmeshopt.md) flags, specifying the type of optimization to perform.</span></span>

</dd> <dt>

<span data-ttu-id="783b8-112">*pAdjacencyIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="783b8-112">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="783b8-113">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="783b8-113">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="783b8-114">指標，指向每個臉部的三個 Dword 陣列，其會為來源網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="783b8-114">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="783b8-115">如果邊緣沒有連續的臉部，則值為0xffffffff。</span><span class="sxs-lookup"><span data-stu-id="783b8-115">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="783b8-116">*pAdjacencyOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="783b8-116">*pAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="783b8-117">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="783b8-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="783b8-118">指標，指向每個臉部的三個 Dword 陣列，以指定優化網格中每個臉部的三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="783b8-118">Pointer to an array of three DWORDs per face that specifies the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="783b8-119">如果邊緣沒有連續的臉部，則值為0xffffffff。</span><span class="sxs-lookup"><span data-stu-id="783b8-119">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="783b8-120">如果提供給這個引數的值為 **Null**，則不會傳回相鄰資料。</span><span class="sxs-lookup"><span data-stu-id="783b8-120">If the value supplied for this argument is **NULL**, adjacency data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="783b8-121">*pFaceRemap* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="783b8-121">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="783b8-122">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="783b8-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="783b8-123">Dword 的陣列，每個臉部各一個，用來識別對應至優化網格中各臉部的原始網格臉部。</span><span class="sxs-lookup"><span data-stu-id="783b8-123">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the optimized mesh.</span></span> <span data-ttu-id="783b8-124">如果提供給此引數的值為 **Null**，則不會傳回臉部重新對應資料。</span><span class="sxs-lookup"><span data-stu-id="783b8-124">If the value supplied for this argument is **NULL**, face remap data is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="783b8-125">*ppVertexRemap* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="783b8-125">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="783b8-126">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="783b8-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="783b8-127">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址，其中包含每個頂點的 DWORD，以指定新頂點如何對應至舊頂點。</span><span class="sxs-lookup"><span data-stu-id="783b8-127">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="783b8-128">如果您需要根據新的頂點對應來改變外部資料，這個重新對應會很有用。</span><span class="sxs-lookup"><span data-stu-id="783b8-128">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span> <span data-ttu-id="783b8-129">如果提供給這個引數的值為 **Null**，則不會傳回頂點重新對應資料。</span><span class="sxs-lookup"><span data-stu-id="783b8-129">If the value supplied for this argument is **NULL**, vertex remap data is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="783b8-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="783b8-130">Return value</span></span>

<span data-ttu-id="783b8-131">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="783b8-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="783b8-132">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="783b8-132">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="783b8-133">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ CANNOTATTRSORT、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="783b8-133">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_CANNOTATTRSORT, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="783b8-134">備註</span><span class="sxs-lookup"><span data-stu-id="783b8-134">Remarks</span></span>

<span data-ttu-id="783b8-135">執行 **ID3DXMesh：： OptimizeInplace** 之前，應用程式必須藉由呼叫 [**ID3DXBaseMesh：： GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)來產生連續的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="783b8-135">Before running **ID3DXMesh::OptimizeInplace**, an application must generate an adjacency buffer by calling [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md).</span></span> <span data-ttu-id="783b8-136">鄰接緩衝區包含連續的資料，例如邊緣清單和彼此連續的臉部。</span><span class="sxs-lookup"><span data-stu-id="783b8-136">The adjacency buffer contains adjacency data, such as a list of edges and the faces that are adjacent to each other.</span></span>

> [!Note]  
> <span data-ttu-id="783b8-137">如果網格與另一個網格共用其頂點緩衝區，則此方法將會失敗，除非在 \_ 旗標中設定了 D3DXMESHOPT IGNOREVERTS。</span><span class="sxs-lookup"><span data-stu-id="783b8-137">This method will fail if the mesh is sharing its vertex buffer with another mesh, unless the D3DXMESHOPT\_IGNOREVERTS is set in Flags.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="783b8-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="783b8-138">Requirements</span></span>



| <span data-ttu-id="783b8-139">需求</span><span class="sxs-lookup"><span data-stu-id="783b8-139">Requirement</span></span> | <span data-ttu-id="783b8-140">值</span><span class="sxs-lookup"><span data-stu-id="783b8-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="783b8-141">標頭</span><span class="sxs-lookup"><span data-stu-id="783b8-141">Header</span></span><br/>  | <dl> <span data-ttu-id="783b8-142"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="783b8-142"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="783b8-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="783b8-143">Library</span></span><br/> | <dl> <span data-ttu-id="783b8-144"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="783b8-144"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="783b8-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="783b8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="783b8-146">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="783b8-146">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="783b8-147">**ID3DXMesh：： Optimize**</span><span class="sxs-lookup"><span data-stu-id="783b8-147">**ID3DXMesh::Optimize**</span></span>](id3dxmesh--optimize.md)
</dt> </dl>

 

 
