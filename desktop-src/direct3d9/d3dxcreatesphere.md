---
description: 使用左手座標系統建立包含球體的網格。
ms.assetid: d3198805-9435-4849-892d-ec98dc2221d2
title: 'D3DXCreateSphere 函式 (D3dx9shape) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56ac6b8e8cc2195e2176e505cf430ea33b6b6ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196268"
---
# <a name="d3dxcreatesphere-function"></a><span data-ttu-id="82f91-103">D3DXCreateSphere 函式</span><span class="sxs-lookup"><span data-stu-id="82f91-103">D3DXCreateSphere function</span></span>

<span data-ttu-id="82f91-104">使用左手座標系統建立包含球體的網格。</span><span class="sxs-lookup"><span data-stu-id="82f91-104">Uses a left-handed coordinate system to create a mesh containing a sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="82f91-105">語法</span><span class="sxs-lookup"><span data-stu-id="82f91-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSphere(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="82f91-106">參數</span><span class="sxs-lookup"><span data-stu-id="82f91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82f91-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82f91-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82f91-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="82f91-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="82f91-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表與所建立球體網格相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="82f91-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created sphere mesh.</span></span>

</dd> <dt>

<span data-ttu-id="82f91-110">*Radius* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82f91-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82f91-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82f91-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82f91-112">球體的半徑。</span><span class="sxs-lookup"><span data-stu-id="82f91-112">Radius of the sphere.</span></span> <span data-ttu-id="82f91-113">此值應大於或等於 0.0 f。</span><span class="sxs-lookup"><span data-stu-id="82f91-113">This value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="82f91-114">配量 \[在\]</span><span class="sxs-lookup"><span data-stu-id="82f91-114">*Slices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82f91-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82f91-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82f91-116">主要軸的磁區數目。</span><span class="sxs-lookup"><span data-stu-id="82f91-116">Number of slices about the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="82f91-117">*堆疊* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82f91-117">*Stacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82f91-118">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82f91-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82f91-119">沿著主要軸的堆疊數目。</span><span class="sxs-lookup"><span data-stu-id="82f91-119">Number of stacks along the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="82f91-120">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="82f91-120">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82f91-121">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="82f91-121">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="82f91-122">輸出圖形（ [**ID3DXMesh**](id3dxmesh.md) 介面）指標的位址。</span><span class="sxs-lookup"><span data-stu-id="82f91-122">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="82f91-123">*ppAdjacency* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="82f91-123">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82f91-124">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="82f91-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="82f91-125">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="82f91-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="82f91-126">當方法傳回時，此參數會填入三個 Dword 的陣列，每個臉部會針對網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="82f91-126">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="82f91-127">您可以指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="82f91-127">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82f91-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="82f91-128">Return value</span></span>

<span data-ttu-id="82f91-129">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="82f91-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="82f91-130">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="82f91-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="82f91-131">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="82f91-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="82f91-132">備註</span><span class="sxs-lookup"><span data-stu-id="82f91-132">Remarks</span></span>

<span data-ttu-id="82f91-133">建立的球體會以原點為中心，而且其軸會對齊 Z 軸。</span><span class="sxs-lookup"><span data-stu-id="82f91-133">The created sphere is centered at the origin, and its axis is aligned with the z-axis.</span></span>

<span data-ttu-id="82f91-134">此函式會使用 D3DXMESH \_ MANAGED 建立選項建立網格，並 [D3DFVF \_ XYZ \| D3DFVF \_ 標準](d3dfvf.md) 的彈性頂點格式 (FVF) 。</span><span class="sxs-lookup"><span data-stu-id="82f91-134">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="82f91-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="82f91-135">Requirements</span></span>



| <span data-ttu-id="82f91-136">需求</span><span class="sxs-lookup"><span data-stu-id="82f91-136">Requirement</span></span> | <span data-ttu-id="82f91-137">值</span><span class="sxs-lookup"><span data-stu-id="82f91-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82f91-138">標頭</span><span class="sxs-lookup"><span data-stu-id="82f91-138">Header</span></span><br/>  | <dl> <span data-ttu-id="82f91-139"><dt>D3dx9shape。h</dt></span><span class="sxs-lookup"><span data-stu-id="82f91-139"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="82f91-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="82f91-140">Library</span></span><br/> | <dl> <span data-ttu-id="82f91-141"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="82f91-141"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="82f91-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82f91-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82f91-143">圖形繪圖函數</span><span class="sxs-lookup"><span data-stu-id="82f91-143">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
