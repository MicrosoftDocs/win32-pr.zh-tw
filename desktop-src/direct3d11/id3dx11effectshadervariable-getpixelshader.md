---
title: 'ID3DX11EffectShaderVariable GetPixelShader 方法 (D3dx11effect .h) '
description: 取得圖元著色器。
ms.assetid: 4ce4b248-23b9-4135-a2b4-262e63247688
keywords:
- GetPixelShader 方法 Direct3D 11
- GetPixelShader 方法 Direct3D 11，ID3DX11EffectShaderVariable 介面
- ID3DX11EffectShaderVariable 介面 Direct3D 11，GetPixelShader 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPixelShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6588fd9afb7e58308f0fbc120705d4a22d9f2ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514676"
---
# <a name="id3dx11effectshadervariablegetpixelshader-method"></a><span data-ttu-id="c3a2d-106">ID3DX11EffectShaderVariable：： GetPixelShader 方法</span><span class="sxs-lookup"><span data-stu-id="c3a2d-106">ID3DX11EffectShaderVariable::GetPixelShader method</span></span>

<span data-ttu-id="c3a2d-107">取得圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="c3a2d-107">Get a pixel shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a2d-108">語法</span><span class="sxs-lookup"><span data-stu-id="c3a2d-108">Syntax</span></span>


```C++
HRESULT GetPixelShader(
   UINT              ShaderIndex,
   ID3D11PixelShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="c3a2d-109">參數</span><span class="sxs-lookup"><span data-stu-id="c3a2d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3a2d-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="c3a2d-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="c3a2d-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c3a2d-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c3a2d-112">以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="c3a2d-112">A zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="c3a2d-113">*ppPS*</span><span class="sxs-lookup"><span data-stu-id="c3a2d-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="c3a2d-114">類型： **[ **ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="c3a2d-114">Type: **[**ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader)\*\***</span></span>

<span data-ttu-id="c3a2d-115">[**ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader)指標的指標，會在傳回時設定為圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="c3a2d-115">A pointer to an [**ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader) pointer that will be set to the pixel shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3a2d-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3a2d-116">Return value</span></span>

<span data-ttu-id="c3a2d-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3a2d-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3a2d-118">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="c3a2d-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c3a2d-119">備註</span><span class="sxs-lookup"><span data-stu-id="c3a2d-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c3a2d-120">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="c3a2d-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c3a2d-121">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c3a2d-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c3a2d-122">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="c3a2d-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c3a2d-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3a2d-123">Requirements</span></span>



| <span data-ttu-id="c3a2d-124">需求</span><span class="sxs-lookup"><span data-stu-id="c3a2d-124">Requirement</span></span> | <span data-ttu-id="c3a2d-125">值</span><span class="sxs-lookup"><span data-stu-id="c3a2d-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a2d-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c3a2d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c3a2d-127"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="c3a2d-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c3a2d-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="c3a2d-128">Library</span></span><br/> | <dl> <span data-ttu-id="c3a2d-129"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="c3a2d-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3a2d-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3a2d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a2d-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="c3a2d-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

