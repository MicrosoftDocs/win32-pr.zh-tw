---
title: 'D3DX11FilterTexture 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用此函式，而是使用 DirectXTex 程式庫 GenerateMipMaps 和 GenerateMipMaps3D。 使用特定的材質篩選器產生 mipmap 鏈。
ms.assetid: 52ae3228-f9d7-4944-b49c-55df1816f1f7
keywords:
- D3DX11FilterTexture 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11FilterTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e74e60e9d66e2a5251c161e4df6451266d3fb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974600"
---
# <a name="d3dx11filtertexture-function"></a><span data-ttu-id="7ad2d-106">D3DX11FilterTexture 函式</span><span class="sxs-lookup"><span data-stu-id="7ad2d-106">D3DX11FilterTexture function</span></span>

> [!Note]  
> <span data-ttu-id="7ad2d-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="7ad2d-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="7ad2d-108">我們建議您不要使用此函式，而是使用 [DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫 **GenerateMipMaps** 和 **GenerateMipMaps3D**。</span><span class="sxs-lookup"><span data-stu-id="7ad2d-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GenerateMipMaps** and **GenerateMipMaps3D**.</span></span>

 

<span data-ttu-id="7ad2d-109">使用特定的材質篩選器產生 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="7ad2d-109">Generates mipmap chain using a particular texture filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ad2d-110">語法</span><span class="sxs-lookup"><span data-stu-id="7ad2d-110">Syntax</span></span>


```C++
HRESULT D3DX11FilterTexture(
   ID3D11DeviceContext *pContext,
   ID3D11Resource      *pTexture,
   UINT                SrcLevel,
   UINT                MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="7ad2d-111">參數</span><span class="sxs-lookup"><span data-stu-id="7ad2d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ad2d-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="7ad2d-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="7ad2d-113">類型： **[ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="7ad2d-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="7ad2d-114">[**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="7ad2d-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="7ad2d-115">*pTexture*</span><span class="sxs-lookup"><span data-stu-id="7ad2d-115">*pTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="7ad2d-116">類型： **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="7ad2d-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="7ad2d-117">要篩選的材質物件。</span><span class="sxs-lookup"><span data-stu-id="7ad2d-117">The texture object to be filtered.</span></span> <span data-ttu-id="7ad2d-118">請參閱 [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)。</span><span class="sxs-lookup"><span data-stu-id="7ad2d-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="7ad2d-119">*SrcLevel*</span><span class="sxs-lookup"><span data-stu-id="7ad2d-119">*SrcLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="7ad2d-120">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7ad2d-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7ad2d-121">Mipmap 層級的資料會用來產生 mipmap 鏈的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="7ad2d-121">The mipmap level whose data is used to generate the rest of the mipmap chain.</span></span>

</dd> <dt>

<span data-ttu-id="7ad2d-122">*MipFilter*</span><span class="sxs-lookup"><span data-stu-id="7ad2d-122">*MipFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="7ad2d-123">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7ad2d-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="7ad2d-124">旗標，控制每個 miplevel 的篩選方式 (或 D3DX11 \_ D3DX11 \_ 篩選線性) 的預設值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7ad2d-124">Flags controlling how each miplevel is filtered (or D3DX11\_DEFAULT for D3DX11\_FILTER\_LINEAR).</span></span> <span data-ttu-id="7ad2d-125">請參閱 [**D3DX11 \_ 篩選 \_ 旗**](d3dx11-filter-flag.md)標。</span><span class="sxs-lookup"><span data-stu-id="7ad2d-125">See [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ad2d-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="7ad2d-126">Return value</span></span>

<span data-ttu-id="7ad2d-127">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ad2d-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ad2d-128">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7ad2d-128">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ad2d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ad2d-129">Requirements</span></span>



| <span data-ttu-id="7ad2d-130">需求</span><span class="sxs-lookup"><span data-stu-id="7ad2d-130">Requirement</span></span> | <span data-ttu-id="7ad2d-131">值</span><span class="sxs-lookup"><span data-stu-id="7ad2d-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad2d-132">標頭</span><span class="sxs-lookup"><span data-stu-id="7ad2d-132">Header</span></span><br/>  | <dl> <span data-ttu-id="7ad2d-133"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ad2d-133"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="7ad2d-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="7ad2d-134">Library</span></span><br/> | <dl> <span data-ttu-id="7ad2d-135"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ad2d-135"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7ad2d-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ad2d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ad2d-137">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="7ad2d-137">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

