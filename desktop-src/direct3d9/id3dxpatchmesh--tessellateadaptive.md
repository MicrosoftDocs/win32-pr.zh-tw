---
description: 根據以 z 為基礎的調適型鑲嵌準則，執行適應性鑲嵌。
ms.assetid: 9f8f5c18-e866-4893-ba07-2a3c0d26c028
title: 'ID3DXPatchMesh：： TessellateAdaptive 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.TessellateAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e4cc6c6b7ff7b0cdb99e56386df49529f26c9166
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992332"
---
# <a name="id3dxpatchmeshtessellateadaptive-method"></a><span data-ttu-id="fe443-103">ID3DXPatchMesh：： TessellateAdaptive 方法</span><span class="sxs-lookup"><span data-stu-id="fe443-103">ID3DXPatchMesh::TessellateAdaptive method</span></span>

<span data-ttu-id="fe443-104">根據以 z 為基礎的調適型鑲嵌準則，執行適應性鑲嵌。</span><span class="sxs-lookup"><span data-stu-id="fe443-104">Performs adaptive tessellation based on the z-based adaptive tessellation criterion.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe443-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe443-105">Syntax</span></span>


```C++
HRESULT TessellateAdaptive(
  [in] const D3DXVECTOR4 *pTrans,
  [in]       DWORD       dwMaxTessLevel,
  [in]       DWORD       dwMinTessLevel,
  [in]       LPD3DXMESH  pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="fe443-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe443-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe443-107">*pTrans* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe443-107">*pTrans* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe443-108">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe443-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="fe443-109">指定以頂點表示的4D 向量，以取得每個頂點的自我調整鑲嵌量。</span><span class="sxs-lookup"><span data-stu-id="fe443-109">Specifies a 4D vector that is dotted with the vertices to get the per-vertex adaptive tessellation amount.</span></span> <span data-ttu-id="fe443-110">每個邊緣都會鑲嵌至它所連接的兩個頂點的鑲嵌層平均值。</span><span class="sxs-lookup"><span data-stu-id="fe443-110">Each edge is tessellated to the average value of the tessellation levels for the two vertices it connects.</span></span>

</dd> <dt>

<span data-ttu-id="fe443-111">*dwMaxTessLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe443-111">*dwMaxTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe443-112">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe443-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe443-113">適應性鑲嵌的最大限制。</span><span class="sxs-lookup"><span data-stu-id="fe443-113">Maximum limit for adaptive tessellation.</span></span> <span data-ttu-id="fe443-114">這是在現有頂點之間引進的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="fe443-114">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="fe443-115">這個整數值的範圍可以從1到32（含）。</span><span class="sxs-lookup"><span data-stu-id="fe443-115">This integer value can range from 1 to 32, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="fe443-116">*dwMinTessLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe443-116">*dwMinTessLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe443-117">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe443-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe443-118">適應性鑲嵌的最小限制。</span><span class="sxs-lookup"><span data-stu-id="fe443-118">Minimum limit for adaptive tessellation.</span></span> <span data-ttu-id="fe443-119">這是在現有頂點之間引進的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="fe443-119">This is the number of vertices introduced between existing vertices.</span></span> <span data-ttu-id="fe443-120">這個整數值的範圍可以從1到32（含）。</span><span class="sxs-lookup"><span data-stu-id="fe443-120">This integer value can range from 1 to 32, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="fe443-121">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe443-121">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe443-122">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="fe443-122">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="fe443-123">產生的鑲嵌網格。</span><span class="sxs-lookup"><span data-stu-id="fe443-123">Resulting tessellated mesh.</span></span> <span data-ttu-id="fe443-124">請參閱 [**ID3DXMesh**](id3dxmesh.md)。</span><span class="sxs-lookup"><span data-stu-id="fe443-124">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe443-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe443-125">Return value</span></span>

<span data-ttu-id="fe443-126">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe443-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe443-127">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="fe443-127">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fe443-128">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="fe443-128">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe443-129">備註</span><span class="sxs-lookup"><span data-stu-id="fe443-129">Remarks</span></span>

<span data-ttu-id="fe443-130">如果已使用 [**ID3DXPatchMesh：： Optimize**](id3dxpatchmesh--optimize.md)將修補程式網格優化，此函式將會更有效率地執行。</span><span class="sxs-lookup"><span data-stu-id="fe443-130">This function will perform more efficiently if the patch mesh has been optimized using [**ID3DXPatchMesh::Optimize**](id3dxpatchmesh--optimize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe443-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe443-131">Requirements</span></span>



| <span data-ttu-id="fe443-132">需求</span><span class="sxs-lookup"><span data-stu-id="fe443-132">Requirement</span></span> | <span data-ttu-id="fe443-133">值</span><span class="sxs-lookup"><span data-stu-id="fe443-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe443-134">標頭</span><span class="sxs-lookup"><span data-stu-id="fe443-134">Header</span></span><br/>  | <dl> <span data-ttu-id="fe443-135"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe443-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fe443-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="fe443-136">Library</span></span><br/> | <dl> <span data-ttu-id="fe443-137"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe443-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fe443-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe443-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe443-139">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="fe443-139">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
