---
title: 'ID3DX11EffectPass GetDomainShaderDesc 方法 (D3dx11effect .h) '
description: 取得網域著色器描述。
ms.assetid: 02109930-0922-46b8-9381-bb75abd0c4a0
keywords:
- GetDomainShaderDesc 方法 Direct3D 11
- GetDomainShaderDesc 方法 Direct3D 11，ID3DX11EffectPass 介面
- ID3DX11EffectPass 介面 Direct3D 11，GetDomainShaderDesc 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetDomainShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2157134d97332fc9c76267f5e0db49d2c40e96a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974665"
---
# <a name="id3dx11effectpassgetdomainshaderdesc-method"></a><span data-ttu-id="627cf-106">ID3DX11EffectPass：： GetDomainShaderDesc 方法</span><span class="sxs-lookup"><span data-stu-id="627cf-106">ID3DX11EffectPass::GetDomainShaderDesc method</span></span>

<span data-ttu-id="627cf-107">取得網域著色器描述。</span><span class="sxs-lookup"><span data-stu-id="627cf-107">Get a domain-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="627cf-108">語法</span><span class="sxs-lookup"><span data-stu-id="627cf-108">Syntax</span></span>


```C++
HRESULT GetDomainShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="627cf-109">參數</span><span class="sxs-lookup"><span data-stu-id="627cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="627cf-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="627cf-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="627cf-111">類型： **[ **D3DX11 \_ PASS \_ 著色器 \_ DESC**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="627cf-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="627cf-112">網域著色器描述的指標 (參閱 [**D3DX11 \_ 傳遞 \_ 著色器 \_ DESC**](d3dx11-pass-shader-desc.md)) 。</span><span class="sxs-lookup"><span data-stu-id="627cf-112">A pointer to a domain-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="627cf-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="627cf-113">Return value</span></span>

<span data-ttu-id="627cf-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="627cf-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="627cf-115">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="627cf-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="627cf-116">備註</span><span class="sxs-lookup"><span data-stu-id="627cf-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="627cf-117">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="627cf-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="627cf-118">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="627cf-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="627cf-119">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="627cf-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="627cf-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="627cf-120">Requirements</span></span>



| <span data-ttu-id="627cf-121">需求</span><span class="sxs-lookup"><span data-stu-id="627cf-121">Requirement</span></span> | <span data-ttu-id="627cf-122">值</span><span class="sxs-lookup"><span data-stu-id="627cf-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="627cf-123">標頭</span><span class="sxs-lookup"><span data-stu-id="627cf-123">Header</span></span><br/>  | <dl> <span data-ttu-id="627cf-124"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="627cf-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="627cf-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="627cf-125">Library</span></span><br/> | <dl> <span data-ttu-id="627cf-126"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="627cf-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="627cf-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="627cf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="627cf-128">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="627cf-128">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





