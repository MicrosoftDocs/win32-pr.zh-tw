---
description: 將網格分割成小於指定大小的網格。
ms.assetid: 55cdd82f-91fa-4805-969f-8fbe53cbde58
title: 'D3DXSplitMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSplitMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d1f01cdb4ddd009f5cdf0b7f0310a492840955f1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107001480"
---
# <a name="d3dxsplitmesh-function"></a><span data-ttu-id="bf568-103">D3DXSplitMesh 函式</span><span class="sxs-lookup"><span data-stu-id="bf568-103">D3DXSplitMesh function</span></span>

<span data-ttu-id="bf568-104">將網格分割成小於指定大小的網格。</span><span class="sxs-lookup"><span data-stu-id="bf568-104">Splits a mesh into meshes smaller than the specified size.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf568-105">語法</span><span class="sxs-lookup"><span data-stu-id="bf568-105">Syntax</span></span>


```C++
void D3DXSplitMesh(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const DWORD        *pAdjacencyIn,
  _In_  const DWORD        MaxSize,
  _In_  const DWORD        Options,
  _Out_       DWORD        *pMeshesOut,
  _Out_       LPD3DXBUFFER *ppMeshArrayOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyArrayOut,
  _Out_       LPD3DXBUFFER *ppFaceRemapArrayOut,
  _Out_       LPD3DXBUFFER *ppVertRemapArrayOut
);
```



## <a name="parameters"></a><span data-ttu-id="bf568-106">參數</span><span class="sxs-lookup"><span data-stu-id="bf568-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf568-107">*pMeshIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bf568-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf568-108">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="bf568-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="bf568-109">[**ID3DXMesh**](id3dxmesh.md)介面的指標，代表來源網格。</span><span class="sxs-lookup"><span data-stu-id="bf568-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="bf568-110">*pAdjacencyIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bf568-110">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf568-111">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="bf568-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bf568-112">指標，指向每個臉部的三個 Dword 陣列，以指定要簡化網格中每個臉部的三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="bf568-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be simplified.</span></span>

</dd> <dt>

<span data-ttu-id="bf568-113">*MaxSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bf568-113">*MaxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf568-114">類型： **Const [**DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf568-114">Type: **const [**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf568-115">所產生網格中頂點的最大數目。</span><span class="sxs-lookup"><span data-stu-id="bf568-115">Maximum number of vertices in the resulting mesh.</span></span>

</dd> <dt>

<span data-ttu-id="bf568-116">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bf568-116">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf568-117">類型： **Const [**DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bf568-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bf568-118">新網格的選項旗標。</span><span class="sxs-lookup"><span data-stu-id="bf568-118">Option flags for the new meshes.</span></span>

</dd> <dt>

<span data-ttu-id="bf568-119">*pMeshesOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bf568-119">*pMeshesOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf568-120">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf568-120">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bf568-121">傳回的網格數目。</span><span class="sxs-lookup"><span data-stu-id="bf568-121">Number of meshes returned.</span></span>

</dd> <dt>

<span data-ttu-id="bf568-122">*ppMeshArrayOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bf568-122">*ppMeshArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf568-123">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf568-123">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="bf568-124">包含新網格 [**ID3DXMesh**](id3dxmesh.md) 介面陣列的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bf568-124">Buffer containing an array of [**ID3DXMesh**](id3dxmesh.md) interfaces for the new meshes.</span></span> <span data-ttu-id="bf568-125">如果來源網格分割成 n 個網格，則 *ppMeshArrayOut* 是 n 個 **ID3DXMesh** 指標的陣列。</span><span class="sxs-lookup"><span data-stu-id="bf568-125">For a source mesh split into n meshes, *ppMeshArrayOut* is an array of n **ID3DXMesh** pointers.</span></span>

</dd> <dt>

<span data-ttu-id="bf568-126">*ppAdjacencyArrayOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bf568-126">*ppAdjacencyArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf568-127">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf568-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="bf568-128">包含相鄰陣列陣列的緩衝區， (Dword) 用於新的網格。</span><span class="sxs-lookup"><span data-stu-id="bf568-128">Buffer containing an array of adjacency arrays (DWORDs) for the new meshes.</span></span> <span data-ttu-id="bf568-129">請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="bf568-129">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="bf568-130">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="bf568-130">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="bf568-131">*ppFaceRemapArrayOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bf568-131">*ppFaceRemapArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf568-132">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf568-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="bf568-133">包含臉部重新對應陣列陣列的緩衝區， (Dword) 用於新的網格。</span><span class="sxs-lookup"><span data-stu-id="bf568-133">Buffer containing an array of face remap arrays (DWORDs) for the new meshes.</span></span> <span data-ttu-id="bf568-134">請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="bf568-134">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="bf568-135">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="bf568-135">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="bf568-136">*ppVertRemapArrayOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bf568-136">*ppVertRemapArrayOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf568-137">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="bf568-137">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="bf568-138">包含新網格之頂點重新對應陣列陣列的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bf568-138">Buffer containing an array of vertex remap arrays for the new meshes.</span></span> <span data-ttu-id="bf568-139">請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="bf568-139">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span> <span data-ttu-id="bf568-140">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="bf568-140">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf568-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf568-141">Return value</span></span>

<span data-ttu-id="bf568-142">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="bf568-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bf568-143">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="bf568-143">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf568-144">備註</span><span class="sxs-lookup"><span data-stu-id="bf568-144">Remarks</span></span>

<span data-ttu-id="bf568-145">此函式的常見用法是將具有32位索引的網格分割 (超過65535個頂點) 多個網格中，每個網格都有16位的索引。</span><span class="sxs-lookup"><span data-stu-id="bf568-145">A common use of this function is to split a mesh with 32-bit indices (more than 65535 vertices) into more than one mesh, each of which has 16-bit indices.</span></span>

<span data-ttu-id="bf568-146">相鄰、頂點重新對應和臉部重新對應陣列是一個 Dword，其中每個陣列包含 n 個 DWORD 指標，後面接著指標所參考的 DWORD 資料。</span><span class="sxs-lookup"><span data-stu-id="bf568-146">The adjacency, vertex remap and face remap arrays are arrays are DWORDs where each array contains n DWORD pointers, followed by the DWORD data referenced by the pointers.</span></span> <span data-ttu-id="bf568-147">例如，若要取得網格2中臉部3的臉部重新對應資訊，可使用下列程式碼，假設臉部重新對應資料是在名為 *ppFaceRemapArrayOut* 的變數中傳回。</span><span class="sxs-lookup"><span data-stu-id="bf568-147">For example, to obtain the face remap information for face 3 in mesh 2, the following code could be used, assuming the face remap data was returned in a variable named *ppFaceRemapArrayOut*.</span></span>


```
   
const DWORD **face_remaps = 
    static_cast<DWORD **>(ppFaceRemapArrayOut->GetBufferPointer());
const DWORD remap = face_remaps[2][3];
```



## <a name="requirements"></a><span data-ttu-id="bf568-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf568-148">Requirements</span></span>



| <span data-ttu-id="bf568-149">需求</span><span class="sxs-lookup"><span data-stu-id="bf568-149">Requirement</span></span> | <span data-ttu-id="bf568-150">值</span><span class="sxs-lookup"><span data-stu-id="bf568-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf568-151">標頭</span><span class="sxs-lookup"><span data-stu-id="bf568-151">Header</span></span><br/>  | <dl> <span data-ttu-id="bf568-152"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="bf568-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bf568-153">程式庫</span><span class="sxs-lookup"><span data-stu-id="bf568-153">Library</span></span><br/> | <dl> <span data-ttu-id="bf568-154"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf568-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bf568-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf568-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf568-156">網格函數</span><span class="sxs-lookup"><span data-stu-id="bf568-156">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
