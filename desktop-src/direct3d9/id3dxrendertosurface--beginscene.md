---
description: 開始場景。
ms.assetid: 8125c592-b985-42f7-8644-59ba93a1c517
title: 'ID3DXRenderToSurface：： BeginScene 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.BeginScene
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5aa2229e88123cc1d52f65f1edf032c46f819229
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982908"
---
# <a name="id3dxrendertosurfacebeginscene-method"></a><span data-ttu-id="961a1-103">ID3DXRenderToSurface：： BeginScene 方法</span><span class="sxs-lookup"><span data-stu-id="961a1-103">ID3DXRenderToSurface::BeginScene method</span></span>

<span data-ttu-id="961a1-104">開始場景。</span><span class="sxs-lookup"><span data-stu-id="961a1-104">Begins a scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="961a1-105">語法</span><span class="sxs-lookup"><span data-stu-id="961a1-105">Syntax</span></span>


```C++
HRESULT BeginScene(
  [in]       LPDIRECT3DSURFACE9 pSurface,
  [in] const D3DVIEWPORT9       *pViewport
);
```



## <a name="parameters"></a><span data-ttu-id="961a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="961a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="961a1-107">*pSurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="961a1-107">*pSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="961a1-108">類型： **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="961a1-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="961a1-109">[**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)介面的指標，表示呈現介面。</span><span class="sxs-lookup"><span data-stu-id="961a1-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the render surface.</span></span>

</dd> <dt>

<span data-ttu-id="961a1-110">*pViewport* \[在\]</span><span class="sxs-lookup"><span data-stu-id="961a1-110">*pViewport* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="961a1-111">Type： **Const [**D3DVIEWPORT9**](d3dviewport9.md) \***</span><span class="sxs-lookup"><span data-stu-id="961a1-111">Type: **const [**D3DVIEWPORT9**](d3dviewport9.md)\***</span></span>

<span data-ttu-id="961a1-112">[**D3DVIEWPORT9**](d3dviewport9.md)結構的指標，描述場景的區。</span><span class="sxs-lookup"><span data-stu-id="961a1-112">Pointer to a [**D3DVIEWPORT9**](d3dviewport9.md) structure, describing the viewport for the scene.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="961a1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="961a1-113">Return value</span></span>

<span data-ttu-id="961a1-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="961a1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="961a1-115">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="961a1-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="961a1-116">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL。D3DERR \_ OUTOFVIDEOMEMORY D3DXERR \_ INVALIDDATA E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="961a1-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL.D3DERR\_OUTOFVIDEOMEMORY D3DXERR\_INVALIDDATA E\_OUTOFMEMORY</span></span>

## <a name="requirements"></a><span data-ttu-id="961a1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="961a1-117">Requirements</span></span>



| <span data-ttu-id="961a1-118">需求</span><span class="sxs-lookup"><span data-stu-id="961a1-118">Requirement</span></span> | <span data-ttu-id="961a1-119">值</span><span class="sxs-lookup"><span data-stu-id="961a1-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="961a1-120">標頭</span><span class="sxs-lookup"><span data-stu-id="961a1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="961a1-121"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="961a1-121"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="961a1-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="961a1-122">Library</span></span><br/> | <dl> <span data-ttu-id="961a1-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="961a1-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="961a1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="961a1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="961a1-125">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="961a1-125">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> <dt>

[<span data-ttu-id="961a1-126">**ID3DXRenderToSurface::EndScene**</span><span class="sxs-lookup"><span data-stu-id="961a1-126">**ID3DXRenderToSurface::EndScene**</span></span>](id3dxrendertosurface--endscene.md)
</dt> </dl>

 

 
