---
description: 使用左手座標系統建立包含茶壺的網格。
ms.assetid: c002d6d4-1829-4293-9a86-d8560d6ec0e9
title: 'D3DXCreateTeapot 函式 (D3dx9shape) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTeapot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 13f5ed44bdc31958729209f01183eba409298fcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196267"
---
# <a name="d3dxcreateteapot-function"></a><span data-ttu-id="6d740-103">D3DXCreateTeapot 函式</span><span class="sxs-lookup"><span data-stu-id="6d740-103">D3DXCreateTeapot function</span></span>

<span data-ttu-id="6d740-104">使用左手座標系統建立包含茶壺的網格。</span><span class="sxs-lookup"><span data-stu-id="6d740-104">Uses a left-handed coordinate system to create a mesh containing a teapot.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d740-105">語法</span><span class="sxs-lookup"><span data-stu-id="6d740-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTeapot(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="6d740-106">參數</span><span class="sxs-lookup"><span data-stu-id="6d740-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d740-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6d740-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d740-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6d740-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6d740-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表與所建立之茶壺網格相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="6d740-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created teapot mesh.</span></span>

</dd> <dt>

<span data-ttu-id="6d740-110">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6d740-110">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d740-111">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="6d740-111">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="6d740-112">輸出圖形（ [**ID3DXMesh**](id3dxmesh.md) 介面）指標的位址。</span><span class="sxs-lookup"><span data-stu-id="6d740-112">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="6d740-113">*ppAdjacency* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6d740-113">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d740-114">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6d740-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6d740-115">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="6d740-115">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="6d740-116">當方法傳回時，此參數會填入三個 Dword 的陣列，每個臉部會針對網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="6d740-116">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="6d740-117">您可以指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="6d740-117">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d740-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d740-118">Return value</span></span>

<span data-ttu-id="6d740-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d740-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d740-120">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="6d740-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6d740-121">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="6d740-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d740-122">備註</span><span class="sxs-lookup"><span data-stu-id="6d740-122">Remarks</span></span>

<span data-ttu-id="6d740-123">此函式會使用 D3DXMESH \_ MANAGED 建立選項建立網格，並 [D3DFVF \_ XYZ \| D3DFVF \_ 標準](d3dfvf.md) 的彈性頂點格式 (FVF) 。</span><span class="sxs-lookup"><span data-stu-id="6d740-123">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d740-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d740-124">Requirements</span></span>



| <span data-ttu-id="6d740-125">需求</span><span class="sxs-lookup"><span data-stu-id="6d740-125">Requirement</span></span> | <span data-ttu-id="6d740-126">值</span><span class="sxs-lookup"><span data-stu-id="6d740-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d740-127">標頭</span><span class="sxs-lookup"><span data-stu-id="6d740-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6d740-128"><dt>D3dx9shape。h</dt></span><span class="sxs-lookup"><span data-stu-id="6d740-128"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="6d740-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="6d740-129">Library</span></span><br/> | <dl> <span data-ttu-id="6d740-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d740-130"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6d740-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d740-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d740-132">圖形繪圖函數</span><span class="sxs-lookup"><span data-stu-id="6d740-132">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
