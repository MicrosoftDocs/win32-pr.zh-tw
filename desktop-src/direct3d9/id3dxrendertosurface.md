---
description: ID3DXRenderToSurface 介面可用來將轉譯的程式一般化至表面。
ms.assetid: e9f2ca5e-faa3-45a8-94eb-16f354618e80
title: 'ID3DXRenderToSurface 介面 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 577e729e4e1a510dd24dc981b2b90bdca27dc0f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323307"
---
# <a name="id3dxrendertosurface-interface"></a><span data-ttu-id="bc203-103">ID3DXRenderToSurface 介面</span><span class="sxs-lookup"><span data-stu-id="bc203-103">ID3DXRenderToSurface interface</span></span>

<span data-ttu-id="bc203-104">ID3DXRenderToSurface 介面可用來將轉譯的程式一般化至表面。</span><span class="sxs-lookup"><span data-stu-id="bc203-104">The ID3DXRenderToSurface interface is used to generalize the process of rendering to surfaces.</span></span>

## <a name="members"></a><span data-ttu-id="bc203-105">成員</span><span class="sxs-lookup"><span data-stu-id="bc203-105">Members</span></span>

<span data-ttu-id="bc203-106">**ID3DXRenderToSurface** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="bc203-106">The **ID3DXRenderToSurface** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bc203-107">**ID3DXRenderToSurface** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bc203-107">**ID3DXRenderToSurface** also has these types of members:</span></span>

-   [<span data-ttu-id="bc203-108">方法</span><span class="sxs-lookup"><span data-stu-id="bc203-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bc203-109">方法</span><span class="sxs-lookup"><span data-stu-id="bc203-109">Methods</span></span>

<span data-ttu-id="bc203-110">**ID3DXRenderToSurface** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="bc203-110">The **ID3DXRenderToSurface** interface has these methods.</span></span>



| <span data-ttu-id="bc203-111">方法</span><span class="sxs-lookup"><span data-stu-id="bc203-111">Method</span></span>                                                       | <span data-ttu-id="bc203-112">描述</span><span class="sxs-lookup"><span data-stu-id="bc203-112">Description</span></span>                                                                                                                                                                                     |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc203-113">**BeginScene**</span><span class="sxs-lookup"><span data-stu-id="bc203-113">**BeginScene**</span></span>](id3dxrendertosurface--beginscene.md)       | <span data-ttu-id="bc203-114">開始場景。</span><span class="sxs-lookup"><span data-stu-id="bc203-114">Begins a scene.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="bc203-115">**EndScene**</span><span class="sxs-lookup"><span data-stu-id="bc203-115">**EndScene**</span></span>](id3dxrendertosurface--endscene.md)           | <span data-ttu-id="bc203-116">結束場景。</span><span class="sxs-lookup"><span data-stu-id="bc203-116">Ends a scene.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="bc203-117">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="bc203-117">**GetDesc**</span></span>](id3dxrendertosurface--getdesc.md)             | <span data-ttu-id="bc203-118">捕獲呈現介面的參數。</span><span class="sxs-lookup"><span data-stu-id="bc203-118">Retrieves the parameters of the render surface.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="bc203-119">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="bc203-119">**GetDevice**</span></span>](id3dxrendertosurface--getdevice.md)         | <span data-ttu-id="bc203-120">抓取與呈現介面相關聯的 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="bc203-120">Retrieves the Direct3D device associated with the render surface.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="bc203-121">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="bc203-121">**OnLostDevice**</span></span>](id3dxrendertosurface--onlostdevice.md)   | <span data-ttu-id="bc203-122">您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。</span><span class="sxs-lookup"><span data-stu-id="bc203-122">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="bc203-123">只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="bc203-123">This method should be called whenever a device is lost or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="bc203-124">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="bc203-124">**OnResetDevice**</span></span>](id3dxrendertosurface--onresetdevice.md) | <span data-ttu-id="bc203-125">您可以使用這個方法來重新取得資源，並儲存初始狀態。</span><span class="sxs-lookup"><span data-stu-id="bc203-125">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="bc203-126">備註</span><span class="sxs-lookup"><span data-stu-id="bc203-126">Remarks</span></span>

<span data-ttu-id="bc203-127">您可以使用各種方式來使用介面，包括轉譯目標、螢幕轉譯或轉譯成紋理。</span><span class="sxs-lookup"><span data-stu-id="bc203-127">Surfaces can be used in a variety of ways including render targets, off-screen rendering, or rendering to textures.</span></span>

<span data-ttu-id="bc203-128">您可以使用 [**ID3DXRenderToSurface：： BeginScene**](id3dxrendertosurface--beginscene.md) 方法，透過不同的區隔圖來設定介面，以提供自訂呈現視圖。</span><span class="sxs-lookup"><span data-stu-id="bc203-128">A surface can be configured using a separate viewport using the [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md) method, to provide a custom render view.</span></span> <span data-ttu-id="bc203-129">如果介面不是轉譯目標，則會使用相容的呈現目標，並將結果複製到場景結尾的介面。</span><span class="sxs-lookup"><span data-stu-id="bc203-129">If the surface is not a render target, a compatible render target is used, and the result is copied to the surface at the end of the scene.</span></span>

<span data-ttu-id="bc203-130">**ID3DXRenderToSurface** 介面是藉由呼叫 [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md)函數來取得。</span><span class="sxs-lookup"><span data-stu-id="bc203-130">The **ID3DXRenderToSurface** interface is obtained by calling the [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) function.</span></span>

<span data-ttu-id="bc203-131">LPD3DXRENDERTOSURFACE 型別定義為 **ID3DXRenderToSurface** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="bc203-131">The LPD3DXRENDERTOSURFACE type is defined as a pointer to the **ID3DXRenderToSurface** interface.</span></span>


```
typedef interface ID3DXRenderToSurface ID3DXRenderToSurface;
typedef interface ID3DXRenderToSurface *LPD3DXRENDERTOSURFACE;
```



## <a name="requirements"></a><span data-ttu-id="bc203-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc203-132">Requirements</span></span>



| <span data-ttu-id="bc203-133">需求</span><span class="sxs-lookup"><span data-stu-id="bc203-133">Requirement</span></span> | <span data-ttu-id="bc203-134">值</span><span class="sxs-lookup"><span data-stu-id="bc203-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc203-135">標頭</span><span class="sxs-lookup"><span data-stu-id="bc203-135">Header</span></span><br/>  | <dl> <span data-ttu-id="bc203-136"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="bc203-136"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="bc203-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="bc203-137">Library</span></span><br/> | <dl> <span data-ttu-id="bc203-138"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc203-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bc203-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc203-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc203-140">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="bc203-140">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
