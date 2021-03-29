---
title: 'ID3DX11EffectShaderVariable GetInputSignatureElementDesc 方法 (D3dx11effect .h) '
description: 取得輸入簽名描述。
ms.assetid: 45b1fd25-1005-48fd-8a61-561ea2c273e5
keywords:
- GetInputSignatureElementDesc 方法 Direct3D 11
- GetInputSignatureElementDesc 方法 Direct3D 11，ID3DX11EffectShaderVariable 介面
- ID3DX11EffectShaderVariable 介面 Direct3D 11，GetInputSignatureElementDesc 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetInputSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf788370c26da1ba773d797de544b1a64750d90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116305"
---
# <a name="id3dx11effectshadervariablegetinputsignatureelementdesc-method"></a><span data-ttu-id="6acd4-106">ID3DX11EffectShaderVariable：： GetInputSignatureElementDesc 方法</span><span class="sxs-lookup"><span data-stu-id="6acd4-106">ID3DX11EffectShaderVariable::GetInputSignatureElementDesc method</span></span>

<span data-ttu-id="6acd4-107">取得輸入簽名描述。</span><span class="sxs-lookup"><span data-stu-id="6acd4-107">Get an input-signature description.</span></span>

## <a name="syntax"></a><span data-ttu-id="6acd4-108">語法</span><span class="sxs-lookup"><span data-stu-id="6acd4-108">Syntax</span></span>


```C++
HRESULT GetInputSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="6acd4-109">參數</span><span class="sxs-lookup"><span data-stu-id="6acd4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6acd4-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="6acd4-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="6acd4-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6acd4-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6acd4-112">以零為基底的著色器索引。</span><span class="sxs-lookup"><span data-stu-id="6acd4-112">A zero-based shader index.</span></span>

</dd> <dt>

<span data-ttu-id="6acd4-113">*Element*</span><span class="sxs-lookup"><span data-stu-id="6acd4-113">*Element*</span></span> 
</dt> <dd>

<span data-ttu-id="6acd4-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6acd4-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6acd4-115">以零為基底的著色器元素索引。</span><span class="sxs-lookup"><span data-stu-id="6acd4-115">A zero-based shader-element index.</span></span>

</dd> <dt>

<span data-ttu-id="6acd4-116">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="6acd4-116">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="6acd4-117">Type： **[ **D3D11 \_ SIGNATURE \_ 參數 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span><span class="sxs-lookup"><span data-stu-id="6acd4-117">Type: **[**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span></span>

<span data-ttu-id="6acd4-118">參數描述的指標 (參閱 [**D3D11 \_ 簽名 \_ 參數 \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)) 。</span><span class="sxs-lookup"><span data-stu-id="6acd4-118">A pointer to a parameter description (see [**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6acd4-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="6acd4-119">Return value</span></span>

<span data-ttu-id="6acd4-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6acd4-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6acd4-121">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="6acd4-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6acd4-122">備註</span><span class="sxs-lookup"><span data-stu-id="6acd4-122">Remarks</span></span>

<span data-ttu-id="6acd4-123">效果包含一或多個著色器;每個著色器都有輸入和輸出簽章;每個簽章都包含一或多個)  (或參數的元素。</span><span class="sxs-lookup"><span data-stu-id="6acd4-123">An effect contains one or more shaders; each shader has an input and output signature; each signature contains one or more elements (or parameters).</span></span> <span data-ttu-id="6acd4-124">著色器索引會識別著色器，而元素索引會識別著色器簽章中 (或參數) 的元素。</span><span class="sxs-lookup"><span data-stu-id="6acd4-124">The shader index identifies the shader and the element index identifies the element (or parameter) in the shader signature.</span></span>

> [!Note]  
> <span data-ttu-id="6acd4-125">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="6acd4-125">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6acd4-126">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6acd4-126">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6acd4-127">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="6acd4-127">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6acd4-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="6acd4-128">Requirements</span></span>



| <span data-ttu-id="6acd4-129">需求</span><span class="sxs-lookup"><span data-stu-id="6acd4-129">Requirement</span></span> | <span data-ttu-id="6acd4-130">值</span><span class="sxs-lookup"><span data-stu-id="6acd4-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6acd4-131">標頭</span><span class="sxs-lookup"><span data-stu-id="6acd4-131">Header</span></span><br/>  | <dl> <span data-ttu-id="6acd4-132"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="6acd4-132"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6acd4-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="6acd4-133">Library</span></span><br/> | <dl> <span data-ttu-id="6acd4-134"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="6acd4-134"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6acd4-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6acd4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6acd4-136">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="6acd4-136">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

