---
title: 'ID3DX11EffectVariable 介面 (D3dx11effect .h) '
description: ID3DX11EffectVariable 介面是所有效果變數的基類。ID3DX11EffectVariable 物件的存留期等於其父 ID3DX11Effect 物件的存留期。
ms.assetid: 07f1b7d7-c266-49ae-b79a-7a645521df89
keywords:
- ID3DX11EffectVariable 介面 Direct3D 11
- ID3DX11EffectVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1df38a12c54776072bb922ffc4cd5bcd0d79776
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696743"
---
# <a name="id3dx11effectvariable-interface"></a><span data-ttu-id="ad7ea-105">ID3DX11EffectVariable 介面</span><span class="sxs-lookup"><span data-stu-id="ad7ea-105">ID3DX11EffectVariable interface</span></span>

<span data-ttu-id="ad7ea-106">**ID3DX11EffectVariable** 介面是所有效果變數的基類。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-106">The **ID3DX11EffectVariable** interface is the base class for all effect variables.</span></span>

<span data-ttu-id="ad7ea-107">**ID3DX11EffectVariable** 物件的存留期等於其父 [**ID3DX11Effect**](id3dx11effect.md)物件的存留期。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-107">The lifetime of an **ID3DX11EffectVariable** object is equal to the lifetime of its parent [**ID3DX11Effect**](id3dx11effect.md) object.</span></span>

-   [<span data-ttu-id="ad7ea-108">方法</span><span class="sxs-lookup"><span data-stu-id="ad7ea-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ad7ea-109">方法</span><span class="sxs-lookup"><span data-stu-id="ad7ea-109">Methods</span></span>

<span data-ttu-id="ad7ea-110">**ID3DX11EffectVariable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-110">The **ID3DX11EffectVariable** interface has these methods.</span></span>



| <span data-ttu-id="ad7ea-111">方法</span><span class="sxs-lookup"><span data-stu-id="ad7ea-111">Method</span></span>                                                                           | <span data-ttu-id="ad7ea-112">描述</span><span class="sxs-lookup"><span data-stu-id="ad7ea-112">Description</span></span>                                            |
|:---------------------------------------------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="ad7ea-113">**AsBlend**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-113">**AsBlend**</span></span>](id3dx11effectvariable-asblend.md)                                 | <span data-ttu-id="ad7ea-114">取得效果 blend 變數。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-114">Get a effect-blend variable.</span></span><br/>                |
| [<span data-ttu-id="ad7ea-115">**AsClassInstance**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-115">**AsClassInstance**</span></span>](id3dx11effectvariable-asclassinstance.md)                 | <span data-ttu-id="ad7ea-116">取得類別執行個體變數。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-116">Get a class-instance variable.</span></span><br/>              |
| [<span data-ttu-id="ad7ea-117">**AsConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-117">**AsConstantBuffer**</span></span>](id3dx11effectvariable-asconstantbuffer.md)               | <span data-ttu-id="ad7ea-118">取得常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-118">Get a constant buffer.</span></span><br/>                      |
| [<span data-ttu-id="ad7ea-119">**AsDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-119">**AsDepthStencil**</span></span>](id3dx11effectvariable-asdepthstencil.md)                   | <span data-ttu-id="ad7ea-120">取得深度樣板變數。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-120">Get a depth-stencil variable.</span></span><br/>               |
| [<span data-ttu-id="ad7ea-121">**AsDepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-121">**AsDepthStencilView**</span></span>](id3dx11effectvariable-asdepthstencilview.md)           | <span data-ttu-id="ad7ea-122">取得深度樣板視圖變數。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-122">Get a depth-stencil-view variable.</span></span><br/>          |
| [<span data-ttu-id="ad7ea-123">**AsInterface**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-123">**AsInterface**</span></span>](id3dx11effectvariable-asinterface.md)                         | <span data-ttu-id="ad7ea-124">取得介面變數。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-124">Get an interface variable.</span></span><br/>                  |
| [<span data-ttu-id="ad7ea-125">**AsMatrix**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-125">**AsMatrix**</span></span>](id3dx11effectvariable-asmatrix.md)                               | <span data-ttu-id="ad7ea-126">取得矩陣變數。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-126">Get a matrix variable.</span></span><br/>                      |
| [<span data-ttu-id="ad7ea-127">**AsRasterizer**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-127">**AsRasterizer**</span></span>](id3dx11effectvariable-asrasterizer.md)                       | <span data-ttu-id="ad7ea-128">取得轉譯器變數。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-128">Get a rasterizer variable.</span></span><br/>                  |
| [<span data-ttu-id="ad7ea-129">**AsRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-129">**AsRenderTargetView**</span></span>](id3dx11effectvariable-asrendertargetview.md)           | <span data-ttu-id="ad7ea-130">取得呈現目標視圖變數。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-130">Get a render-target-view variable.</span></span><br/>          |
| [<span data-ttu-id="ad7ea-131">**AsSampler**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-131">**AsSampler**</span></span>](id3dx11effectvariable-assampler.md)                             | <span data-ttu-id="ad7ea-132">取得取樣器變數。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-132">Get a sampler variable.</span></span><br/>                     |
| [<span data-ttu-id="ad7ea-133">**AsScalar**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-133">**AsScalar**</span></span>](id3dx11effectvariable-asscalar.md)                               | <span data-ttu-id="ad7ea-134">取得純量變數。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-134">Get a scalar variable.</span></span><br/>                      |
| [<span data-ttu-id="ad7ea-135">**AsShader**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-135">**AsShader**</span></span>](id3dx11effectvariable-asshader.md)                               | <span data-ttu-id="ad7ea-136">取得著色器變數。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-136">Get a shader variable.</span></span><br/>                      |
| [<span data-ttu-id="ad7ea-137">**AsShaderResource**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-137">**AsShaderResource**</span></span>](id3dx11effectvariable-asshaderresource.md)               | <span data-ttu-id="ad7ea-138">取得著色器的資源變數。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-138">Get a shader-resource variable.</span></span><br/>             |
| [<span data-ttu-id="ad7ea-139">**AsString**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-139">**AsString**</span></span>](id3dx11effectvariable-asstring.md)                               | <span data-ttu-id="ad7ea-140">取得字串變數。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-140">Get a string variable.</span></span><br/>                      |
| [<span data-ttu-id="ad7ea-141">**AsUnorderedAccessView**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-141">**AsUnorderedAccessView**</span></span>](id3dx11effectvariable-asunorderedaccessview.md)     | <span data-ttu-id="ad7ea-142">取得未排序的存取視圖變數。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-142">Get an unordered-access-view variable.</span></span><br/>      |
| [<span data-ttu-id="ad7ea-143">**AsVector**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-143">**AsVector**</span></span>](id3dx11effectvariable-asvector.md)                               | <span data-ttu-id="ad7ea-144">取得向量變數。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-144">Get a vector variable.</span></span><br/>                      |
| [<span data-ttu-id="ad7ea-145">**GetAnnotationByIndex**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-145">**GetAnnotationByIndex**</span></span>](id3dx11effectvariable-getannotationbyindex.md)       | <span data-ttu-id="ad7ea-146">依索引取得批註。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-146">Get an annotation by index.</span></span><br/>                 |
| [<span data-ttu-id="ad7ea-147">**GetAnnotationByName**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-147">**GetAnnotationByName**</span></span>](id3dx11effectvariable-getannotationbyname.md)         | <span data-ttu-id="ad7ea-148">依名稱取得批註。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-148">Get an annotation by name.</span></span><br/>                  |
| [<span data-ttu-id="ad7ea-149">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-149">**GetDesc**</span></span>](id3dx11effectvariable-getdesc.md)                                 | <span data-ttu-id="ad7ea-150">取得描述。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-150">Get a description.</span></span><br/>                          |
| [<span data-ttu-id="ad7ea-151">**GetElement**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-151">**GetElement**</span></span>](id3dx11effectvariable-getelement.md)                           | <span data-ttu-id="ad7ea-152">取得陣列元素。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-152">Get an array element.</span></span><br/>                       |
| [<span data-ttu-id="ad7ea-153">**GetMemberByIndex**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-153">**GetMemberByIndex**</span></span>](id3dx11effectvariable-getmemberbyindex.md)               | <span data-ttu-id="ad7ea-154">依索引取得結構成員。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-154">Get a structure member by index.</span></span><br/>            |
| [<span data-ttu-id="ad7ea-155">**GetMemberByName**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-155">**GetMemberByName**</span></span>](id3dx11effectvariable-getmemberbyname.md)                 | <span data-ttu-id="ad7ea-156">依名稱取得結構成員。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-156">Get a structure member by name.</span></span><br/>             |
| [<span data-ttu-id="ad7ea-157">**GetMemberBySemantic**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-157">**GetMemberBySemantic**</span></span>](id3dx11effectvariable-getmemberbysemantic.md)         | <span data-ttu-id="ad7ea-158">依語義取得結構成員。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-158">Get a structure member by semantic.</span></span><br/>         |
| [<span data-ttu-id="ad7ea-159">**GetParentConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-159">**GetParentConstantBuffer**</span></span>](id3dx11effectvariable-getparentconstantbuffer.md) | <span data-ttu-id="ad7ea-160">取得常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-160">Get a constant buffer.</span></span><br/>                      |
| [<span data-ttu-id="ad7ea-161">**GetRawValue**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-161">**GetRawValue**</span></span>](id3dx11effectvariable-getrawvalue.md)                         | <span data-ttu-id="ad7ea-162">取得資料。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-162">Get data.</span></span><br/>                                   |
| [<span data-ttu-id="ad7ea-163">**GetType**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-163">**GetType**</span></span>](id3dx11effectvariable-gettype.md)                                 | <span data-ttu-id="ad7ea-164">取得型別資訊。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-164">Get type information.</span></span><br/>                       |
| [<span data-ttu-id="ad7ea-165">**IsValid**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-165">**IsValid**</span></span>](id3dx11effectvariable-isvalid.md)                                 | <span data-ttu-id="ad7ea-166">比較資料類型與儲存的資料。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-166">Compare the data type with the data stored.</span></span><br/> |
| [<span data-ttu-id="ad7ea-167">**SetRawValue**</span><span class="sxs-lookup"><span data-stu-id="ad7ea-167">**SetRawValue**</span></span>](id3dx11effectvariable-setrawvalue.md)                         | <span data-ttu-id="ad7ea-168">設定資料。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-168">Set data.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="ad7ea-169">備註</span><span class="sxs-lookup"><span data-stu-id="ad7ea-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ad7ea-170">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-170">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ad7ea-171">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-171">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ad7ea-172">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="ad7ea-172">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ad7ea-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad7ea-173">Requirements</span></span>



| <span data-ttu-id="ad7ea-174">需求</span><span class="sxs-lookup"><span data-stu-id="ad7ea-174">Requirement</span></span> | <span data-ttu-id="ad7ea-175">值</span><span class="sxs-lookup"><span data-stu-id="ad7ea-175">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad7ea-176">標頭</span><span class="sxs-lookup"><span data-stu-id="ad7ea-176">Header</span></span><br/>  | <dl> <span data-ttu-id="ad7ea-177"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="ad7ea-177"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ad7ea-178">程式庫</span><span class="sxs-lookup"><span data-stu-id="ad7ea-178">Library</span></span><br/> | <dl> <span data-ttu-id="ad7ea-179"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="ad7ea-179"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad7ea-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad7ea-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad7ea-181">效果11介面</span><span class="sxs-lookup"><span data-stu-id="ad7ea-181">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="ad7ea-182">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="ad7ea-182">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





