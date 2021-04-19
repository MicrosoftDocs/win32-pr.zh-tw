---
description: ID3DXRenderToEnvMap 介面可用來將轉譯的程式一般化至環境對應。
ms.assetid: d72db260-5493-4381-9269-521ad333f0b2
title: 'ID3DXRenderToEnvMap 介面 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c3fdfc37c206b6360fc0b7296bbf90c319652e28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000627"
---
# <a name="id3dxrendertoenvmap-interface"></a><span data-ttu-id="8f800-103">ID3DXRenderToEnvMap 介面</span><span class="sxs-lookup"><span data-stu-id="8f800-103">ID3DXRenderToEnvMap interface</span></span>

<span data-ttu-id="8f800-104">ID3DXRenderToEnvMap 介面可用來將轉譯的程式一般化至環境對應。</span><span class="sxs-lookup"><span data-stu-id="8f800-104">The ID3DXRenderToEnvMap interface is used to generalize the process of rendering to environment maps.</span></span>

## <a name="members"></a><span data-ttu-id="8f800-105">成員</span><span class="sxs-lookup"><span data-stu-id="8f800-105">Members</span></span>

<span data-ttu-id="8f800-106">**ID3DXRenderToEnvMap** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="8f800-106">The **ID3DXRenderToEnvMap** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8f800-107">**ID3DXRenderToEnvMap** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8f800-107">**ID3DXRenderToEnvMap** also has these types of members:</span></span>

-   [<span data-ttu-id="8f800-108">方法</span><span class="sxs-lookup"><span data-stu-id="8f800-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8f800-109">方法</span><span class="sxs-lookup"><span data-stu-id="8f800-109">Methods</span></span>

<span data-ttu-id="8f800-110">**ID3DXRenderToEnvMap** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8f800-110">The **ID3DXRenderToEnvMap** interface has these methods.</span></span>



| <span data-ttu-id="8f800-111">方法</span><span class="sxs-lookup"><span data-stu-id="8f800-111">Method</span></span>                                                          | <span data-ttu-id="8f800-112">描述</span><span class="sxs-lookup"><span data-stu-id="8f800-112">Description</span></span>                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f800-113">**BeginCube**</span><span class="sxs-lookup"><span data-stu-id="8f800-113">**BeginCube**</span></span>](id3dxrendertoenvmap--begincube.md)             | <span data-ttu-id="8f800-114">起始三次環境對應的呈現。</span><span class="sxs-lookup"><span data-stu-id="8f800-114">Initiate the rendering of a cubic environment map.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="8f800-115">**BeginHemisphere**</span><span class="sxs-lookup"><span data-stu-id="8f800-115">**BeginHemisphere**</span></span>](id3dxrendertoenvmap--beginhemisphere.md) | <span data-ttu-id="8f800-116">起始 hemispheric 環境對應的呈現。</span><span class="sxs-lookup"><span data-stu-id="8f800-116">Initiate the rendering of a hemispheric environment map.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="8f800-117">**BeginParabolic**</span><span class="sxs-lookup"><span data-stu-id="8f800-117">**BeginParabolic**</span></span>](id3dxrendertoenvmap--beginparabolic.md)   | <span data-ttu-id="8f800-118">起始拋物線環境對應的呈現。</span><span class="sxs-lookup"><span data-stu-id="8f800-118">Initiate the rendering of a parabolic environment map.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="8f800-119">**BeginSphere**</span><span class="sxs-lookup"><span data-stu-id="8f800-119">**BeginSphere**</span></span>](id3dxrendertoenvmap--beginsphere.md)         | <span data-ttu-id="8f800-120">起始球形環境對應的呈現。</span><span class="sxs-lookup"><span data-stu-id="8f800-120">Initiate the rendering of a spherical environment map.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="8f800-121">**結束**</span><span class="sxs-lookup"><span data-stu-id="8f800-121">**End**</span></span>](id3dxrendertoenvmap--end.md)                         | <span data-ttu-id="8f800-122">還原所有呈現目標，並視需要將所有呈現的臉部組成環境地圖介面。</span><span class="sxs-lookup"><span data-stu-id="8f800-122">Restore all render targets and, if needed, compose all the rendered faces into the environment map surface.</span></span><br/>                                                                           |
| [<span data-ttu-id="8f800-123">**臉部**</span><span class="sxs-lookup"><span data-stu-id="8f800-123">**Face**</span></span>](id3dxrendertoenvmap--face.md)                       | <span data-ttu-id="8f800-124">起始每個環境圖臉部的繪圖。</span><span class="sxs-lookup"><span data-stu-id="8f800-124">Initiate the drawing of each face of an environment map.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="8f800-125">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="8f800-125">**GetDesc**</span></span>](id3dxrendertoenvmap--getdesc.md)                 | <span data-ttu-id="8f800-126">抓取呈現介面的描述。</span><span class="sxs-lookup"><span data-stu-id="8f800-126">Retrieves the description of the render surface.</span></span><br/>                                                                                                                                      |
| [<span data-ttu-id="8f800-127">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="8f800-127">**GetDevice**</span></span>](id3dxrendertoenvmap--getdevice.md)             | <span data-ttu-id="8f800-128">捕獲與環境對應相關聯的 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="8f800-128">Retrieves the Direct3D device associated with the environment map.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="8f800-129">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="8f800-129">**OnLostDevice**</span></span>](id3dxrendertoenvmap--onlostdevice.md)       | <span data-ttu-id="8f800-130">您可以使用此方法來釋放視訊記憶體資源的所有參考，並刪除所有 stateblocks。</span><span class="sxs-lookup"><span data-stu-id="8f800-130">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="8f800-131">只要裝置遺失或在重設裝置之前，都應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="8f800-131">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="8f800-132">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="8f800-132">**OnResetDevice**</span></span>](id3dxrendertoenvmap--onresetdevice.md)     | <span data-ttu-id="8f800-133">您可以使用這個方法來重新取得資源，並儲存初始狀態。</span><span class="sxs-lookup"><span data-stu-id="8f800-133">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="8f800-134">備註</span><span class="sxs-lookup"><span data-stu-id="8f800-134">Remarks</span></span>

<span data-ttu-id="8f800-135">環境對應可用來紋理對應場景幾何，以提供更精密的場景，而不使用複雜的幾何。</span><span class="sxs-lookup"><span data-stu-id="8f800-135">An environment map is used to texture-map scene geometry to provide a more sophisticated scene without using complex geometry.</span></span> <span data-ttu-id="8f800-136">此介面支援針對下列種類的幾何建立介面： cube、半球體或 hemispheric、拋物線或球體。</span><span class="sxs-lookup"><span data-stu-id="8f800-136">This interface supports creating surfaces for the following kinds of geometry: cube, half sphere or hemispheric, parabolic, or sphere.</span></span>

<span data-ttu-id="8f800-137">**ID3DXRenderToEnvMap** 介面是藉由呼叫 [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md)函數來取得。</span><span class="sxs-lookup"><span data-stu-id="8f800-137">The **ID3DXRenderToEnvMap** interface is obtained by calling the [**D3DXCreateRenderToEnvMap**](d3dxcreaterendertoenvmap.md) function.</span></span>

<span data-ttu-id="8f800-138">LPD3DXRenderToEnvMap 型別定義為 **ID3DXRenderToEnvMap** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="8f800-138">The LPD3DXRenderToEnvMap type is defined as a pointer to the **ID3DXRenderToEnvMap** interface.</span></span>


```
typedef interface ID3DXRenderToEnvMap ID3DXRenderToEnvMap;
typedef interface ID3DXRenderToEnvMap *LPD3DXRenderToEnvMap;
```



## <a name="requirements"></a><span data-ttu-id="8f800-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f800-139">Requirements</span></span>



| <span data-ttu-id="8f800-140">需求</span><span class="sxs-lookup"><span data-stu-id="8f800-140">Requirement</span></span> | <span data-ttu-id="8f800-141">值</span><span class="sxs-lookup"><span data-stu-id="8f800-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f800-142">標頭</span><span class="sxs-lookup"><span data-stu-id="8f800-142">Header</span></span><br/>  | <dl> <span data-ttu-id="8f800-143"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="8f800-143"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="8f800-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="8f800-144">Library</span></span><br/> | <dl> <span data-ttu-id="8f800-145"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f800-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8f800-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f800-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f800-147">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="8f800-147">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
