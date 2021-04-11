---
title: 'ID3DX11EffectPass 介面 (D3dx11effect .h) '
description: ID3DX11EffectPass 介面會將狀態指派封裝在技術內。ID3DX11EffectPass 物件的存留期等於其父 ID3DX11Effect 物件的存留期。
ms.assetid: 4d86c362-b0f8-4396-86de-c7c89710f46d
keywords:
- ID3DX11EffectPass 介面 Direct3D 11
- ID3DX11EffectPass 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectPass
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a26732543d1033cfc439755df6ac397d2a28ec1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196392"
---
# <a name="id3dx11effectpass-interface"></a><span data-ttu-id="9a51c-105">ID3DX11EffectPass 介面</span><span class="sxs-lookup"><span data-stu-id="9a51c-105">ID3DX11EffectPass interface</span></span>

<span data-ttu-id="9a51c-106">**ID3DX11EffectPass** 介面會將狀態指派封裝在技術內。</span><span class="sxs-lookup"><span data-stu-id="9a51c-106">An **ID3DX11EffectPass** interface encapsulates state assignments within a technique.</span></span>

<span data-ttu-id="9a51c-107">**ID3DX11EffectPass** 物件的存留期等於其父 [**ID3DX11Effect**](id3dx11effect.md)物件的存留期。</span><span class="sxs-lookup"><span data-stu-id="9a51c-107">The lifetime of an **ID3DX11EffectPass** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="9a51c-108">方法</span><span class="sxs-lookup"><span data-stu-id="9a51c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9a51c-109">方法</span><span class="sxs-lookup"><span data-stu-id="9a51c-109">Methods</span></span>

<span data-ttu-id="9a51c-110">**ID3DX11EffectPass** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9a51c-110">The **ID3DX11EffectPass** interface has these methods.</span></span>



| <span data-ttu-id="9a51c-111">方法</span><span class="sxs-lookup"><span data-stu-id="9a51c-111">Method</span></span>                                                                   | <span data-ttu-id="9a51c-112">描述</span><span class="sxs-lookup"><span data-stu-id="9a51c-112">Description</span></span>                                                       |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="9a51c-113">**套用**</span><span class="sxs-lookup"><span data-stu-id="9a51c-113">**Apply**</span></span>](id3dx11effectpass-apply.md)                                 | <span data-ttu-id="9a51c-114">將傳遞中包含的狀態設定為裝置。</span><span class="sxs-lookup"><span data-stu-id="9a51c-114">Set the state contained in a pass to the device.</span></span><br/>       |
| [<span data-ttu-id="9a51c-115">**ComputeStateBlockMask**</span><span class="sxs-lookup"><span data-stu-id="9a51c-115">**ComputeStateBlockMask**</span></span>](id3dx11effectpass-computestateblockmask.md) | <span data-ttu-id="9a51c-116">產生遮罩以允許/防止狀態變更。</span><span class="sxs-lookup"><span data-stu-id="9a51c-116">Generate a mask for allowing/preventing state changes.</span></span><br/> |
| [<span data-ttu-id="9a51c-117">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="9a51c-117">**GetAnnotationByIndex**</span></span>](id3dx11effectpass-getannotationbyindex.md)   | <span data-ttu-id="9a51c-118">依索引取得批註。</span><span class="sxs-lookup"><span data-stu-id="9a51c-118">Get an annotation by index.</span></span><br/>                            |
| [<span data-ttu-id="9a51c-119">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="9a51c-119">**GetAnnotationByName**</span></span>](id3dx11effectpass-getannotationbyname.md)     | <span data-ttu-id="9a51c-120">依名稱取得批註。</span><span class="sxs-lookup"><span data-stu-id="9a51c-120">Get an annotation by name.</span></span><br/>                             |
| [<span data-ttu-id="9a51c-121">**GetComputeShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="9a51c-121">**GetComputeShaderDesc**</span></span>](id3dx11effectpass-getcomputeshaderdesc.md)   | <span data-ttu-id="9a51c-122">取得計算著色器的描述。</span><span class="sxs-lookup"><span data-stu-id="9a51c-122">Get a compute-shader description.</span></span><br/>                      |
| [<span data-ttu-id="9a51c-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="9a51c-123">**GetDesc**</span></span>](id3dx11effectpass-getdesc.md)                             | <span data-ttu-id="9a51c-124">取得傳遞描述。</span><span class="sxs-lookup"><span data-stu-id="9a51c-124">Get a pass description.</span></span><br/>                                |
| [<span data-ttu-id="9a51c-125">**GetDomainShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="9a51c-125">**GetDomainShaderDesc**</span></span>](id3dx11effectpass-getdomainshaderdesc.md)     | <span data-ttu-id="9a51c-126">取得網域著色器描述。</span><span class="sxs-lookup"><span data-stu-id="9a51c-126">Get a domain-shader description.</span></span><br/>                       |
| [<span data-ttu-id="9a51c-127">**GetGeometryShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="9a51c-127">**GetGeometryShaderDesc**</span></span>](id3dx11effectpass-getgeometryshaderdesc.md) | <span data-ttu-id="9a51c-128">取得幾何著色器描述。</span><span class="sxs-lookup"><span data-stu-id="9a51c-128">Get a geometry-shader description.</span></span><br/>                     |
| [<span data-ttu-id="9a51c-129">**GetHullShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="9a51c-129">**GetHullShaderDesc**</span></span>](id3dx11effectpass-gethullshaderdesc.md)         | <span data-ttu-id="9a51c-130">取得輪廓-著色器描述。</span><span class="sxs-lookup"><span data-stu-id="9a51c-130">Get hull-shader description.</span></span><br/>                           |
| [<span data-ttu-id="9a51c-131">**GetPixelShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="9a51c-131">**GetPixelShaderDesc**</span></span>](id3dx11effectpass-getpixelshaderdesc.md)       | <span data-ttu-id="9a51c-132">取得圖元著色器描述。</span><span class="sxs-lookup"><span data-stu-id="9a51c-132">Get a pixel-shader description.</span></span><br/>                        |
| [<span data-ttu-id="9a51c-133">**GetVertexShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="9a51c-133">**GetVertexShaderDesc**</span></span>](id3dx11effectpass-getvertexshaderdesc.md)     | <span data-ttu-id="9a51c-134">取得頂點著色器描述。</span><span class="sxs-lookup"><span data-stu-id="9a51c-134">Get a vertex-shader description.</span></span><br/>                       |
| [<span data-ttu-id="9a51c-135">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="9a51c-135">**IsValid**</span></span>](id3dx11effectpass-isvalid.md)                             | <span data-ttu-id="9a51c-136">測試 pass 以查看它是否包含有效的語法。</span><span class="sxs-lookup"><span data-stu-id="9a51c-136">Test a pass to see if it contains valid syntax.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="9a51c-137">備註</span><span class="sxs-lookup"><span data-stu-id="9a51c-137">Remarks</span></span>

<span data-ttu-id="9a51c-138">Pass 是設定呈現狀態物件和著色器的程式碼區塊。</span><span class="sxs-lookup"><span data-stu-id="9a51c-138">A pass is a block of code that sets render-state objects and shaders.</span></span> <span data-ttu-id="9a51c-139">Pass 會在技術內宣告。</span><span class="sxs-lookup"><span data-stu-id="9a51c-139">A pass is declared within a technique.</span></span>

<span data-ttu-id="9a51c-140">若要取得效果傳遞介面，請呼叫 [**ID3DX11EffectTechnique：： GetPassByName**](id3dx11effecttechnique-getpassbyname.md)之類的方法。</span><span class="sxs-lookup"><span data-stu-id="9a51c-140">To get an effect-pass interface, call a method like [**ID3DX11EffectTechnique::GetPassByName**](id3dx11effecttechnique-getpassbyname.md).</span></span>

> [!Note]  
> <span data-ttu-id="9a51c-141">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="9a51c-141">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9a51c-142">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="9a51c-142">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9a51c-143">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="9a51c-143">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9a51c-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a51c-144">Requirements</span></span>



| <span data-ttu-id="9a51c-145">需求</span><span class="sxs-lookup"><span data-stu-id="9a51c-145">Requirement</span></span> | <span data-ttu-id="9a51c-146">值</span><span class="sxs-lookup"><span data-stu-id="9a51c-146">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a51c-147">標頭</span><span class="sxs-lookup"><span data-stu-id="9a51c-147">Header</span></span><br/>  | <dl> <span data-ttu-id="9a51c-148"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a51c-148"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9a51c-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="9a51c-149">Library</span></span><br/> | <dl> <span data-ttu-id="9a51c-150"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="9a51c-150"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a51c-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a51c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a51c-152">效果11介面</span><span class="sxs-lookup"><span data-stu-id="9a51c-152">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="9a51c-153">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="9a51c-153">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





