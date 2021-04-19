---
description: 從輸入網格和材質資料建立 ID3DXTextureGutterHelper 物件。
ms.assetid: 1696fc3d-5b35-48cc-a79b-c0d4ed44e420
title: 'D3DXCreateTextureGutterHelper 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureGutterHelper
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8957649f3cef6ea67932579918163613160ee993
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999008"
---
# <a name="d3dxcreatetexturegutterhelper-function"></a><span data-ttu-id="2da91-103">D3DXCreateTextureGutterHelper 函式</span><span class="sxs-lookup"><span data-stu-id="2da91-103">D3DXCreateTextureGutterHelper function</span></span>

<span data-ttu-id="2da91-104">從輸入網格和材質資料建立 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="2da91-104">Creates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object from an input mesh and texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2da91-105">語法</span><span class="sxs-lookup"><span data-stu-id="2da91-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureGutterHelper(
  _In_    UINT                      Width,
  _In_    UINT                      Height,
  _In_    LPD3DXMESH                pMesh,
  _In_    FLOAT                     GutterSize,
  _Inout_ LPD3DXTEXTUREGUTTERHELPER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="2da91-106">參數</span><span class="sxs-lookup"><span data-stu-id="2da91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2da91-107">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2da91-107">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2da91-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2da91-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2da91-109">材質的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2da91-109">Width of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="2da91-110">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2da91-110">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2da91-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2da91-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2da91-112">紋理的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="2da91-112">Height of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="2da91-113">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2da91-113">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2da91-114">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="2da91-114">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="2da91-115">輸入 [**ID3DXMesh**](id3dxmesh.md) 網格物件的指標。</span><span class="sxs-lookup"><span data-stu-id="2da91-115">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="2da91-116">*GutterSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2da91-116">*GutterSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2da91-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2da91-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2da91-118">用來過度取樣材質和建立裝訂邊區域的材質數目。</span><span class="sxs-lookup"><span data-stu-id="2da91-118">Number of texels by which to over-sample the texture and create the gutter region.</span></span> <span data-ttu-id="2da91-119">必須至少為1。</span><span class="sxs-lookup"><span data-stu-id="2da91-119">Must be at least 1.</span></span>

</dd> <dt>

<span data-ttu-id="2da91-120">*ppBuffer* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2da91-120">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2da91-121">類型： **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***</span><span class="sxs-lookup"><span data-stu-id="2da91-121">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***</span></span>

<span data-ttu-id="2da91-122">要建立之 [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="2da91-122">Pointer to an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2da91-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="2da91-123">Return value</span></span>

<span data-ttu-id="2da91-124">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2da91-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2da91-125">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="2da91-125">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2da91-126">如果函式失敗，則傳回值可以是下列其中一個： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="2da91-126">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2da91-127">備註</span><span class="sxs-lookup"><span data-stu-id="2da91-127">Remarks</span></span>

<span data-ttu-id="2da91-128">使用 [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) 將場景轉換成新座標。</span><span class="sxs-lookup"><span data-stu-id="2da91-128">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) to transform a scene to new coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="2da91-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="2da91-129">Requirements</span></span>



| <span data-ttu-id="2da91-130">需求</span><span class="sxs-lookup"><span data-stu-id="2da91-130">Requirement</span></span> | <span data-ttu-id="2da91-131">值</span><span class="sxs-lookup"><span data-stu-id="2da91-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2da91-132">標頭</span><span class="sxs-lookup"><span data-stu-id="2da91-132">Header</span></span><br/>  | <dl> <span data-ttu-id="2da91-133"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="2da91-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="2da91-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="2da91-134">Library</span></span><br/> | <dl> <span data-ttu-id="2da91-135"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2da91-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2da91-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2da91-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da91-137">預先計算 Radiance 傳送函式</span><span class="sxs-lookup"><span data-stu-id="2da91-137">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
