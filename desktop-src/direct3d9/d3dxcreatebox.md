---
description: 使用左手座標系統來建立包含軸對齊方塊的網格。
ms.assetid: 396ef0f7-65d5-46f9-9b97-e6471f2fb5fe
title: 'D3DXCreateBox 函式 (D3dx9shape) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBox
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 187c389dd2d90b4457237540026a63edc4ab4f4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986083"
---
# <a name="d3dxcreatebox-function"></a><span data-ttu-id="e2ff5-103">D3DXCreateBox 函式</span><span class="sxs-lookup"><span data-stu-id="e2ff5-103">D3DXCreateBox function</span></span>

<span data-ttu-id="e2ff5-104">使用左手座標系統來建立包含軸對齊方塊的網格。</span><span class="sxs-lookup"><span data-stu-id="e2ff5-104">Uses a left-handed coordinate system to create a mesh containing an axis-aligned box.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2ff5-105">語法</span><span class="sxs-lookup"><span data-stu-id="e2ff5-105">Syntax</span></span>


```C++
HRESULT D3DXCreateBox(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Width,
  _In_  FLOAT             Height,
  _In_  FLOAT             Depth,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="e2ff5-106">參數</span><span class="sxs-lookup"><span data-stu-id="e2ff5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2ff5-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2ff5-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ff5-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e2ff5-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e2ff5-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表與所建立之 box 網格相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="e2ff5-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created box mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e2ff5-110">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2ff5-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ff5-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2ff5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2ff5-112">方塊的寬度，沿著 X 軸。</span><span class="sxs-lookup"><span data-stu-id="e2ff5-112">Width of the box, along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="e2ff5-113">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2ff5-113">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ff5-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2ff5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2ff5-115">方塊的高度，沿著 y 軸。</span><span class="sxs-lookup"><span data-stu-id="e2ff5-115">Height of the box, along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="e2ff5-116">*深度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2ff5-116">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ff5-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2ff5-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2ff5-118">沿著 Z 軸的方塊深度。</span><span class="sxs-lookup"><span data-stu-id="e2ff5-118">Depth of the box, along the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="e2ff5-119">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e2ff5-119">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ff5-120">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2ff5-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="e2ff5-121">輸出圖形（ [**ID3DXMesh**](id3dxmesh.md) 介面）指標的位址。</span><span class="sxs-lookup"><span data-stu-id="e2ff5-121">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e2ff5-122">*ppAdjacency* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e2ff5-122">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2ff5-123">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e2ff5-123">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e2ff5-124">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="e2ff5-124">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="e2ff5-125">當方法傳回時，此參數會填入三個 Dword 的陣列，每個臉部會針對網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="e2ff5-125">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="e2ff5-126">您可以指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="e2ff5-126">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2ff5-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2ff5-127">Return value</span></span>

<span data-ttu-id="e2ff5-128">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e2ff5-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e2ff5-129">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="e2ff5-129">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e2ff5-130">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="e2ff5-130">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2ff5-131">備註</span><span class="sxs-lookup"><span data-stu-id="e2ff5-131">Remarks</span></span>

<span data-ttu-id="e2ff5-132">所建立的方塊會在原點中央。</span><span class="sxs-lookup"><span data-stu-id="e2ff5-132">The created box is centered at the origin.</span></span>

<span data-ttu-id="e2ff5-133">此函式會使用 D3DXMESH \_ MANAGED 建立選項建立網格，並 [D3DFVF \_ XYZ \| D3DFVF \_ 標準](d3dfvf.md) 的彈性頂點格式 (FVF) 。</span><span class="sxs-lookup"><span data-stu-id="e2ff5-133">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2ff5-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2ff5-134">Requirements</span></span>



| <span data-ttu-id="e2ff5-135">需求</span><span class="sxs-lookup"><span data-stu-id="e2ff5-135">Requirement</span></span> | <span data-ttu-id="e2ff5-136">值</span><span class="sxs-lookup"><span data-stu-id="e2ff5-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2ff5-137">標頭</span><span class="sxs-lookup"><span data-stu-id="e2ff5-137">Header</span></span><br/>  | <dl> <span data-ttu-id="e2ff5-138"><dt>D3dx9shape。h</dt></span><span class="sxs-lookup"><span data-stu-id="e2ff5-138"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="e2ff5-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="e2ff5-139">Library</span></span><br/> | <dl> <span data-ttu-id="e2ff5-140"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2ff5-140"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e2ff5-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2ff5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2ff5-142">圖形繪圖函數</span><span class="sxs-lookup"><span data-stu-id="e2ff5-142">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
