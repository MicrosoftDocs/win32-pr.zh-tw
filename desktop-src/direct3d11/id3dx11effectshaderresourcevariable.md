---
title: 'ID3DX11EffectShaderResourceVariable 介面 (D3dx11effect .h) '
description: 著色器資源介面會存取著色器資源。
ms.assetid: 936a3439-1f7d-4fea-b124-1d6ead528250
keywords:
- ID3DX11EffectShaderResourceVariable 介面 Direct3D 11
- ID3DX11EffectShaderResourceVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7abfc2bf29bf3ea5333bf9e7da6630a62c5747aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992389"
---
# <a name="id3dx11effectshaderresourcevariable-interface"></a><span data-ttu-id="f7696-105">ID3DX11EffectShaderResourceVariable 介面</span><span class="sxs-lookup"><span data-stu-id="f7696-105">ID3DX11EffectShaderResourceVariable interface</span></span>

<span data-ttu-id="f7696-106">著色器資源介面會存取著色器資源。</span><span class="sxs-lookup"><span data-stu-id="f7696-106">A shader-resource interface accesses a shader resource.</span></span>

## <a name="members"></a><span data-ttu-id="f7696-107">成員</span><span class="sxs-lookup"><span data-stu-id="f7696-107">Members</span></span>

<span data-ttu-id="f7696-108">**ID3DX11EffectShaderResourceVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。</span><span class="sxs-lookup"><span data-stu-id="f7696-108">The **ID3DX11EffectShaderResourceVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="f7696-109">**ID3DX11EffectShaderResourceVariable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f7696-109">**ID3DX11EffectShaderResourceVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="f7696-110">方法</span><span class="sxs-lookup"><span data-stu-id="f7696-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f7696-111">方法</span><span class="sxs-lookup"><span data-stu-id="f7696-111">Methods</span></span>

<span data-ttu-id="f7696-112">**ID3DX11EffectShaderResourceVariable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f7696-112">The **ID3DX11EffectShaderResourceVariable** interface has these methods.</span></span>



| <span data-ttu-id="f7696-113">方法</span><span class="sxs-lookup"><span data-stu-id="f7696-113">Method</span></span>                                                                           | <span data-ttu-id="f7696-114">描述</span><span class="sxs-lookup"><span data-stu-id="f7696-114">Description</span></span>                                  |
|:---------------------------------------------------------------------------------|:---------------------------------------------|
| [<span data-ttu-id="f7696-115">**GetResource**</span><span class="sxs-lookup"><span data-stu-id="f7696-115">**GetResource**</span></span>](id3dx11effectshaderresourcevariable-getresource.md)           | <span data-ttu-id="f7696-116">取得著色器資源。</span><span class="sxs-lookup"><span data-stu-id="f7696-116">Get a shader resource.</span></span><br/>            |
| [<span data-ttu-id="f7696-117">**GetResourceArray**</span><span class="sxs-lookup"><span data-stu-id="f7696-117">**GetResourceArray**</span></span>](id3dx11effectshaderresourcevariable-getresourcearray.md) | <span data-ttu-id="f7696-118">取得著色器資源的陣列。</span><span class="sxs-lookup"><span data-stu-id="f7696-118">Get an array of shader resources.</span></span><br/> |
| [<span data-ttu-id="f7696-119">**SetResource**</span><span class="sxs-lookup"><span data-stu-id="f7696-119">**SetResource**</span></span>](id3dx11effectshaderresourcevariable-setresource.md)           | <span data-ttu-id="f7696-120">設定著色器資源。</span><span class="sxs-lookup"><span data-stu-id="f7696-120">Set a shader resource.</span></span><br/>            |
| [<span data-ttu-id="f7696-121">**SetResourceArray**</span><span class="sxs-lookup"><span data-stu-id="f7696-121">**SetResourceArray**</span></span>](id3dx11effectshaderresourcevariable-setresourcearray.md) | <span data-ttu-id="f7696-122">設定著色器資源的陣列。</span><span class="sxs-lookup"><span data-stu-id="f7696-122">Set an array of shader resources.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f7696-123">備註</span><span class="sxs-lookup"><span data-stu-id="f7696-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f7696-124">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="f7696-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f7696-125">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f7696-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f7696-126">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="f7696-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f7696-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7696-127">Requirements</span></span>



| <span data-ttu-id="f7696-128">需求</span><span class="sxs-lookup"><span data-stu-id="f7696-128">Requirement</span></span> | <span data-ttu-id="f7696-129">值</span><span class="sxs-lookup"><span data-stu-id="f7696-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7696-130">標頭</span><span class="sxs-lookup"><span data-stu-id="f7696-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f7696-131"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="f7696-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f7696-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="f7696-132">Library</span></span><br/> | <dl> <span data-ttu-id="f7696-133"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="f7696-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7696-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7696-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7696-135">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="f7696-135">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="f7696-136">效果11介面</span><span class="sxs-lookup"><span data-stu-id="f7696-136">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f7696-137">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="f7696-137">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





