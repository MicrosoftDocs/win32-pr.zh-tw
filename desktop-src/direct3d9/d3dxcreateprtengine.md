---
description: 建立 ID3DXPRTEngine 物件，該物件可以有效率地產生3D 場景的預先計算 radiance 傳輸 (PRT) 模擬。
ms.assetid: fdfe02b5-03fb-4bee-a53b-012ae3572644
title: 'D3DXCreatePRTEngine 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTEngine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b76b58953de81041922659c3315bba9cdf7788b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514612"
---
# <a name="d3dxcreateprtengine-function"></a><span data-ttu-id="5a47f-103">D3DXCreatePRTEngine 函式</span><span class="sxs-lookup"><span data-stu-id="5a47f-103">D3DXCreatePRTEngine function</span></span>

<span data-ttu-id="5a47f-104">建立 [**ID3DXPRTEngine**](id3dxprtengine.md) 物件，該物件可以有效率地產生3d 場景的預先計算 radiance 傳輸 (PRT) 模擬。</span><span class="sxs-lookup"><span data-stu-id="5a47f-104">Creates an [**ID3DXPRTEngine**](id3dxprtengine.md) object that can efficiently generate precomputed radiance transfer (PRT) simulations of a 3D scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a47f-105">語法</span><span class="sxs-lookup"><span data-stu-id="5a47f-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTEngine(
  _In_    LPD3DXMESH      pMesh,
  _In_    DWORD           *pAdjacency,
  _In_    BOOL            ExtractUVs,
  _In_    LPD3DXMESH      pBlockerMesh,
  _Inout_ LPD3DXPRTENGINE ppEngine
);
```



## <a name="parameters"></a><span data-ttu-id="5a47f-106">參數</span><span class="sxs-lookup"><span data-stu-id="5a47f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a47f-107">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a47f-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a47f-108">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="5a47f-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="5a47f-109">輸入 [**ID3DXMesh**](id3dxmesh.md) 網格物件的指標，該物件會將3d 場景模型。</span><span class="sxs-lookup"><span data-stu-id="5a47f-109">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object that models the 3D scene.</span></span> <span data-ttu-id="5a47f-110">這個網格必須有一個屬性工作表，其中頂點位於唯一的屬性中。</span><span class="sxs-lookup"><span data-stu-id="5a47f-110">This mesh must have an attribute table in which vertices are in a unique attribute.</span></span>

</dd> <dt>

<span data-ttu-id="5a47f-111">*pAdjacency* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a47f-111">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a47f-112">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a47f-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5a47f-113">選擇性的指標，指向每個臉部的三個 Dword 陣列，以填滿連續的臉部索引。</span><span class="sxs-lookup"><span data-stu-id="5a47f-113">Optional pointer to an array of three DWORDs per face to be filled with adjacent face indices.</span></span> <span data-ttu-id="5a47f-114">此陣列中的位元組數目必須至少為 ( (3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD) ) 。</span><span class="sxs-lookup"><span data-stu-id="5a47f-114">The number of bytes in this array must be at least ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof(DWORD)).</span></span> <span data-ttu-id="5a47f-115">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5a47f-115">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5a47f-116">*ExtractUVs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a47f-116">*ExtractUVs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a47f-117">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5a47f-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5a47f-118">若 **為 TRUE**，則會使用紋理來儲存 ALBEDOS 或 PRT 向量。</span><span class="sxs-lookup"><span data-stu-id="5a47f-118">If **TRUE**, textures will be used to store albedos or PRT vectors.</span></span>

</dd> <dt>

<span data-ttu-id="5a47f-119">*pBlockerMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a47f-119">*pBlockerMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a47f-120">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="5a47f-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="5a47f-121">封鎖3D 場景之選擇性 [**ID3DXMesh**](id3dxmesh.md) 網格物件的指標。</span><span class="sxs-lookup"><span data-stu-id="5a47f-121">Pointer to an optional [**ID3DXMesh**](id3dxmesh.md) mesh object that blocks the 3D scene.</span></span> <span data-ttu-id="5a47f-122">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5a47f-122">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5a47f-123">*ppEngine* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="5a47f-123">*ppEngine* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a47f-124">類型： **[ **LPD3DXPRTENGINE**](id3dxprtengine.md)**</span><span class="sxs-lookup"><span data-stu-id="5a47f-124">Type: **[**LPD3DXPRTENGINE**](id3dxprtengine.md)**</span></span>

<span data-ttu-id="5a47f-125">輸出 [**ID3DXPRTEngine**](id3dxprtengine.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="5a47f-125">Pointer to an output [**ID3DXPRTEngine**](id3dxprtengine.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a47f-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a47f-126">Return value</span></span>

<span data-ttu-id="5a47f-127">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a47f-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a47f-128">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="5a47f-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5a47f-129">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="5a47f-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a47f-130">備註</span><span class="sxs-lookup"><span data-stu-id="5a47f-130">Remarks</span></span>

<span data-ttu-id="5a47f-131">使用 [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) 將多個網格合併為單一網格介面。</span><span class="sxs-lookup"><span data-stu-id="5a47f-131">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) to combine multiple meshes into a single mesh interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a47f-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a47f-132">Requirements</span></span>



| <span data-ttu-id="5a47f-133">需求</span><span class="sxs-lookup"><span data-stu-id="5a47f-133">Requirement</span></span> | <span data-ttu-id="5a47f-134">值</span><span class="sxs-lookup"><span data-stu-id="5a47f-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a47f-135">標頭</span><span class="sxs-lookup"><span data-stu-id="5a47f-135">Header</span></span><br/>  | <dl> <span data-ttu-id="5a47f-136"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a47f-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5a47f-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="5a47f-137">Library</span></span><br/> | <dl> <span data-ttu-id="5a47f-138"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a47f-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5a47f-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a47f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a47f-140">預先計算 Radiance 傳送函式</span><span class="sxs-lookup"><span data-stu-id="5a47f-140">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
