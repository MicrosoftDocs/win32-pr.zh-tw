---
title: 'ID3DX11EffectTechnique 介面 (D3dx11effect .h) '
description: ID3DX11EffectTechnique 介面是通過的集合。ID3DX11EffectTechnique 物件的存留期等於其父 ID3DX11Effect 物件的存留期。
ms.assetid: 63d52cac-287d-4432-bf2b-7b4e67e525e6
keywords:
- ID3DX11EffectTechnique 介面 Direct3D 11
- ID3DX11EffectTechnique 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e582d8f94b2dbcbb2052a8cf3a59d8ba514367cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974705"
---
# <a name="id3dx11effecttechnique-interface"></a><span data-ttu-id="66290-105">ID3DX11EffectTechnique 介面</span><span class="sxs-lookup"><span data-stu-id="66290-105">ID3DX11EffectTechnique interface</span></span>

<span data-ttu-id="66290-106">**ID3DX11EffectTechnique** 介面是通過的集合。</span><span class="sxs-lookup"><span data-stu-id="66290-106">An **ID3DX11EffectTechnique** interface is a collection of passes.</span></span>

<span data-ttu-id="66290-107">**ID3DX11EffectTechnique** 物件的存留期等於其父 [**ID3DX11Effect**](id3dx11effect.md)物件的存留期。</span><span class="sxs-lookup"><span data-stu-id="66290-107">The lifetime of an **ID3DX11EffectTechnique** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="66290-108">方法</span><span class="sxs-lookup"><span data-stu-id="66290-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="66290-109">方法</span><span class="sxs-lookup"><span data-stu-id="66290-109">Methods</span></span>

<span data-ttu-id="66290-110">**ID3DX11EffectTechnique** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="66290-110">The **ID3DX11EffectTechnique** interface has these methods.</span></span>



| <span data-ttu-id="66290-111">方法</span><span class="sxs-lookup"><span data-stu-id="66290-111">Method</span></span>                                                                        | <span data-ttu-id="66290-112">描述</span><span class="sxs-lookup"><span data-stu-id="66290-112">Description</span></span>                                                           |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="66290-113">**ComputeStateBlockMask**</span><span class="sxs-lookup"><span data-stu-id="66290-113">**ComputeStateBlockMask**</span></span>](id3dx11effecttechnique-computestateblockmask.md) | <span data-ttu-id="66290-114">計算狀態欄塊遮罩以允許/防止狀態變更。</span><span class="sxs-lookup"><span data-stu-id="66290-114">Compute a state-block mask to allow/prevent state changes.</span></span><br/> |
| [<span data-ttu-id="66290-115">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="66290-115">**GetAnnotationByIndex**</span></span>](id3dx11effecttechnique-getannotationbyindex.md)   | <span data-ttu-id="66290-116">依索引取得批註。</span><span class="sxs-lookup"><span data-stu-id="66290-116">Get an annotation by index.</span></span><br/>                                |
| [<span data-ttu-id="66290-117">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="66290-117">**GetAnnotationByName**</span></span>](id3dx11effecttechnique-getannotationbyname.md)     | <span data-ttu-id="66290-118">依名稱取得批註。</span><span class="sxs-lookup"><span data-stu-id="66290-118">Get an annotation by name.</span></span><br/>                                 |
| [<span data-ttu-id="66290-119">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="66290-119">**GetDesc**</span></span>](id3dx11effecttechnique-getdesc.md)                             | <span data-ttu-id="66290-120">取得技術描述。</span><span class="sxs-lookup"><span data-stu-id="66290-120">Get a technique description.</span></span><br/>                               |
| [<span data-ttu-id="66290-121">**GetPassByIndex**</span><span class="sxs-lookup"><span data-stu-id="66290-121">**GetPassByIndex**</span></span>](id3dx11effecttechnique-getpassbyindex.md)               | <span data-ttu-id="66290-122">依索引取得傳遞。</span><span class="sxs-lookup"><span data-stu-id="66290-122">Get a pass by index.</span></span><br/>                                       |
| [<span data-ttu-id="66290-123">**GetPassByName**</span><span class="sxs-lookup"><span data-stu-id="66290-123">**GetPassByName**</span></span>](id3dx11effecttechnique-getpassbyname.md)                 | <span data-ttu-id="66290-124">依名稱取得傳遞。</span><span class="sxs-lookup"><span data-stu-id="66290-124">Get a pass by name.</span></span><br/>                                        |
| [<span data-ttu-id="66290-125">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="66290-125">**IsValid**</span></span>](id3dx11effecttechnique-isvalid.md)                             | <span data-ttu-id="66290-126">測試技術以查看其是否包含有效的語法。</span><span class="sxs-lookup"><span data-stu-id="66290-126">Test a technique to see if it contains valid syntax.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="66290-127">備註</span><span class="sxs-lookup"><span data-stu-id="66290-127">Remarks</span></span>

<span data-ttu-id="66290-128">效果包含一或多個技術;每個技術都包含一或多個階段;每個階段都包含狀態指派。</span><span class="sxs-lookup"><span data-stu-id="66290-128">An effect contains one or more techniques; each technique contains one or more passes; each pass contains state assignments.</span></span>

<span data-ttu-id="66290-129">若要取得效果技巧介面，請呼叫 [**ID3DX11Effect：： GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)之類的方法。</span><span class="sxs-lookup"><span data-stu-id="66290-129">To get an effect-technique interface, call a method such as [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="66290-130">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="66290-130">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="66290-131">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="66290-131">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="66290-132">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="66290-132">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="66290-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="66290-133">Requirements</span></span>



| <span data-ttu-id="66290-134">需求</span><span class="sxs-lookup"><span data-stu-id="66290-134">Requirement</span></span> | <span data-ttu-id="66290-135">值</span><span class="sxs-lookup"><span data-stu-id="66290-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66290-136">標頭</span><span class="sxs-lookup"><span data-stu-id="66290-136">Header</span></span><br/>  | <dl> <span data-ttu-id="66290-137"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="66290-137"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="66290-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="66290-138">Library</span></span><br/> | <dl> <span data-ttu-id="66290-139"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="66290-139"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66290-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66290-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66290-141">效果11介面</span><span class="sxs-lookup"><span data-stu-id="66290-141">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="66290-142">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="66290-142">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





