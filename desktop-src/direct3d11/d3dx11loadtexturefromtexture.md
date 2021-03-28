---
title: 'D3DX11LoadTextureFromTexture 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用此函式，而是使用 DirectXTex 程式庫、調整大小、轉換、壓縮、解壓縮和/或 CopyRectangle。 從材質載入紋理。
ms.assetid: 4e673f73-531d-4df8-8542-798e4e70c481
keywords:
- D3DX11LoadTextureFromTexture 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11LoadTextureFromTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246429433dea11fddfd4396f3e59677877081592
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974592"
---
# <a name="d3dx11loadtexturefromtexture-function"></a><span data-ttu-id="ed0ae-106">D3DX11LoadTextureFromTexture 函式</span><span class="sxs-lookup"><span data-stu-id="ed0ae-106">D3DX11LoadTextureFromTexture function</span></span>

> [!Note]  
> <span data-ttu-id="ed0ae-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ed0ae-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="ed0ae-108">我們建議您不要使用此函式，而是使用 [DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫、重 **設大小**、 **轉換**、 **壓縮**、 **解壓縮** 和/或 **CopyRectangle**。</span><span class="sxs-lookup"><span data-stu-id="ed0ae-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **Resize**, **Convert**, **Compress**, **Decompress**, and/or **CopyRectangle**.</span></span>

 

<span data-ttu-id="ed0ae-109">從材質載入紋理。</span><span class="sxs-lookup"><span data-stu-id="ed0ae-109">Load a texture from a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed0ae-110">語法</span><span class="sxs-lookup"><span data-stu-id="ed0ae-110">Syntax</span></span>


```C++
HRESULT D3DX11LoadTextureFromTexture(
   ID3D11DeviceContext      *pContext,
   ID3D11Resource           *pSrcTexture,
   D3DX11_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D11Resource           *pDstTexture
);
```



## <a name="parameters"></a><span data-ttu-id="ed0ae-111">參數</span><span class="sxs-lookup"><span data-stu-id="ed0ae-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed0ae-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="ed0ae-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="ed0ae-113">類型： **[ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="ed0ae-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="ed0ae-114">[**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="ed0ae-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="ed0ae-115">*pSrcTexture*</span><span class="sxs-lookup"><span data-stu-id="ed0ae-115">*pSrcTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="ed0ae-116">類型： **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="ed0ae-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="ed0ae-117">來源紋理的指標。</span><span class="sxs-lookup"><span data-stu-id="ed0ae-117">Pointer to the source texture.</span></span> <span data-ttu-id="ed0ae-118">請參閱 [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)。</span><span class="sxs-lookup"><span data-stu-id="ed0ae-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="ed0ae-119">*pLoadInfo*</span><span class="sxs-lookup"><span data-stu-id="ed0ae-119">*pLoadInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="ed0ae-120">類型： **[ **D3DX11 \_ 材質 \_ 載入 \_ 資訊**](d3dx11-texture-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed0ae-120">Type: **[**D3DX11\_TEXTURE\_LOAD\_INFO**](d3dx11-texture-load-info.md)\***</span></span>

<span data-ttu-id="ed0ae-121">材質載入參數的指標。</span><span class="sxs-lookup"><span data-stu-id="ed0ae-121">Pointer to texture loading parameters.</span></span> <span data-ttu-id="ed0ae-122">請參閱 [**D3DX11 \_ 材質 \_ 載入 \_ 資訊**](d3dx11-texture-load-info.md)。</span><span class="sxs-lookup"><span data-stu-id="ed0ae-122">See [**D3DX11\_TEXTURE\_LOAD\_INFO**](d3dx11-texture-load-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed0ae-123">*pDstTexture*</span><span class="sxs-lookup"><span data-stu-id="ed0ae-123">*pDstTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="ed0ae-124">類型： **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="ed0ae-124">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="ed0ae-125">目的地材質的指標。</span><span class="sxs-lookup"><span data-stu-id="ed0ae-125">Pointer to the destination texture.</span></span> <span data-ttu-id="ed0ae-126">請參閱 [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)。</span><span class="sxs-lookup"><span data-stu-id="ed0ae-126">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed0ae-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed0ae-127">Return value</span></span>

<span data-ttu-id="ed0ae-128">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed0ae-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed0ae-129">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ed0ae-129">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed0ae-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed0ae-130">Requirements</span></span>



| <span data-ttu-id="ed0ae-131">需求</span><span class="sxs-lookup"><span data-stu-id="ed0ae-131">Requirement</span></span> | <span data-ttu-id="ed0ae-132">值</span><span class="sxs-lookup"><span data-stu-id="ed0ae-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed0ae-133">標頭</span><span class="sxs-lookup"><span data-stu-id="ed0ae-133">Header</span></span><br/>  | <dl> <span data-ttu-id="ed0ae-134"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="ed0ae-134"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ed0ae-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="ed0ae-135">Library</span></span><br/> | <dl> <span data-ttu-id="ed0ae-136"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed0ae-136"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ed0ae-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed0ae-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed0ae-138">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="ed0ae-138">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





