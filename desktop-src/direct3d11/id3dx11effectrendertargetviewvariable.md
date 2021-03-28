---
title: 'ID3DX11EffectRenderTargetViewVariable 介面 (D3dx11effect .h) '
description: 呈現目標視圖介面會存取轉譯目標。
ms.assetid: 35c4e1da-05a8-4f1c-8730-58e3c90ad213
keywords:
- ID3DX11EffectRenderTargetViewVariable 介面 Direct3D 11
- ID3DX11EffectRenderTargetViewVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5b20f83639fd973016bbe263d9d21dae7b295c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974512"
---
# <a name="id3dx11effectrendertargetviewvariable-interface"></a><span data-ttu-id="8c596-105">ID3DX11EffectRenderTargetViewVariable 介面</span><span class="sxs-lookup"><span data-stu-id="8c596-105">ID3DX11EffectRenderTargetViewVariable interface</span></span>

<span data-ttu-id="8c596-106">呈現目標視圖介面會存取轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="8c596-106">A render-target-view interface accesses a render target.</span></span>

## <a name="members"></a><span data-ttu-id="8c596-107">成員</span><span class="sxs-lookup"><span data-stu-id="8c596-107">Members</span></span>

<span data-ttu-id="8c596-108">**ID3DX11EffectRenderTargetViewVariable** 介面繼承自 [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md)。</span><span class="sxs-lookup"><span data-stu-id="8c596-108">The **ID3DX11EffectRenderTargetViewVariable** interface inherits from [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="8c596-109">**ID3DX11EffectRenderTargetViewVariable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8c596-109">**ID3DX11EffectRenderTargetViewVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="8c596-110">方法</span><span class="sxs-lookup"><span data-stu-id="8c596-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8c596-111">方法</span><span class="sxs-lookup"><span data-stu-id="8c596-111">Methods</span></span>

<span data-ttu-id="8c596-112">**ID3DX11EffectRenderTargetViewVariable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8c596-112">The **ID3DX11EffectRenderTargetViewVariable** interface has these methods.</span></span>



| <span data-ttu-id="8c596-113">方法</span><span class="sxs-lookup"><span data-stu-id="8c596-113">Method</span></span>                                                                                     | <span data-ttu-id="8c596-114">描述</span><span class="sxs-lookup"><span data-stu-id="8c596-114">Description</span></span>                                |
|:-------------------------------------------------------------------------------------------|:-------------------------------------------|
| [<span data-ttu-id="8c596-115">**GetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="8c596-115">**GetRenderTarget**</span></span>](id3dx11effectrendertargetviewvariable-getrendertarget.md)           | <span data-ttu-id="8c596-116">取得呈現目標。</span><span class="sxs-lookup"><span data-stu-id="8c596-116">Get a render-target.</span></span><br/>            |
| [<span data-ttu-id="8c596-117">**GetRenderTargetArray**</span><span class="sxs-lookup"><span data-stu-id="8c596-117">**GetRenderTargetArray**</span></span>](id3dx11effectrendertargetviewvariable-getrendertargetarray.md) | <span data-ttu-id="8c596-118">取得呈現目標的陣列。</span><span class="sxs-lookup"><span data-stu-id="8c596-118">Get an array of render-targets.</span></span><br/> |
| [<span data-ttu-id="8c596-119">**SetRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="8c596-119">**SetRenderTarget**</span></span>](id3dx11effectrendertargetviewvariable-setrendertarget.md)           | <span data-ttu-id="8c596-120">設定呈現目標。</span><span class="sxs-lookup"><span data-stu-id="8c596-120">Set a render-target.</span></span><br/>            |
| [<span data-ttu-id="8c596-121">**SetRenderTargetArray**</span><span class="sxs-lookup"><span data-stu-id="8c596-121">**SetRenderTargetArray**</span></span>](id3dx11effectrendertargetviewvariable-setrendertargetarray.md) | <span data-ttu-id="8c596-122">設定呈現目標的陣列。</span><span class="sxs-lookup"><span data-stu-id="8c596-122">Set an array of render-targets.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8c596-123">備註</span><span class="sxs-lookup"><span data-stu-id="8c596-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8c596-124">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="8c596-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8c596-125">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8c596-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8c596-126">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="8c596-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8c596-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c596-127">Requirements</span></span>



| <span data-ttu-id="8c596-128">需求</span><span class="sxs-lookup"><span data-stu-id="8c596-128">Requirement</span></span> | <span data-ttu-id="8c596-129">值</span><span class="sxs-lookup"><span data-stu-id="8c596-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c596-130">標頭</span><span class="sxs-lookup"><span data-stu-id="8c596-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8c596-131"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c596-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8c596-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="8c596-132">Library</span></span><br/> | <dl> <span data-ttu-id="8c596-133"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="8c596-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c596-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c596-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c596-135">**ID3DX11EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="8c596-135">**ID3DX11EffectRasterizerVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="8c596-136">效果11介面</span><span class="sxs-lookup"><span data-stu-id="8c596-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="8c596-137">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="8c596-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





