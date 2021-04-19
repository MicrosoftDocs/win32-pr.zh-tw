---
description: 建立呈現介面。
ms.assetid: 35e0007e-c405-46e1-a52b-625adc84732b
title: 'D3DXCreateRenderToSurface 函式 (D3dx9core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fc64cbc65d30838db2105e0458d3553247f1ab1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998207"
---
# <a name="d3dxcreaterendertosurface-function"></a><span data-ttu-id="cd2fe-103">D3DXCreateRenderToSurface 函式</span><span class="sxs-lookup"><span data-stu-id="cd2fe-103">D3DXCreateRenderToSurface function</span></span>

<span data-ttu-id="cd2fe-104">建立呈現介面。</span><span class="sxs-lookup"><span data-stu-id="cd2fe-104">Creates a render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd2fe-105">語法</span><span class="sxs-lookup"><span data-stu-id="cd2fe-105">Syntax</span></span>


```C++
HRESULT D3DXCreateRenderToSurface(
  _In_  LPDIRECT3DDEVICE9     pDevice,
  _In_  UINT                  Width,
  _In_  UINT                  Height,
  _In_  D3DFORMAT             Format,
  _In_  BOOL                  DepthStencil,
  _In_  D3DFORMAT             DepthStencilFormat,
  _Out_ LPD3DXRENDERTOSURFACE *ppRenderToSurface
);
```



## <a name="parameters"></a><span data-ttu-id="cd2fe-106">參數</span><span class="sxs-lookup"><span data-stu-id="cd2fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd2fe-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd2fe-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2fe-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="cd2fe-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="cd2fe-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，與呈現介面相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="cd2fe-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="cd2fe-110">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd2fe-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2fe-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd2fe-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd2fe-112">呈現介面的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="cd2fe-112">Width of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="cd2fe-113">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd2fe-113">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2fe-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd2fe-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd2fe-115">轉譯介面的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="cd2fe-115">Height of the render surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="cd2fe-116">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd2fe-116">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2fe-117">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="cd2fe-117">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="cd2fe-118">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述呈現介面的像素格式。</span><span class="sxs-lookup"><span data-stu-id="cd2fe-118">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the pixel format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="cd2fe-119">*DepthStencil* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd2fe-119">*DepthStencil* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2fe-120">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cd2fe-120">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cd2fe-121">若 **為 TRUE**，表示呈現介面支援深度樣板表面。</span><span class="sxs-lookup"><span data-stu-id="cd2fe-121">If **TRUE**, the render surface supports a depth-stencil surface.</span></span> <span data-ttu-id="cd2fe-122">否則，此成員會設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="cd2fe-122">Otherwise, this member is set to **FALSE**.</span></span> <span data-ttu-id="cd2fe-123">此函數會建立新的深度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cd2fe-123">This function will create a new depth buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cd2fe-124">*DepthStencilFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd2fe-124">*DepthStencilFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2fe-125">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="cd2fe-125">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="cd2fe-126">如果 *DepthStencil* 設定為 **TRUE**，這個參數就是 [D3DFORMAT](d3dformat.md) 列舉型別的成員，它會描述呈現介面的深度樣板格式。</span><span class="sxs-lookup"><span data-stu-id="cd2fe-126">If *DepthStencil* is set to **TRUE**, this parameter is a member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the depth-stencil format of the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="cd2fe-127">*ppRenderToSurface* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cd2fe-127">*ppRenderToSurface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd2fe-128">類型： **[ **LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd2fe-128">Type: **[**LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***</span></span>

<span data-ttu-id="cd2fe-129">[**ID3DXRenderToSurface**](id3dxrendertosurface.md)介面指標的位址，表示所建立的呈現介面。</span><span class="sxs-lookup"><span data-stu-id="cd2fe-129">Address of a pointer to an [**ID3DXRenderToSurface**](id3dxrendertosurface.md) interface, representing the created render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd2fe-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd2fe-130">Return value</span></span>

<span data-ttu-id="cd2fe-131">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cd2fe-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cd2fe-132">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="cd2fe-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cd2fe-133">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="cd2fe-133">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd2fe-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd2fe-134">Requirements</span></span>



| <span data-ttu-id="cd2fe-135">需求</span><span class="sxs-lookup"><span data-stu-id="cd2fe-135">Requirement</span></span> | <span data-ttu-id="cd2fe-136">值</span><span class="sxs-lookup"><span data-stu-id="cd2fe-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd2fe-137">標頭</span><span class="sxs-lookup"><span data-stu-id="cd2fe-137">Header</span></span><br/>  | <dl> <span data-ttu-id="cd2fe-138"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="cd2fe-138"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="cd2fe-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="cd2fe-139">Library</span></span><br/> | <dl> <span data-ttu-id="cd2fe-140"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd2fe-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cd2fe-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd2fe-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd2fe-142">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="cd2fe-142">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
