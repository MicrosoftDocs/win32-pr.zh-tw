---
description: 將具有相同屬性的已複寫頂點一起進行焊縫。 這個方法會使用指定的 epsilon 值進行相等比較。
ms.assetid: bddf6e0c-55a1-40d2-8681-e7f0f9002bfa
title: 'D3DXWeldVertices 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWeldVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 76e0a6f259bc8ba547a02b2e95cccf718d54e904
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696667"
---
# <a name="d3dxweldvertices-function"></a><span data-ttu-id="a8d26-104">D3DXWeldVertices 函式</span><span class="sxs-lookup"><span data-stu-id="a8d26-104">D3DXWeldVertices function</span></span>

<span data-ttu-id="a8d26-105">將具有相同屬性的已複寫頂點一起進行焊縫。</span><span class="sxs-lookup"><span data-stu-id="a8d26-105">Welds together replicated vertices that have equal attributes.</span></span> <span data-ttu-id="a8d26-106">這個方法會使用指定的 epsilon 值進行相等比較。</span><span class="sxs-lookup"><span data-stu-id="a8d26-106">This method uses specified epsilon values for equality comparisons.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8d26-107">語法</span><span class="sxs-lookup"><span data-stu-id="a8d26-107">Syntax</span></span>


```C++
HRESULT D3DXWeldVertices(
  _In_          LPD3DXMESH       pMesh,
  _In_          DWORD            Flags,
  _In_    const D3DXWeldEpsilons *pEpsilons,
  _In_    const DWORD            *pAdjacencyIn,
  _Inout_       DWORD            *pAdjacencyOut,
  _Out_         DWORD            *pFaceRemap,
  _Out_         LPD3DXBUFFER     *ppVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="a8d26-108">參數</span><span class="sxs-lookup"><span data-stu-id="a8d26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8d26-109">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8d26-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d26-110">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="a8d26-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="a8d26-111">[**ID3DXMesh**](id3dxmesh.md)物件的指標，也就是用來焊接頂點的網格。</span><span class="sxs-lookup"><span data-stu-id="a8d26-111">Pointer to an [**ID3DXMesh**](id3dxmesh.md) object, the mesh from which to weld vertices.</span></span>

</dd> <dt>

<span data-ttu-id="a8d26-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="a8d26-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d26-113">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8d26-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8d26-114">[**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md)中一或多個旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="a8d26-114">Combination of one or more flags from [**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8d26-115">*pEpsilons* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8d26-115">*pEpsilons* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d26-116">Type： **Const [**D3DXWeldEpsilons**](d3dxweldepsilons.md) \***</span><span class="sxs-lookup"><span data-stu-id="a8d26-116">Type: **const [**D3DXWeldEpsilons**](d3dxweldepsilons.md)\***</span></span>

<span data-ttu-id="a8d26-117">[**D3DXWeldEpsilons**](d3dxweldepsilons.md)結構的指標，指定要用於此方法的 epsilon 值。</span><span class="sxs-lookup"><span data-stu-id="a8d26-117">Pointer to a [**D3DXWeldEpsilons**](d3dxweldepsilons.md) structure, specifying the epsilon values to be used for this method.</span></span> <span data-ttu-id="a8d26-118">使用 **Null** 將所有結構成員初始化為預設值 1.0 e-6f。</span><span class="sxs-lookup"><span data-stu-id="a8d26-118">Use **NULL** to initialize all structure members to a default value of 1.0e-6f.</span></span>

</dd> <dt>

<span data-ttu-id="a8d26-119">*pAdjacencyIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8d26-119">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d26-120">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a8d26-120">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a8d26-121">指標，指向每個臉部的三個 Dword 陣列，以針對來源網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="a8d26-121">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="a8d26-122">如果邊緣沒有連續的臉部，則值為0xffffffff。</span><span class="sxs-lookup"><span data-stu-id="a8d26-122">If the edge has no adjacent faces, the value is 0xffffffff.</span></span> <span data-ttu-id="a8d26-123">如果此參數設定為 **Null**，則會呼叫 [**ID3DXBaseMesh：： GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) 來建立邏輯相鄰資訊。</span><span class="sxs-lookup"><span data-stu-id="a8d26-123">If this parameter is set to **NULL**, [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) will be called to create logical adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="a8d26-124">*pAdjacencyOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="a8d26-124">*pAdjacencyOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d26-125">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8d26-125">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a8d26-126">指標，指向每個臉部的三個 Dword 陣列，以針對優化網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="a8d26-126">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the optimized mesh.</span></span> <span data-ttu-id="a8d26-127">如果邊緣沒有連續的臉部，則值為0xffffffff。</span><span class="sxs-lookup"><span data-stu-id="a8d26-127">If the edge has no adjacent faces, the value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="a8d26-128">*pFaceRemap* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a8d26-128">*pFaceRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d26-129">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8d26-129">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a8d26-130">Dword 的陣列，每個臉部各一個，用來識別對應至焊接網格中各臉部的原始網格臉部。</span><span class="sxs-lookup"><span data-stu-id="a8d26-130">An array of DWORDs, one per face, that identifies the original mesh face that corresponds to each face in the welded mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a8d26-131">*ppVertexRemap* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a8d26-131">*ppVertexRemap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8d26-132">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8d26-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a8d26-133">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址，其中包含每個頂點的 DWORD，以指定新頂點如何對應至舊頂點。</span><span class="sxs-lookup"><span data-stu-id="a8d26-133">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains a DWORD for each vertex that specifies how the new vertices map to the old vertices.</span></span> <span data-ttu-id="a8d26-134">如果您需要根據新的頂點對應來改變外部資料，這個重新對應會很有用。</span><span class="sxs-lookup"><span data-stu-id="a8d26-134">This remap is useful if you need to alter external data based on the new vertex mapping.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8d26-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8d26-135">Return value</span></span>

<span data-ttu-id="a8d26-136">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a8d26-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a8d26-137">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="a8d26-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a8d26-138">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="a8d26-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8d26-139">備註</span><span class="sxs-lookup"><span data-stu-id="a8d26-139">Remarks</span></span>

<span data-ttu-id="a8d26-140">此函數會使用提供的相鄰資訊來判斷複寫的點。</span><span class="sxs-lookup"><span data-stu-id="a8d26-140">This function uses supplied adjacency information to determine the points that are replicated.</span></span> <span data-ttu-id="a8d26-141">頂點會根據 epsilon 比較來合併。</span><span class="sxs-lookup"><span data-stu-id="a8d26-141">Vertices are merged based on an epsilon comparison.</span></span> <span data-ttu-id="a8d26-142">具有相等位置的頂點必須已經過計算，並以點代表資料表示。</span><span class="sxs-lookup"><span data-stu-id="a8d26-142">Vertices with equal position must already have been calculated and represented by point-representative data.</span></span>

<span data-ttu-id="a8d26-143">此函式會結合具有類似元件的邏輯上焊接頂點，例如 pEpsilons 內的法線或紋理座標。</span><span class="sxs-lookup"><span data-stu-id="a8d26-143">This function combines logically-welded vertices that have similar components, such as normals or texture coordinates within pEpsilons.</span></span>

<span data-ttu-id="a8d26-144">下列範例程式碼會呼叫此函數，並啟用焊接。</span><span class="sxs-lookup"><span data-stu-id="a8d26-144">The following example code calls this function with welding enabled.</span></span> <span data-ttu-id="a8d26-145">頂點會使用標準向量和頂點位置的 epsilon 值進行比較。</span><span class="sxs-lookup"><span data-stu-id="a8d26-145">Vertices are compared using epsilon values for normal vector and vertex position.</span></span> <span data-ttu-id="a8d26-146">指標會傳回至臉部重新對應陣列， (*pFaceRemap*) 。</span><span class="sxs-lookup"><span data-stu-id="a8d26-146">A pointer is returned to a face remapping array (*pFaceRemap*).</span></span>


```
TCHAR            strMediaPath[512];       // X-file path 
LPD3DXBUFFER     pAdjacencyBuffer = NULL; // adjacency data buffer
LPD3DXBUFFER     pD3DXMtrlBuffer  = NULL; // material buffer
LPD3DXMESH       pMesh            = NULL; // mesh object
DWORD            m_dwNumMaterials;        // number of materials
D3DXWELDEPSILONS Epsilons;                // structure with epsilon values
DWORD            *pFaceRemap[65536];      // face remapping array
DWORD            i;                       // internal variable
    
    // Load the mesh from the specified file
    hr = D3DXLoadMeshFromX ( strMediaPath,
                         D3DXMESH_MANAGED,
                         m_pd3dDevice,
                         &pAdjacencyBuffer,
                         &pD3DXMtrlBuffer,
                         NULL,
                         &m_dwNumMaterials,
                         &pMesh ) )
                             
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
    
    // Set epsilon values
    Epsilons.Normal = 0.001;
    Epsilons.Position = 0.1;
    
    // Weld the vertices
    for( i=0; i < 65536; i++ )
    { 
        pFaceRemap[i] = 0; 
    }
    
    hr = D3DXWeldVertices ( pMesh,
                            D3DXWELDEPSILONS_WELDPARTIALMATCHES,
                            &Epsilons,
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pFaceRemap,
                            NULL )
                            
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
```



## <a name="requirements"></a><span data-ttu-id="a8d26-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8d26-147">Requirements</span></span>



| <span data-ttu-id="a8d26-148">需求</span><span class="sxs-lookup"><span data-stu-id="a8d26-148">Requirement</span></span> | <span data-ttu-id="a8d26-149">值</span><span class="sxs-lookup"><span data-stu-id="a8d26-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d26-150">標頭</span><span class="sxs-lookup"><span data-stu-id="a8d26-150">Header</span></span><br/>  | <dl> <span data-ttu-id="a8d26-151"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="a8d26-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a8d26-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="a8d26-152">Library</span></span><br/> | <dl> <span data-ttu-id="a8d26-153"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8d26-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a8d26-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8d26-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8d26-155">網格函數</span><span class="sxs-lookup"><span data-stu-id="a8d26-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
