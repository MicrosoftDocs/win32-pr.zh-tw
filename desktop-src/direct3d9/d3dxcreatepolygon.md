---
description: 使用左方座標系統建立包含單面多邊形的網格。
ms.assetid: f3313f55-3e60-4440-8bea-d2886b636c9a
title: 'D3DXCreatePolygon 函式 (D3dx9shape) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePolygon
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94a7e48f512d25ca53d1f3ff80889a013e2ecdcb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035354"
---
# <a name="d3dxcreatepolygon-function"></a><span data-ttu-id="99354-103">D3DXCreatePolygon 函式</span><span class="sxs-lookup"><span data-stu-id="99354-103">D3DXCreatePolygon function</span></span>

<span data-ttu-id="99354-104">使用左方座標系統建立包含單面多邊形的網格。</span><span class="sxs-lookup"><span data-stu-id="99354-104">Uses a left-handed coordinate system to create a mesh containing an n-sided polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="99354-105">語法</span><span class="sxs-lookup"><span data-stu-id="99354-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePolygon(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Length,
  _In_  UINT              Sides,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="99354-106">參數</span><span class="sxs-lookup"><span data-stu-id="99354-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99354-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99354-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99354-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="99354-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="99354-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表與建立的多邊形網格相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="99354-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created polygon mesh.</span></span>

</dd> <dt>

<span data-ttu-id="99354-110">*長度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99354-110">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99354-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99354-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99354-112">每一側的長度。</span><span class="sxs-lookup"><span data-stu-id="99354-112">Length of each side.</span></span>

</dd> <dt>

<span data-ttu-id="99354-113">*邊* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99354-113">*Sides* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99354-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99354-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99354-115">多邊形的邊數。</span><span class="sxs-lookup"><span data-stu-id="99354-115">Number of sides for the polygon.</span></span> <span data-ttu-id="99354-116">值必須大於或等於3。</span><span class="sxs-lookup"><span data-stu-id="99354-116">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="99354-117">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="99354-117">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99354-118">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="99354-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="99354-119">輸出圖形（ [**ID3DXMesh**](id3dxmesh.md) 介面）指標的位址。</span><span class="sxs-lookup"><span data-stu-id="99354-119">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="99354-120">*ppAdjacency* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="99354-120">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99354-121">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="99354-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="99354-122">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="99354-122">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="99354-123">當方法傳回時，此參數會填入三個 Dword 的陣列，每個臉部會針對網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="99354-123">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="99354-124">您可以指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="99354-124">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99354-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="99354-125">Return value</span></span>

<span data-ttu-id="99354-126">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99354-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99354-127">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="99354-127">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="99354-128">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="99354-128">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="99354-129">備註</span><span class="sxs-lookup"><span data-stu-id="99354-129">Remarks</span></span>

<span data-ttu-id="99354-130">建立的多邊形會以原點為中心。</span><span class="sxs-lookup"><span data-stu-id="99354-130">The created polygon is centered at the origin.</span></span>

<span data-ttu-id="99354-131">此函式會使用 D3DXMESH \_ MANAGED 建立選項建立網格，並 [D3DFVF \_ XYZ \| D3DFVF \_ 標準](d3dfvf.md) 的彈性頂點格式 (FVF) 。</span><span class="sxs-lookup"><span data-stu-id="99354-131">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="99354-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="99354-132">Requirements</span></span>



| <span data-ttu-id="99354-133">需求</span><span class="sxs-lookup"><span data-stu-id="99354-133">Requirement</span></span> | <span data-ttu-id="99354-134">值</span><span class="sxs-lookup"><span data-stu-id="99354-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99354-135">標頭</span><span class="sxs-lookup"><span data-stu-id="99354-135">Header</span></span><br/>  | <dl> <span data-ttu-id="99354-136"><dt>D3dx9shape。h</dt></span><span class="sxs-lookup"><span data-stu-id="99354-136"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="99354-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="99354-137">Library</span></span><br/> | <dl> <span data-ttu-id="99354-138"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="99354-138"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="99354-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99354-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99354-140">圖形繪圖函數</span><span class="sxs-lookup"><span data-stu-id="99354-140">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
