---
title: 'ID3DX11EffectDepthStencilViewVariable 介面 (D3dx11effect .h) '
description: 深度樣板視圖變數介面會存取深度樣板視圖。
ms.assetid: 316bf0cc-a7cd-4a40-932a-d566e3c2001e
keywords:
- ID3DX11EffectDepthStencilViewVariable 介面 Direct3D 11
- ID3DX11EffectDepthStencilViewVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51961bd1300157eef4acb4dd15484d5146a166f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196347"
---
# <a name="id3dx11effectdepthstencilviewvariable-interface"></a><span data-ttu-id="59b42-105">ID3DX11EffectDepthStencilViewVariable 介面</span><span class="sxs-lookup"><span data-stu-id="59b42-105">ID3DX11EffectDepthStencilViewVariable interface</span></span>

<span data-ttu-id="59b42-106">深度樣板視圖變數介面會存取深度樣板視圖。</span><span class="sxs-lookup"><span data-stu-id="59b42-106">A depth-stencil-view-variable interface accesses a depth-stencil view.</span></span>

## <a name="members"></a><span data-ttu-id="59b42-107">成員</span><span class="sxs-lookup"><span data-stu-id="59b42-107">Members</span></span>

<span data-ttu-id="59b42-108">**ID3DX11EffectDepthStencilViewVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。</span><span class="sxs-lookup"><span data-stu-id="59b42-108">The **ID3DX11EffectDepthStencilViewVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="59b42-109">**ID3DX11EffectDepthStencilViewVariable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="59b42-109">**ID3DX11EffectDepthStencilViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="59b42-110">方法</span><span class="sxs-lookup"><span data-stu-id="59b42-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="59b42-111">方法</span><span class="sxs-lookup"><span data-stu-id="59b42-111">Methods</span></span>

<span data-ttu-id="59b42-112">**ID3DX11EffectDepthStencilViewVariable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="59b42-112">The **ID3DX11EffectDepthStencilViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="59b42-113">方法</span><span class="sxs-lookup"><span data-stu-id="59b42-113">Method</span></span>                                                                                     | <span data-ttu-id="59b42-114">描述</span><span class="sxs-lookup"><span data-stu-id="59b42-114">Description</span></span>                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="59b42-115">**GetDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="59b42-115">**GetDepthStencil**</span></span>](id3dx11effectdepthstencilviewvariable-getdepthstencil.md)           | <span data-ttu-id="59b42-116">取得深度樣板查看資源。</span><span class="sxs-lookup"><span data-stu-id="59b42-116">Get a depth-stencil-view resource.</span></span><br/>            |
| [<span data-ttu-id="59b42-117">**GetDepthStencilArray**</span><span class="sxs-lookup"><span data-stu-id="59b42-117">**GetDepthStencilArray**</span></span>](id3dx11effectdepthstencilviewvariable-getdepthstencilarray.md) | <span data-ttu-id="59b42-118">取得深度樣板視圖資源的陣列。</span><span class="sxs-lookup"><span data-stu-id="59b42-118">Get an array of depth-stencil-view resources.</span></span><br/> |
| [<span data-ttu-id="59b42-119">**SetDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="59b42-119">**SetDepthStencil**</span></span>](id3dx11effectdepthstencilviewvariable-setdepthstencil.md)           | <span data-ttu-id="59b42-120">設定深度範本-view 資源。</span><span class="sxs-lookup"><span data-stu-id="59b42-120">Set a depth-stencil-view resource.</span></span><br/>            |
| [<span data-ttu-id="59b42-121">**SetDepthStencilArray**</span><span class="sxs-lookup"><span data-stu-id="59b42-121">**SetDepthStencilArray**</span></span>](id3dx11effectdepthstencilviewvariable-setdepthstencilarray.md) | <span data-ttu-id="59b42-122">設定深度樣板視圖資源的陣列。</span><span class="sxs-lookup"><span data-stu-id="59b42-122">Set an array of depth-stencil-view resources.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="59b42-123">備註</span><span class="sxs-lookup"><span data-stu-id="59b42-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="59b42-124">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="59b42-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="59b42-125">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="59b42-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="59b42-126">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="59b42-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="59b42-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="59b42-127">Requirements</span></span>



| <span data-ttu-id="59b42-128">需求</span><span class="sxs-lookup"><span data-stu-id="59b42-128">Requirement</span></span> | <span data-ttu-id="59b42-129">值</span><span class="sxs-lookup"><span data-stu-id="59b42-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59b42-130">標頭</span><span class="sxs-lookup"><span data-stu-id="59b42-130">Header</span></span><br/>  | <dl> <span data-ttu-id="59b42-131"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="59b42-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="59b42-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="59b42-132">Library</span></span><br/> | <dl> <span data-ttu-id="59b42-133"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="59b42-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59b42-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59b42-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b42-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="59b42-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="59b42-136">效果11介面</span><span class="sxs-lookup"><span data-stu-id="59b42-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="59b42-137">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="59b42-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





