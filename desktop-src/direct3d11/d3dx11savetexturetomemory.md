---
title: 'D3DX11SaveTextureToMemory 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用 DirectXTex 程式庫，CaptureTexture 接著 SaveToXXXMemory (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。 將材質儲存至記憶體。
ms.assetid: 3b54d8e1-6474-48fd-8348-a3baac406101
keywords:
- D3DX11SaveTextureToMemory 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4718f32f8d8288f83b30e3d742ebbe619421dc48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196370"
---
# <a name="d3dx11savetexturetomemory-function"></a><span data-ttu-id="1bb59-106">D3DX11SaveTextureToMemory 函式</span><span class="sxs-lookup"><span data-stu-id="1bb59-106">D3DX11SaveTextureToMemory function</span></span>

> [!Note]  
> <span data-ttu-id="1bb59-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="1bb59-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="1bb59-108">我們建議您不要使用這個函式，而是使用 [DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫， **CaptureTexture** 接著 **SAVETOXXXMEMORY** (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。</span><span class="sxs-lookup"><span data-stu-id="1bb59-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **CaptureTexture** then **SaveToXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="1bb59-109">將材質儲存至記憶體。</span><span class="sxs-lookup"><span data-stu-id="1bb59-109">Save a texture to memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bb59-110">語法</span><span class="sxs-lookup"><span data-stu-id="1bb59-110">Syntax</span></span>


```C++
HRESULT D3DX11SaveTextureToMemory(
        ID3D11DeviceContext      *pContext,
  _In_  ID3D11Resource           *pSrcTexture,
  _In_  D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="1bb59-111">參數</span><span class="sxs-lookup"><span data-stu-id="1bb59-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bb59-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="1bb59-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="1bb59-113">類型： **[ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="1bb59-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="1bb59-114">[**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="1bb59-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="1bb59-115">*pSrcTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1bb59-115">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb59-116">類型： **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="1bb59-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="1bb59-117">要儲存的材質指標。</span><span class="sxs-lookup"><span data-stu-id="1bb59-117">Pointer to the texture to be saved.</span></span> <span data-ttu-id="1bb59-118">請參閱 [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)。</span><span class="sxs-lookup"><span data-stu-id="1bb59-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="1bb59-119">*DestFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1bb59-119">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb59-120">類型： **[ **D3DX11 \_ 圖像 \_ 檔案 \_ 格式**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="1bb59-120">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

<span data-ttu-id="1bb59-121">材質將儲存成的格式。</span><span class="sxs-lookup"><span data-stu-id="1bb59-121">The format the texture will be saved as.</span></span> <span data-ttu-id="1bb59-122">請參閱 [**D3DX11 \_ 影像檔案 \_ \_ 格式**](d3dx11-image-file-format.md)。</span><span class="sxs-lookup"><span data-stu-id="1bb59-122">See [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md).</span></span>

</dd> <dt>

<span data-ttu-id="1bb59-123">*ppDestBuf* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1bb59-123">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb59-124">類型： **[ **LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="1bb59-124">Type: **[**LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="1bb59-125">包含已儲存材質之記憶體的指標位址。</span><span class="sxs-lookup"><span data-stu-id="1bb59-125">Address of a pointer to the memory containing the saved texture.</span></span>

</dd> <dt>

<span data-ttu-id="1bb59-126">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="1bb59-126">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bb59-127">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1bb59-127">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1bb59-128">選擇性。</span><span class="sxs-lookup"><span data-stu-id="1bb59-128">Optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bb59-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="1bb59-129">Return value</span></span>

<span data-ttu-id="1bb59-130">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1bb59-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1bb59-131">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1bb59-131">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1bb59-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bb59-132">Requirements</span></span>



| <span data-ttu-id="1bb59-133">需求</span><span class="sxs-lookup"><span data-stu-id="1bb59-133">Requirement</span></span> | <span data-ttu-id="1bb59-134">值</span><span class="sxs-lookup"><span data-stu-id="1bb59-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bb59-135">標頭</span><span class="sxs-lookup"><span data-stu-id="1bb59-135">Header</span></span><br/>  | <dl> <span data-ttu-id="1bb59-136"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="1bb59-136"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="1bb59-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="1bb59-137">Library</span></span><br/> | <dl> <span data-ttu-id="1bb59-138"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bb59-138"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1bb59-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1bb59-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bb59-140">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="1bb59-140">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

