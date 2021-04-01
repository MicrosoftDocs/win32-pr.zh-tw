---
title: 'ID3DX11EffectShaderResourceVariable GetResource 方法 (D3dx11effect .h) '
description: 取得著色器資源。
ms.assetid: 7c56aba0-ce60-4b50-9c1a-802bf1d73c6b
keywords:
- GetResource 方法 Direct3D 11
- GetResource 方法 Direct3D 11，ID3DX11EffectShaderResourceVariable 介面
- ID3DX11EffectShaderResourceVariable 介面 Direct3D 11，GetResource 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.GetResource
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea841ae63646958603396d5b65305c242961942
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196189"
---
# <a name="id3dx11effectshaderresourcevariablegetresource-method"></a><span data-ttu-id="9eed2-106">ID3DX11EffectShaderResourceVariable：： GetResource 方法</span><span class="sxs-lookup"><span data-stu-id="9eed2-106">ID3DX11EffectShaderResourceVariable::GetResource method</span></span>

<span data-ttu-id="9eed2-107">取得著色器資源。</span><span class="sxs-lookup"><span data-stu-id="9eed2-107">Get a shader resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eed2-108">語法</span><span class="sxs-lookup"><span data-stu-id="9eed2-108">Syntax</span></span>


```C++
HRESULT GetResource(
   ID3D11ShaderResourceView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="9eed2-109">參數</span><span class="sxs-lookup"><span data-stu-id="9eed2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eed2-110">*ppResource*</span><span class="sxs-lookup"><span data-stu-id="9eed2-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="9eed2-111">類型： **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="9eed2-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="9eed2-112">著色器資源-view 介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="9eed2-112">The address of a pointer to a shader-resource-view interface.</span></span> <span data-ttu-id="9eed2-113">請參閱 [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)。</span><span class="sxs-lookup"><span data-stu-id="9eed2-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eed2-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9eed2-114">Return value</span></span>

<span data-ttu-id="9eed2-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9eed2-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9eed2-116">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="9eed2-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9eed2-117">備註</span><span class="sxs-lookup"><span data-stu-id="9eed2-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9eed2-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="9eed2-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9eed2-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="9eed2-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9eed2-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="9eed2-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9eed2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="9eed2-121">Requirements</span></span>



| <span data-ttu-id="9eed2-122">需求</span><span class="sxs-lookup"><span data-stu-id="9eed2-122">Requirement</span></span> | <span data-ttu-id="9eed2-123">值</span><span class="sxs-lookup"><span data-stu-id="9eed2-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eed2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="9eed2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9eed2-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="9eed2-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9eed2-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="9eed2-126">Library</span></span><br/> | <dl> <span data-ttu-id="9eed2-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="9eed2-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eed2-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9eed2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eed2-129">ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="9eed2-129">ID3DX11EffectShaderResourceVariable</span></span>](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

 





