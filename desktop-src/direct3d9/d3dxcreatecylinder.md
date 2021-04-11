---
description: 使用左手座標系統建立包含圓柱的網格。
ms.assetid: 54b8a59e-d13f-44cb-84c0-f63c7b1ffb1b
title: 'D3DXCreateCylinder 函式 (D3dx9shape) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCylinder
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec97755d45b21a85e1a73bbcd2214ee4c1e2358f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696671"
---
# <a name="d3dxcreatecylinder-function"></a><span data-ttu-id="539c3-103">D3DXCreateCylinder 函式</span><span class="sxs-lookup"><span data-stu-id="539c3-103">D3DXCreateCylinder function</span></span>

<span data-ttu-id="539c3-104">使用左手座標系統建立包含圓柱的網格。</span><span class="sxs-lookup"><span data-stu-id="539c3-104">Uses a left-handed coordinate system to create a mesh containing a cylinder.</span></span>

## <a name="syntax"></a><span data-ttu-id="539c3-105">語法</span><span class="sxs-lookup"><span data-stu-id="539c3-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCylinder(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius1,
  _In_  FLOAT             Radius2,
  _In_  FLOAT             Length,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="539c3-106">參數</span><span class="sxs-lookup"><span data-stu-id="539c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="539c3-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="539c3-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="539c3-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="539c3-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="539c3-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表與所建立之圓柱網格相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="539c3-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created cylinder mesh.</span></span>

</dd> <dt>

<span data-ttu-id="539c3-110">*Radius1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="539c3-110">*Radius1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="539c3-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="539c3-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="539c3-112">以負 Z 結尾的半徑。</span><span class="sxs-lookup"><span data-stu-id="539c3-112">Radius at the negative Z end.</span></span> <span data-ttu-id="539c3-113">值應大於或等於 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="539c3-113">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="539c3-114">*Radius2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="539c3-114">*Radius2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="539c3-115">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="539c3-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="539c3-116">正 Z 端的半徑。</span><span class="sxs-lookup"><span data-stu-id="539c3-116">Radius at the positive Z end.</span></span> <span data-ttu-id="539c3-117">值應大於或等於 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="539c3-117">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="539c3-118">*長度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="539c3-118">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="539c3-119">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="539c3-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="539c3-120">沿著 Z 軸的圓柱長度。</span><span class="sxs-lookup"><span data-stu-id="539c3-120">Length of the cylinder along the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="539c3-121">配量 \[在\]</span><span class="sxs-lookup"><span data-stu-id="539c3-121">*Slices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="539c3-122">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="539c3-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="539c3-123">主要軸的磁區數目。</span><span class="sxs-lookup"><span data-stu-id="539c3-123">Number of slices about the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="539c3-124">*堆疊* \[在\]</span><span class="sxs-lookup"><span data-stu-id="539c3-124">*Stacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="539c3-125">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="539c3-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="539c3-126">沿著主要軸的堆疊數目。</span><span class="sxs-lookup"><span data-stu-id="539c3-126">Number of stacks along the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="539c3-127">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="539c3-127">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="539c3-128">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="539c3-128">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="539c3-129">輸出圖形（ [**ID3DXMesh**](id3dxmesh.md) 介面）指標的位址。</span><span class="sxs-lookup"><span data-stu-id="539c3-129">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="539c3-130">*ppAdjacency* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="539c3-130">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="539c3-131">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="539c3-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="539c3-132">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="539c3-132">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="539c3-133">當方法傳回時，此參數會填入三個 Dword 的陣列，每個臉部會針對網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="539c3-133">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="539c3-134">您可以指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="539c3-134">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="539c3-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="539c3-135">Return value</span></span>

<span data-ttu-id="539c3-136">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="539c3-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="539c3-137">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="539c3-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="539c3-138">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="539c3-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="539c3-139">備註</span><span class="sxs-lookup"><span data-stu-id="539c3-139">Remarks</span></span>

<span data-ttu-id="539c3-140">建立的圓柱會以原點為中心，而且其軸會對齊 Z 軸。</span><span class="sxs-lookup"><span data-stu-id="539c3-140">The created cylinder is centered at the origin, and its axis is aligned with the z-axis.</span></span>

<span data-ttu-id="539c3-141">此函式會使用 D3DXMESH \_ MANAGED 建立選項建立網格，並 [D3DFVF \_ XYZ \| D3DFVF \_ 標準](d3dfvf.md) 的彈性頂點格式 (FVF) 。</span><span class="sxs-lookup"><span data-stu-id="539c3-141">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="539c3-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="539c3-142">Requirements</span></span>



| <span data-ttu-id="539c3-143">需求</span><span class="sxs-lookup"><span data-stu-id="539c3-143">Requirement</span></span> | <span data-ttu-id="539c3-144">值</span><span class="sxs-lookup"><span data-stu-id="539c3-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="539c3-145">標頭</span><span class="sxs-lookup"><span data-stu-id="539c3-145">Header</span></span><br/>  | <dl> <span data-ttu-id="539c3-146"><dt>D3dx9shape。h</dt></span><span class="sxs-lookup"><span data-stu-id="539c3-146"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="539c3-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="539c3-147">Library</span></span><br/> | <dl> <span data-ttu-id="539c3-148"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="539c3-148"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="539c3-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="539c3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="539c3-150">圖形繪圖函數</span><span class="sxs-lookup"><span data-stu-id="539c3-150">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
