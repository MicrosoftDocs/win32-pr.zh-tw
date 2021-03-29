---
title: 'D3DX11SaveTextureToFile 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用 DirectXTex 程式庫，CaptureTexture 接著 SaveToXXXFile (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。 針對從呈現目標材質建立螢幕擷取畫面的簡化案例，建議您使用 DirectXTK 程式庫 SaveDDSTextureToFile 或 SaveWICTextureToFile。 將材質儲存至檔案。
ms.assetid: da161268-fb68-42dd-ba31-b090a993f369
keywords:
- D3DX11SaveTextureToFile 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87188c3e58a8bea36b1cffb675c229aed71677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974588"
---
# <a name="d3dx11savetexturetofile-function"></a><span data-ttu-id="a209b-107">D3DX11SaveTextureToFile 函式</span><span class="sxs-lookup"><span data-stu-id="a209b-107">D3DX11SaveTextureToFile function</span></span>

> [!Note]  
> <span data-ttu-id="a209b-108">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a209b-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="a209b-109">我們建議您不要使用這個函式，而是使用 [DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫， **CaptureTexture** 接著 **SAVETOXXXFILE** (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。</span><span class="sxs-lookup"><span data-stu-id="a209b-109">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **CaptureTexture** then **SaveToXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span> <span data-ttu-id="a209b-110">針對從呈現目標材質建立螢幕擷取畫面的簡化案例，建議您使用 [DirectXTK](https://github.com/Microsoft/DirectXTK) 程式庫 **SaveDDSTextureToFile** 或 **SaveWICTextureToFile**。</span><span class="sxs-lookup"><span data-stu-id="a209b-110">For the simplified scenario of creating a screen shot from a render target texture, we recommend that you use the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SaveDDSTextureToFile** or **SaveWICTextureToFile**.</span></span>

 

<span data-ttu-id="a209b-111">將材質儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="a209b-111">Save a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a209b-112">語法</span><span class="sxs-lookup"><span data-stu-id="a209b-112">Syntax</span></span>


```C++
HRESULT D3DX11SaveTextureToFile(
       ID3D11DeviceContext      *pContext,
  _In_ ID3D11Resource           *pSrcTexture,
  _In_ D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a><span data-ttu-id="a209b-113">參數</span><span class="sxs-lookup"><span data-stu-id="a209b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a209b-114">*pContext*</span><span class="sxs-lookup"><span data-stu-id="a209b-114">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="a209b-115">類型： **[ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="a209b-115">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="a209b-116">[**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="a209b-116">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="a209b-117">*pSrcTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a209b-117">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a209b-118">類型： **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="a209b-118">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="a209b-119">要儲存的材質指標。</span><span class="sxs-lookup"><span data-stu-id="a209b-119">Pointer to the texture to be saved.</span></span> <span data-ttu-id="a209b-120">請參閱 [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)。</span><span class="sxs-lookup"><span data-stu-id="a209b-120">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="a209b-121">*DestFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a209b-121">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a209b-122">類型： **[ **D3DX11 \_ 圖像 \_ 檔案 \_ 格式**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="a209b-122">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

<span data-ttu-id="a209b-123">材質儲存格式的格式 (參閱 [**D3DX11 \_ 圖像 \_ 檔案 \_ 格式**](d3dx11-image-file-format.md)) 。</span><span class="sxs-lookup"><span data-stu-id="a209b-123">The format the texture will be saved as (see [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)).</span></span> <span data-ttu-id="a209b-124">D3DX11 \_ 如果 \_ DDS 是慣用的格式，因為它是唯一支援 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)格式的選項。</span><span class="sxs-lookup"><span data-stu-id="a209b-124">D3DX11\_IFF\_DDS is the preferred format since it is the only option that supports all the formats in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="a209b-125">*pDestFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a209b-125">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a209b-126">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a209b-126">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a209b-127">將儲存材質的目的地輸出檔名稱。</span><span class="sxs-lookup"><span data-stu-id="a209b-127">Name of the destination output file where the texture will be saved.</span></span> <span data-ttu-id="a209b-128">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="a209b-128">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="a209b-129">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="a209b-129">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a209b-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="a209b-130">Return value</span></span>

<span data-ttu-id="a209b-131">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a209b-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a209b-132">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值;使用傳回值來查看是否支援 *DestFormat* 。</span><span class="sxs-lookup"><span data-stu-id="a209b-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md); use the return value to see if the *DestFormat* is supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="a209b-133">備註</span><span class="sxs-lookup"><span data-stu-id="a209b-133">Remarks</span></span>

<span data-ttu-id="a209b-134">**D3DX11SaveTextureToFile** 只會在必要時為輸入材質寫出額外的 [**DDS \_ 標頭 \_ DXT10**](/windows/desktop/direct3ddds/dds-header-dxt10) 結構 (例如，因為輸入材質是在標準 RGB (sRGB) 格式) 。</span><span class="sxs-lookup"><span data-stu-id="a209b-134">**D3DX11SaveTextureToFile** writes out the extra [**DDS\_HEADER\_DXT10**](/windows/desktop/direct3ddds/dds-header-dxt10) structure for the input texture only if necessary (for example, because the input texture is in standard RGB (sRGB) format).</span></span> <span data-ttu-id="a209b-135">如果 **D3DX11SaveTextureToFile** 寫出 **dds \_ 標頭 \_ DXT10** 結構，則會將材質 [**\_ PIXELFORMAT**](/windows/desktop/direct3ddds/dds-pixelformat)結構的 **DwFourCC** 成員設定為 [ **DX10** ]，以指出 **DDS \_ 標頭 \_ prescense** 延伸標頭的 DXT10。</span><span class="sxs-lookup"><span data-stu-id="a209b-135">If **D3DX11SaveTextureToFile** writes out the **DDS\_HEADER\_DXT10** structure, it sets the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](/windows/desktop/direct3ddds/dds-pixelformat) structure for the texture to **DX10** to indicate the prescense of the **DDS\_HEADER\_DXT10** extended header.</span></span>

## <a name="requirements"></a><span data-ttu-id="a209b-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="a209b-136">Requirements</span></span>



| <span data-ttu-id="a209b-137">需求</span><span class="sxs-lookup"><span data-stu-id="a209b-137">Requirement</span></span> | <span data-ttu-id="a209b-138">值</span><span class="sxs-lookup"><span data-stu-id="a209b-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a209b-139">標頭</span><span class="sxs-lookup"><span data-stu-id="a209b-139">Header</span></span><br/>  | <dl> <span data-ttu-id="a209b-140"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="a209b-140"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a209b-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="a209b-141">Library</span></span><br/> | <dl> <span data-ttu-id="a209b-142"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a209b-142"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a209b-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a209b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a209b-144">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="a209b-144">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

