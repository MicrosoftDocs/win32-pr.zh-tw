---
title: 'ID3DX11EffectVariable AsShader 方法 (D3dx11effect .h) '
description: 取得著色器變數。
ms.assetid: 660ba087-5320-44f7-946f-e500101fc6bb
keywords:
- AsShader 方法 Direct3D 11
- AsShader 方法 Direct3D 11，ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，AsShader 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3c8d9f1a487e4003bd032180d1f815e4a48fe0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992322"
---
# <a name="id3dx11effectvariableasshader-method"></a><span data-ttu-id="429d8-106">ID3DX11EffectVariable：： AsShader 方法</span><span class="sxs-lookup"><span data-stu-id="429d8-106">ID3DX11EffectVariable::AsShader method</span></span>

<span data-ttu-id="429d8-107">取得著色器變數。</span><span class="sxs-lookup"><span data-stu-id="429d8-107">Get a shader variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="429d8-108">語法</span><span class="sxs-lookup"><span data-stu-id="429d8-108">Syntax</span></span>


```C++
ID3DX11EffectShaderVariable* AsShader();
```



## <a name="parameters"></a><span data-ttu-id="429d8-109">參數</span><span class="sxs-lookup"><span data-stu-id="429d8-109">Parameters</span></span>

<span data-ttu-id="429d8-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="429d8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="429d8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="429d8-111">Return value</span></span>

<span data-ttu-id="429d8-112">類型： **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="429d8-112">Type: **[**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***</span></span>

<span data-ttu-id="429d8-113">著色器變數的指標。</span><span class="sxs-lookup"><span data-stu-id="429d8-113">A pointer to a shader variable.</span></span> <span data-ttu-id="429d8-114">請參閱 [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)。</span><span class="sxs-lookup"><span data-stu-id="429d8-114">See [**ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="429d8-115">備註</span><span class="sxs-lookup"><span data-stu-id="429d8-115">Remarks</span></span>

<span data-ttu-id="429d8-116">AsShader 會傳回已特製化至著色器變數的效果變數版本。</span><span class="sxs-lookup"><span data-stu-id="429d8-116">AsShader returns a version of the effect variable that has been specialized to a shader variable.</span></span> <span data-ttu-id="429d8-117">類似于轉換，如果效果變數不包含著色器資料，則此特製化會傳回不正確物件。</span><span class="sxs-lookup"><span data-stu-id="429d8-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain shader data.</span></span>

<span data-ttu-id="429d8-118">應用程式可以藉由呼叫 [**IsValid**](id3dx11effectvariable-isvalid.md)來測試傳回的物件是否有效。</span><span class="sxs-lookup"><span data-stu-id="429d8-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="429d8-119">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="429d8-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="429d8-120">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="429d8-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="429d8-121">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="429d8-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="429d8-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="429d8-122">Requirements</span></span>



| <span data-ttu-id="429d8-123">需求</span><span class="sxs-lookup"><span data-stu-id="429d8-123">Requirement</span></span> | <span data-ttu-id="429d8-124">值</span><span class="sxs-lookup"><span data-stu-id="429d8-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="429d8-125">標頭</span><span class="sxs-lookup"><span data-stu-id="429d8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="429d8-126"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="429d8-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="429d8-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="429d8-127">Library</span></span><br/> | <dl> <span data-ttu-id="429d8-128"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="429d8-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="429d8-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="429d8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="429d8-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="429d8-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





