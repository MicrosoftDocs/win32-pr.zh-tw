---
title: 'ID3DX11EffectShaderResourceVariable GetResourceArray 方法 (D3dx11effect .h) '
description: 取得著色器資源的陣列。
ms.assetid: 7540183d-dabb-46c2-8df1-6d4734b77f25
keywords:
- GetResourceArray 方法 Direct3D 11
- GetResourceArray 方法 Direct3D 11，ID3DX11EffectShaderResourceVariable 介面
- ID3DX11EffectShaderResourceVariable 介面 Direct3D 11，GetResourceArray 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable.GetResourceArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0091d81b7e157aecb8315e1def380800c8155c60
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946268"
---
# <a name="id3dx11effectshaderresourcevariablegetresourcearray-method"></a><span data-ttu-id="bd957-106">ID3DX11EffectShaderResourceVariable：： GetResourceArray 方法</span><span class="sxs-lookup"><span data-stu-id="bd957-106">ID3DX11EffectShaderResourceVariable::GetResourceArray method</span></span>

<span data-ttu-id="bd957-107">取得著色器資源的陣列。</span><span class="sxs-lookup"><span data-stu-id="bd957-107">Get an array of shader resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd957-108">語法</span><span class="sxs-lookup"><span data-stu-id="bd957-108">Syntax</span></span>


```C++
HRESULT GetResourceArray(
   ID3D11ShaderResourceView **ppResources,
   UINT                     Offset,
   UINT                     Count
);
```



## <a name="parameters"></a><span data-ttu-id="bd957-109">參數</span><span class="sxs-lookup"><span data-stu-id="bd957-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd957-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="bd957-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="bd957-111">類型： **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="bd957-111">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="bd957-112">著色器-資源檢視介面陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="bd957-112">The address of an array of shader-resource-view interfaces.</span></span> <span data-ttu-id="bd957-113">請參閱 [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)。</span><span class="sxs-lookup"><span data-stu-id="bd957-113">See [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="bd957-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="bd957-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="bd957-115">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bd957-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bd957-116">以零為基底的陣列索引，用來取得第一個介面。</span><span class="sxs-lookup"><span data-stu-id="bd957-116">The zero-based array index to get the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="bd957-117">*Count*</span><span class="sxs-lookup"><span data-stu-id="bd957-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="bd957-118">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="bd957-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="bd957-119">陣列中的項目數。</span><span class="sxs-lookup"><span data-stu-id="bd957-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd957-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd957-120">Return value</span></span>

<span data-ttu-id="bd957-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bd957-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bd957-122">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="bd957-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bd957-123">備註</span><span class="sxs-lookup"><span data-stu-id="bd957-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bd957-124">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="bd957-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="bd957-125">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="bd957-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="bd957-126">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="bd957-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bd957-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd957-127">Requirements</span></span>



| <span data-ttu-id="bd957-128">需求</span><span class="sxs-lookup"><span data-stu-id="bd957-128">Requirement</span></span> | <span data-ttu-id="bd957-129">值</span><span class="sxs-lookup"><span data-stu-id="bd957-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd957-130">標頭</span><span class="sxs-lookup"><span data-stu-id="bd957-130">Header</span></span><br/>  | <dl> <span data-ttu-id="bd957-131"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="bd957-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="bd957-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="bd957-132">Library</span></span><br/> | <dl> <span data-ttu-id="bd957-133"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="bd957-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd957-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd957-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd957-135">ID3DX11EffectShaderResourceVariable</span><span class="sxs-lookup"><span data-stu-id="bd957-135">ID3DX11EffectShaderResourceVariable</span></span>](id3dx11effectshaderresourcevariable.md)
</dt> </dl>

 

