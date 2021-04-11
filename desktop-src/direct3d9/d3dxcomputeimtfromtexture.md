---
description: 從對應至網格的材質計算每個三角形的 IMT，以選擇性地當做 D3DX UVAtlas 函式的輸入使用。
ms.assetid: 6671edc4-e494-4847-ae99-b9e56651a875
title: 'D3DXComputeIMTFromTexture 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2fbed0411f3562e3a05ec2ec4df99dfad6d8c902
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035402"
---
# <a name="d3dxcomputeimtfromtexture-function"></a><span data-ttu-id="c4779-103">D3DXComputeIMTFromTexture 函式</span><span class="sxs-lookup"><span data-stu-id="c4779-103">D3DXComputeIMTFromTexture function</span></span>

<span data-ttu-id="c4779-104">從對應至網格的材質計算每個三角形的 IMT，以選擇性地當做 D3DX [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)函式的輸入使用。</span><span class="sxs-lookup"><span data-stu-id="c4779-104">Calculates per-triangle IMT's from a texture mapped onto a mesh, to be used optionally as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4779-105">語法</span><span class="sxs-lookup"><span data-stu-id="c4779-105">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromTexture(
  _In_  LPD3DXMESH         pMesh,
  _In_  LPDIRECT3DTEXTURE9 pTexture,
  _In_  DWORD              dwTextureIndex,
  _In_  DWORD              dwOptions,
        LPD3DXUVATLASCB    pStatusCallback,
        LPVOID             pUserContext,
  _Out_ LPD3DXBUFFER       *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="c4779-106">參數</span><span class="sxs-lookup"><span data-stu-id="c4779-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4779-107">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4779-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4779-108">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="c4779-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="c4779-109">輸入網格 (的指標，請參閱 [**ID3DXMesh**](id3dxmesh.md)) ，其中包含用來計算 IMT 的物件幾何。</span><span class="sxs-lookup"><span data-stu-id="c4779-109">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="c4779-110">*pTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4779-110">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4779-111">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="c4779-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="c4779-112">紋理的指標 (查看對應至網格的 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) 。</span><span class="sxs-lookup"><span data-stu-id="c4779-112">A pointer to the texture (see [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) that is mapped to the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c4779-113">*dwTextureIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4779-113">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4779-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4779-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4779-115">以零為基礎的材質座標索引，識別要使用的材質座標集。</span><span class="sxs-lookup"><span data-stu-id="c4779-115">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="c4779-116">*>dwoptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4779-116">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4779-117">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4779-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4779-118">材質換行選項。</span><span class="sxs-lookup"><span data-stu-id="c4779-118">Texture wrap options.</span></span> <span data-ttu-id="c4779-119">這是一或多個 [**D3DXIMT 旗標**](./d3dximt-flags.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="c4779-119">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4779-120">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="c4779-120">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="c4779-121">類型： **[LPD3DXU加值稅LASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="c4779-121">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="c4779-122">回呼函式的指標，可監視 IMT 計算進度。</span><span class="sxs-lookup"><span data-stu-id="c4779-122">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="c4779-123">*pUserCoNtext*</span><span class="sxs-lookup"><span data-stu-id="c4779-123">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="c4779-124">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4779-124">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4779-125">使用者自訂變數的指標，該變數會傳遞至狀態回呼函數。</span><span class="sxs-lookup"><span data-stu-id="c4779-125">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="c4779-126">通常由應用程式用來傳遞資料結構的指標，以提供回呼函數的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="c4779-126">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="c4779-127">*ppIMTData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c4779-127">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4779-128">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c4779-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c4779-129">緩衝區的指標 (查看包含所傳回 IMT 陣列的 [**ID3DXBuffer**](id3dxbuffer.md)) 。</span><span class="sxs-lookup"><span data-stu-id="c4779-129">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="c4779-130">您可以提供此陣列作為 D3DX [UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) 函式的輸入，來排列材質參數化中材質配置的優先順序。</span><span class="sxs-lookup"><span data-stu-id="c4779-130">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4779-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4779-131">Return value</span></span>

<span data-ttu-id="c4779-132">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4779-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4779-133">如果函式成功，則傳回值為「D3D 正常」， \_ 否則值為 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="c4779-133">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4779-134">備註</span><span class="sxs-lookup"><span data-stu-id="c4779-134">Remarks</span></span>

<span data-ttu-id="c4779-135">如果紋理對應到網格的表面，演算法就會計算每個臉部的 IMT。</span><span class="sxs-lookup"><span data-stu-id="c4779-135">Given a texture that maps over the surface of the mesh, the algorithm computes the IMT for each face.</span></span> <span data-ttu-id="c4779-136">當參數化 UVAtlas 函式時，這會導致包含較低頻率信號資料的三角形，在最終紋理塔中佔用較少的空間。</span><span class="sxs-lookup"><span data-stu-id="c4779-136">This will cause triangles containing lower-frequency signal data to take up less space in the final texture atlas when parameterized with the UVAtlas functions.</span></span> <span data-ttu-id="c4779-137">紋理會假設是透過網格 bilinearly 來插入。</span><span class="sxs-lookup"><span data-stu-id="c4779-137">The texture is assumed to be interpolated over the mesh bilinearly.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4779-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4779-138">Requirements</span></span>



| <span data-ttu-id="c4779-139">需求</span><span class="sxs-lookup"><span data-stu-id="c4779-139">Requirement</span></span> | <span data-ttu-id="c4779-140">值</span><span class="sxs-lookup"><span data-stu-id="c4779-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4779-141">標頭</span><span class="sxs-lookup"><span data-stu-id="c4779-141">Header</span></span><br/>  | <dl> <span data-ttu-id="c4779-142"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4779-142"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c4779-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="c4779-143">Library</span></span><br/> | <dl> <span data-ttu-id="c4779-144"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4779-144"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c4779-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4779-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4779-146">UVAtlas 函式</span><span class="sxs-lookup"><span data-stu-id="c4779-146">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="c4779-147">使用 UVAtlas (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="c4779-147">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
