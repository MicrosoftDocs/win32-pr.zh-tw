---
description: 將指定的網格子集轉換成一連串的條紋。
ms.assetid: 4f005383-6a5a-4393-ac88-202e45946d3d
title: 'D3DXConvertMeshSubsetToStrips 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToStrips
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d62461c13f76eb0efce809fa1114771a5ea2fe6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000621"
---
# <a name="d3dxconvertmeshsubsettostrips-function"></a><span data-ttu-id="82f81-103">D3DXConvertMeshSubsetToStrips 函式</span><span class="sxs-lookup"><span data-stu-id="82f81-103">D3DXConvertMeshSubsetToStrips function</span></span>

<span data-ttu-id="82f81-104">將指定的網格子集轉換成一連串的條紋。</span><span class="sxs-lookup"><span data-stu-id="82f81-104">Convert the specified mesh subset into a series of strips.</span></span>

## <a name="syntax"></a><span data-ttu-id="82f81-105">語法</span><span class="sxs-lookup"><span data-stu-id="82f81-105">Syntax</span></span>


```C++
HRESULT D3DXConvertMeshSubsetToStrips(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices,
  _Out_ LPD3DXBUFFER           *ppStripLengths,
  _Out_ DWORD                  *pNumStrips
);
```



## <a name="parameters"></a><span data-ttu-id="82f81-106">參數</span><span class="sxs-lookup"><span data-stu-id="82f81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82f81-107">*MeshIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82f81-107">*MeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82f81-108">類型： **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="82f81-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="82f81-109">[**ID3DXBaseMesh**](id3dxbasemesh.md)介面的指標，代表要轉換成條紋的網格。</span><span class="sxs-lookup"><span data-stu-id="82f81-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to convert to a strip.</span></span>

</dd> <dt>

<span data-ttu-id="82f81-110">*AttribId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82f81-110">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82f81-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82f81-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82f81-112">要轉換成條紋之網格子集的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="82f81-112">Attribute ID of the mesh subset to convert to strips.</span></span>

</dd> <dt>

<span data-ttu-id="82f81-113">*IBOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82f81-113">*IBOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82f81-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82f81-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82f81-115">結合 [**D3DXMESH**](./d3dxmesh.md) 列舉中的一或多個旗標，指定建立索引緩衝區的選項。</span><span class="sxs-lookup"><span data-stu-id="82f81-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for creating the index buffer.</span></span> <span data-ttu-id="82f81-116">不可為 D3DXMESH \_ 32 位。</span><span class="sxs-lookup"><span data-stu-id="82f81-116">Cannot be D3DXMESH\_32BIT.</span></span> <span data-ttu-id="82f81-117">根據 *MeshIn* 參數所指定之網格的索引緩衝區格式，將會使用32位或16位索引來建立索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="82f81-117">The index buffer will be created with 32-bit or 16-bit indices depending on the format of the index buffer of the mesh specified by the *MeshIn* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="82f81-118">*ppIndexBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="82f81-118">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82f81-119">類型： **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="82f81-119">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="82f81-120">[**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)介面的指標，代表包含該帶的索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="82f81-120">Pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing index buffer containing the strip.</span></span>

</dd> <dt>

<span data-ttu-id="82f81-121">*pNumIndices* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="82f81-121">*pNumIndices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82f81-122">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="82f81-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="82f81-123">在 *ppIndexBuffer* 參數中傳回之緩衝區中的索引數目。</span><span class="sxs-lookup"><span data-stu-id="82f81-123">Number of indices in the buffer returned in the *ppIndexBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="82f81-124">*ppStripLengths* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="82f81-124">*ppStripLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82f81-125">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="82f81-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="82f81-126">緩衝區，其中包含一個 DWORD 的陣列，每個區域會指定該區域內的三角形數目。</span><span class="sxs-lookup"><span data-stu-id="82f81-126">Buffer containing an array of one DWORD per strip, which specifies the number of triangles in the that strip.</span></span>

</dd> <dt>

<span data-ttu-id="82f81-127">*pNumStrips* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="82f81-127">*pNumStrips* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82f81-128">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="82f81-128">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="82f81-129">索引緩衝區中的個別條紋數目和對應的帶長度陣列。</span><span class="sxs-lookup"><span data-stu-id="82f81-129">Number of individual strips in the index buffer and corresponding strip length array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82f81-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="82f81-130">Return value</span></span>

<span data-ttu-id="82f81-131">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="82f81-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="82f81-132">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="82f81-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="82f81-133">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="82f81-133">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="82f81-134">備註</span><span class="sxs-lookup"><span data-stu-id="82f81-134">Remarks</span></span>

<span data-ttu-id="82f81-135">在執行此函式之前，請呼叫 [**Optimize**](id3dxmesh--optimize.md) 或 [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)，並 \_ 設定 D3DXMESHOPT ATTRSORT 旗標。</span><span class="sxs-lookup"><span data-stu-id="82f81-135">Before running this function, call [**Optimize**](id3dxmesh--optimize.md) or [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), with the D3DXMESHOPT\_ATTRSORT flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="82f81-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="82f81-136">Requirements</span></span>



| <span data-ttu-id="82f81-137">需求</span><span class="sxs-lookup"><span data-stu-id="82f81-137">Requirement</span></span> | <span data-ttu-id="82f81-138">值</span><span class="sxs-lookup"><span data-stu-id="82f81-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82f81-139">標頭</span><span class="sxs-lookup"><span data-stu-id="82f81-139">Header</span></span><br/>  | <dl> <span data-ttu-id="82f81-140"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="82f81-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="82f81-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="82f81-141">Library</span></span><br/> | <dl> <span data-ttu-id="82f81-142"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="82f81-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="82f81-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82f81-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82f81-144">網格函數</span><span class="sxs-lookup"><span data-stu-id="82f81-144">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
