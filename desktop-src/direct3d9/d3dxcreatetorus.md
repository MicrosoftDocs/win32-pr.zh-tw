---
description: 使用左手座標系統建立包含圓環的網格。
ms.assetid: 68df7650-8a87-4762-8b57-5704c419b0d7
title: 'D3DXCreateTorus 函式 (D3dx9shape) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTorus
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 384950ca1f00d0115135cf9ae36a2883ec5470e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196264"
---
# <a name="d3dxcreatetorus-function"></a><span data-ttu-id="96f2b-103">D3DXCreateTorus 函式</span><span class="sxs-lookup"><span data-stu-id="96f2b-103">D3DXCreateTorus function</span></span>

<span data-ttu-id="96f2b-104">使用左手座標系統建立包含圓環的網格。</span><span class="sxs-lookup"><span data-stu-id="96f2b-104">Uses a left-handed coordinate system to create a mesh containing a torus.</span></span>

## <a name="syntax"></a><span data-ttu-id="96f2b-105">語法</span><span class="sxs-lookup"><span data-stu-id="96f2b-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTorus(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             InnerRadius,
  _In_  FLOAT             OuterRadius,
  _In_  UINT              Sides,
  _In_  UINT              Rings,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="96f2b-106">參數</span><span class="sxs-lookup"><span data-stu-id="96f2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96f2b-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96f2b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96f2b-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="96f2b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="96f2b-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與所建立環圓點網格相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="96f2b-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created torus mesh.</span></span>

</dd> <dt>

<span data-ttu-id="96f2b-110">*InnerRadius* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96f2b-110">*InnerRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96f2b-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96f2b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="96f2b-112">環圓環的內部半徑。</span><span class="sxs-lookup"><span data-stu-id="96f2b-112">Inner-radius of the torus.</span></span> <span data-ttu-id="96f2b-113">值應大於或等於 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="96f2b-113">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="96f2b-114">*OuterRadius* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96f2b-114">*OuterRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96f2b-115">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96f2b-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="96f2b-116">圓角環的外部半徑。</span><span class="sxs-lookup"><span data-stu-id="96f2b-116">Outer-radius of the torus.</span></span> <span data-ttu-id="96f2b-117">值應大於或等於 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="96f2b-117">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="96f2b-118">*邊* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96f2b-118">*Sides* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96f2b-119">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96f2b-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="96f2b-120">跨區段的邊數。</span><span class="sxs-lookup"><span data-stu-id="96f2b-120">Number of sides in a cross-section.</span></span> <span data-ttu-id="96f2b-121">值必須大於或等於3。</span><span class="sxs-lookup"><span data-stu-id="96f2b-121">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="96f2b-122">*環形* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96f2b-122">*Rings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96f2b-123">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96f2b-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="96f2b-124">組成圓環圈的環形數。</span><span class="sxs-lookup"><span data-stu-id="96f2b-124">Number of rings making up the torus.</span></span> <span data-ttu-id="96f2b-125">值必須大於或等於3。</span><span class="sxs-lookup"><span data-stu-id="96f2b-125">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="96f2b-126">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="96f2b-126">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96f2b-127">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="96f2b-127">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="96f2b-128">輸出圖形（ [**ID3DXMesh**](id3dxmesh.md) 介面）指標的位址。</span><span class="sxs-lookup"><span data-stu-id="96f2b-128">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="96f2b-129">*ppAdjacency* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="96f2b-129">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96f2b-130">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="96f2b-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="96f2b-131">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="96f2b-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="96f2b-132">當方法傳回時，此參數會填入三個 Dword 的陣列，每個臉部會針對網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="96f2b-132">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="96f2b-133">您可以指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="96f2b-133">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96f2b-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="96f2b-134">Return value</span></span>

<span data-ttu-id="96f2b-135">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="96f2b-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="96f2b-136">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="96f2b-136">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="96f2b-137">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="96f2b-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="96f2b-138">備註</span><span class="sxs-lookup"><span data-stu-id="96f2b-138">Remarks</span></span>

<span data-ttu-id="96f2b-139">建立的圓角會置中，並以 Z 軸對齊其軸。</span><span class="sxs-lookup"><span data-stu-id="96f2b-139">The created torus is centered at the origin, and its axis is aligned with the z-axis.</span></span> <span data-ttu-id="96f2b-140">圓環的內部半徑是 (次要半徑) 的交叉區段半徑，而圓環的外部半徑是中央孔的半徑。</span><span class="sxs-lookup"><span data-stu-id="96f2b-140">The inner radius of the torus is the radius of the cross-section (the minor radius), and the outer radius of the torus is the radius of the central hole.</span></span>

<span data-ttu-id="96f2b-141">此函式會傳回可供應用程式用來繪製或操作的網格。</span><span class="sxs-lookup"><span data-stu-id="96f2b-141">This function returns a mesh that can be used later for drawing or manipulation by the application.</span></span>

<span data-ttu-id="96f2b-142">此函式會使用 D3DXMESH \_ MANAGED 建立選項建立網格，並 [D3DFVF \_ XYZ \| D3DFVF \_ 標準](d3dfvf.md) 的彈性頂點格式 (FVF) 。</span><span class="sxs-lookup"><span data-stu-id="96f2b-142">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="96f2b-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="96f2b-143">Requirements</span></span>



| <span data-ttu-id="96f2b-144">需求</span><span class="sxs-lookup"><span data-stu-id="96f2b-144">Requirement</span></span> | <span data-ttu-id="96f2b-145">值</span><span class="sxs-lookup"><span data-stu-id="96f2b-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96f2b-146">標頭</span><span class="sxs-lookup"><span data-stu-id="96f2b-146">Header</span></span><br/>  | <dl> <span data-ttu-id="96f2b-147"><dt>D3dx9shape。h</dt></span><span class="sxs-lookup"><span data-stu-id="96f2b-147"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="96f2b-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="96f2b-148">Library</span></span><br/> | <dl> <span data-ttu-id="96f2b-149"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="96f2b-149"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="96f2b-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96f2b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96f2b-151">圖形繪圖函數</span><span class="sxs-lookup"><span data-stu-id="96f2b-151">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
