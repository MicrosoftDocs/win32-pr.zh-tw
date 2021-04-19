---
description: 使用提供的加權（盡可能接近指定的 MinValue）產生簡化的網格。
ms.assetid: 589356a9-f272-4851-92ae-54dbecc0b234
title: 'D3DXSimplifyMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSimplifyMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0258047631a41e31d108ba45531988e4cb6a35ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993878"
---
# <a name="d3dxsimplifymesh-function"></a><span data-ttu-id="07bf2-103">D3DXSimplifyMesh 函式</span><span class="sxs-lookup"><span data-stu-id="07bf2-103">D3DXSimplifyMesh function</span></span>

<span data-ttu-id="07bf2-104">使用提供的加權（盡可能接近指定的 MinValue）產生簡化的網格。</span><span class="sxs-lookup"><span data-stu-id="07bf2-104">Generates a simplified mesh using the provided weights that come as close as possible to the given MinValue.</span></span>

## <a name="syntax"></a><span data-ttu-id="07bf2-105">語法</span><span class="sxs-lookup"><span data-stu-id="07bf2-105">Syntax</span></span>


```C++
HRESULT D3DXSimplifyMesh(
  _In_        LPD3DXMESH           pMesh,
  _In_  const DWORD                *pAdjacency,
  _In_  const D3DXATTRIBUTEWEIGHTS *pVertexAttributeWeights,
  _In_  const FLOAT                *pVertexWeights,
  _In_        DWORD                MinValue,
  _In_        DWORD                Options,
  _Out_       LPD3DXMESH           *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="07bf2-106">參數</span><span class="sxs-lookup"><span data-stu-id="07bf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07bf2-107">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07bf2-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07bf2-108">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="07bf2-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="07bf2-109">[**ID3DXMesh**](id3dxmesh.md)介面的指標，代表來源網格。</span><span class="sxs-lookup"><span data-stu-id="07bf2-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="07bf2-110">*pAdjacency* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07bf2-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07bf2-111">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="07bf2-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="07bf2-112">指標，指向每個臉部的三個 Dword 陣列，以指定要簡化網格中每個臉部的三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="07bf2-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be simplified.</span></span>

</dd> <dt>

<span data-ttu-id="07bf2-113">*pVertexAttributeWeights* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07bf2-113">*pVertexAttributeWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07bf2-114">Type： **Const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) \***</span><span class="sxs-lookup"><span data-stu-id="07bf2-114">Type: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md)\***</span></span>

<span data-ttu-id="07bf2-115">[**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md)結構的指標，其中包含每個頂點元件的權數。</span><span class="sxs-lookup"><span data-stu-id="07bf2-115">Pointer to a [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) structure, containing the weight for each vertex component.</span></span> <span data-ttu-id="07bf2-116">如果此參數設定為 **Null**，則會使用預設結構。</span><span class="sxs-lookup"><span data-stu-id="07bf2-116">If this parameter is set to **NULL**, a default structure is used.</span></span> <span data-ttu-id="07bf2-117">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="07bf2-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="07bf2-118">*pVertexWeights* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07bf2-118">*pVertexWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07bf2-119">Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="07bf2-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="07bf2-120">頂點加權陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="07bf2-120">Pointer to an array of vertex weights.</span></span> <span data-ttu-id="07bf2-121">如果此參數設定為 **Null**，則所有頂點加權都會設定為1.0。</span><span class="sxs-lookup"><span data-stu-id="07bf2-121">If this parameter is set to **NULL**, all vertex weights are set to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="07bf2-122">*MinValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07bf2-122">*MinValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07bf2-123">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07bf2-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07bf2-124">頂點或臉部的數目（視 *Options* 參數中設定的旗標而定），藉此簡化來源網格。</span><span class="sxs-lookup"><span data-stu-id="07bf2-124">Number of vertices or faces, depending on the flag set in the *Options* parameter, by which to simplify the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="07bf2-125">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07bf2-125">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07bf2-126">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07bf2-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07bf2-127">指定網格的簡化選項。</span><span class="sxs-lookup"><span data-stu-id="07bf2-127">Specifies simplification options for the mesh.</span></span> <span data-ttu-id="07bf2-128">您可以設定 [**D3DXMESHSIMP**](./d3dxmeshsimp.md) 中的其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="07bf2-128">One of the flags in [**D3DXMESHSIMP**](./d3dxmeshsimp.md) can be set.</span></span>

</dd> <dt>

<span data-ttu-id="07bf2-129">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="07bf2-129">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07bf2-130">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="07bf2-130">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="07bf2-131">[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示傳回的簡化網格。</span><span class="sxs-lookup"><span data-stu-id="07bf2-131">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned simplification mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07bf2-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="07bf2-132">Return value</span></span>

<span data-ttu-id="07bf2-133">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="07bf2-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="07bf2-134">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="07bf2-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="07bf2-135">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="07bf2-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="07bf2-136">備註</span><span class="sxs-lookup"><span data-stu-id="07bf2-136">Remarks</span></span>

<span data-ttu-id="07bf2-137">此函數會產生具有 *MinValue* 頂點或臉部的網格。</span><span class="sxs-lookup"><span data-stu-id="07bf2-137">This function generates a mesh that has *MinValue* vertices or faces.</span></span>

<span data-ttu-id="07bf2-138">如果簡化程式無法減少 *MinValue* 的網格，則呼叫仍然會成功，因為 *MinValue* 是所需的最小值，而不是絕對最小值。</span><span class="sxs-lookup"><span data-stu-id="07bf2-138">If the simplification process cannot reduce the mesh to *MinValue*, the call still succeeds because *MinValue* is a desired minimum, not an absolute minimum.</span></span>

<span data-ttu-id="07bf2-139">如果 *pVertexAttributeWeights* 設定為 **Null**，則會將下列值指派給預設的 [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="07bf2-139">If *pVertexAttributeWeights* is set to **NULL**, the following values are assigned to the default [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) structure.</span></span>


```
D3DXATTRIBUTEWEIGHTS AttributeWeights;
    
AttributeWeights.Position  = 1.0;
AttributeWeights.Boundary =  1.0;
AttributeWeights.Normal   =  1.0;
AttributeWeights.Diffuse  =  0.0;
AttributeWeights.Specular =  0.0;
AttributeWeights.Tex[8]   =  {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
```



<span data-ttu-id="07bf2-140">這是大部分應用程式應該使用的預設結構，因為它只會考慮幾何和一般調整。</span><span class="sxs-lookup"><span data-stu-id="07bf2-140">This default structure is what most applications should use because it considers only geometric and normal adjustment.</span></span> <span data-ttu-id="07bf2-141">只有在特殊情況下，才會需要修改其他成員欄位。</span><span class="sxs-lookup"><span data-stu-id="07bf2-141">Only in special cases will the other member fields need to be modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="07bf2-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="07bf2-142">Requirements</span></span>



| <span data-ttu-id="07bf2-143">需求</span><span class="sxs-lookup"><span data-stu-id="07bf2-143">Requirement</span></span> | <span data-ttu-id="07bf2-144">值</span><span class="sxs-lookup"><span data-stu-id="07bf2-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07bf2-145">標頭</span><span class="sxs-lookup"><span data-stu-id="07bf2-145">Header</span></span><br/>  | <dl> <span data-ttu-id="07bf2-146"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="07bf2-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="07bf2-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="07bf2-147">Library</span></span><br/> | <dl> <span data-ttu-id="07bf2-148"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="07bf2-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="07bf2-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07bf2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07bf2-150">網格函數</span><span class="sxs-lookup"><span data-stu-id="07bf2-150">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
