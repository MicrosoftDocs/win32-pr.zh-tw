---
title: 'ID3DX11EffectShaderVariable 介面 (D3dx11effect .h) '
description: 著色器變數介面會存取著色器變數。
ms.assetid: e547a5e9-7b60-4a85-806d-272be55d12e7
keywords:
- ID3DX11EffectShaderVariable 介面 Direct3D 11
- ID3DX11EffectShaderVariable 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbb011591f715b4bac57dfa34f640ea90278f6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992222"
---
# <a name="id3dx11effectshadervariable-interface"></a><span data-ttu-id="81426-105">ID3DX11EffectShaderVariable 介面</span><span class="sxs-lookup"><span data-stu-id="81426-105">ID3DX11EffectShaderVariable interface</span></span>

<span data-ttu-id="81426-106">著色器變數介面會存取著色器變數。</span><span class="sxs-lookup"><span data-stu-id="81426-106">A shader-variable interface accesses a shader variable.</span></span>

## <a name="members"></a><span data-ttu-id="81426-107">成員</span><span class="sxs-lookup"><span data-stu-id="81426-107">Members</span></span>

<span data-ttu-id="81426-108">**ID3DX11EffectShaderVariable** 介面繼承自 [**ID3DX11EffectVariable**](id3dx11effectvariable.md)。</span><span class="sxs-lookup"><span data-stu-id="81426-108">The **ID3DX11EffectShaderVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="81426-109">**ID3DX11EffectShaderVariable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="81426-109">**ID3DX11EffectShaderVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="81426-110">方法</span><span class="sxs-lookup"><span data-stu-id="81426-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="81426-111">方法</span><span class="sxs-lookup"><span data-stu-id="81426-111">Methods</span></span>

<span data-ttu-id="81426-112">**ID3DX11EffectShaderVariable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="81426-112">The **ID3DX11EffectShaderVariable** interface has these methods.</span></span>



| <span data-ttu-id="81426-113">方法</span><span class="sxs-lookup"><span data-stu-id="81426-113">Method</span></span>                                                                                                           | <span data-ttu-id="81426-114">描述</span><span class="sxs-lookup"><span data-stu-id="81426-114">Description</span></span>                                            |
|:-----------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| [<span data-ttu-id="81426-115">**GetComputeShader**</span><span class="sxs-lookup"><span data-stu-id="81426-115">**GetComputeShader**</span></span>](id3dx11effectshadervariable-getcomputeshader.md)                                         | <span data-ttu-id="81426-116">取得計算著色器。</span><span class="sxs-lookup"><span data-stu-id="81426-116">Get a compute shader.</span></span><br/>                       |
| [<span data-ttu-id="81426-117">**GetDomainShader**</span><span class="sxs-lookup"><span data-stu-id="81426-117">**GetDomainShader**</span></span>](id3dx11effectshadervariable-getdomainshader.md)                                           | <span data-ttu-id="81426-118">取得網域著色器。</span><span class="sxs-lookup"><span data-stu-id="81426-118">Get a domain shader.</span></span><br/>                        |
| [<span data-ttu-id="81426-119">**GetGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="81426-119">**GetGeometryShader**</span></span>](id3dx11effectshadervariable-getgeometryshader.md)                                       | <span data-ttu-id="81426-120">取得幾何著色器。</span><span class="sxs-lookup"><span data-stu-id="81426-120">Get a geometry shader.</span></span><br/>                      |
| [<span data-ttu-id="81426-121">**GetHullShader**</span><span class="sxs-lookup"><span data-stu-id="81426-121">**GetHullShader**</span></span>](id3dx11effectshadervariable-gethullshader.md)                                               | <span data-ttu-id="81426-122">取得輪廓著色器。</span><span class="sxs-lookup"><span data-stu-id="81426-122">Get a hull shader.</span></span><br/>                          |
| [<span data-ttu-id="81426-123">**GetInputSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="81426-123">**GetInputSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getinputsignatureelementdesc.md)                 | <span data-ttu-id="81426-124">取得輸入簽名描述。</span><span class="sxs-lookup"><span data-stu-id="81426-124">Get an input-signature description.</span></span><br/>         |
| [<span data-ttu-id="81426-125">**GetOutputSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="81426-125">**GetOutputSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getoutputsignatureelementdesc.md)               | <span data-ttu-id="81426-126">取得輸出特徵標記描述。</span><span class="sxs-lookup"><span data-stu-id="81426-126">Get an output-signature description.</span></span><br/>        |
| [<span data-ttu-id="81426-127">**GetPatchConstantSignatureElementDesc**</span><span class="sxs-lookup"><span data-stu-id="81426-127">**GetPatchConstantSignatureElementDesc**</span></span>](id3dx11effectshadervariable-getpatchconstantsignatureelementdesc.md) | <span data-ttu-id="81426-128">取得修補程式常數簽章描述。</span><span class="sxs-lookup"><span data-stu-id="81426-128">Get a patch constant signature description.</span></span><br/> |
| [<span data-ttu-id="81426-129">**GetPixelShader**</span><span class="sxs-lookup"><span data-stu-id="81426-129">**GetPixelShader**</span></span>](id3dx11effectshadervariable-getpixelshader.md)                                             | <span data-ttu-id="81426-130">取得圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="81426-130">Get a pixel shader.</span></span><br/>                         |
| [<span data-ttu-id="81426-131">**GetShaderDesc**</span><span class="sxs-lookup"><span data-stu-id="81426-131">**GetShaderDesc**</span></span>](id3dx11effectshadervariable-getshaderdesc.md)                                               | <span data-ttu-id="81426-132">取得著色器描述。</span><span class="sxs-lookup"><span data-stu-id="81426-132">Get a shader description.</span></span><br/>                   |
| [<span data-ttu-id="81426-133">**GetVertexShader**</span><span class="sxs-lookup"><span data-stu-id="81426-133">**GetVertexShader**</span></span>](id3dx11effectshadervariable-getvertexshader.md)                                           | <span data-ttu-id="81426-134">取得頂點著色器。</span><span class="sxs-lookup"><span data-stu-id="81426-134">Get a vertex shader.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="81426-135">備註</span><span class="sxs-lookup"><span data-stu-id="81426-135">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="81426-136">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="81426-136">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="81426-137">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="81426-137">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="81426-138">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="81426-138">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="81426-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="81426-139">Requirements</span></span>



| <span data-ttu-id="81426-140">需求</span><span class="sxs-lookup"><span data-stu-id="81426-140">Requirement</span></span> | <span data-ttu-id="81426-141">值</span><span class="sxs-lookup"><span data-stu-id="81426-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81426-142">標頭</span><span class="sxs-lookup"><span data-stu-id="81426-142">Header</span></span><br/>  | <dl> <span data-ttu-id="81426-143"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="81426-143"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="81426-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="81426-144">Library</span></span><br/> | <dl> <span data-ttu-id="81426-145"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="81426-145"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81426-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81426-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81426-147">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="81426-147">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="81426-148">效果11介面</span><span class="sxs-lookup"><span data-stu-id="81426-148">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="81426-149">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="81426-149">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





