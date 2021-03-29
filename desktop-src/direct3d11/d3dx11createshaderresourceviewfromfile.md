---
title: 'D3DX11CreateShaderResourceViewFromFile 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用這些 DirectXTK 程式庫 (runtime) 、CreateXXXTextureFromFile (其中 XXX 是 DDS 或 WIC) DirectXTex 程式庫 (工具) 、LoadFromXXXFile (，其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 CreateShaderResourceView 從檔案建立著色器資源檢視。
ms.assetid: c6a23503-f511-49dc-a0dc-19932cf8f313
keywords:
- D3DX11CreateShaderResourceViewFromFile 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05e7d710b0b379f3027591c2ff9e52c2fdd0d7a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323116"
---
# <a name="d3dx11createshaderresourceviewfromfile-function"></a><span data-ttu-id="cd072-105">D3DX11CreateShaderResourceViewFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="cd072-105">D3DX11CreateShaderResourceViewFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="cd072-106">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="cd072-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="cd072-107">我們建議您不要使用這個函式，而是使用下列功能：</span><span class="sxs-lookup"><span data-stu-id="cd072-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="cd072-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) 程式庫 (runtime) 、 **CreateXXXTextureFromFile** (，其中 XXX 是 DDS 或 WIC) </span><span class="sxs-lookup"><span data-stu-id="cd072-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromFile** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="cd072-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫 (工具) 、 **LOADFROMXXXFILE** (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 **CreateShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="cd072-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateShaderResourceView**</span></span>

 

<span data-ttu-id="cd072-110">從檔案建立著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="cd072-110">Create a shader-resource view from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd072-111">語法</span><span class="sxs-lookup"><span data-stu-id="cd072-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateShaderResourceViewFromFile(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="cd072-112">參數</span><span class="sxs-lookup"><span data-stu-id="cd072-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd072-113">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd072-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd072-114">類型： **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="cd072-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="cd072-115">裝置的指標 (查看將使用該資源的 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) 。</span><span class="sxs-lookup"><span data-stu-id="cd072-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="cd072-116">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd072-116">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd072-117">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cd072-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cd072-118">包含著色器資源檢視的檔案名。</span><span class="sxs-lookup"><span data-stu-id="cd072-118">Name of the file that contains the shader-resource view.</span></span> <span data-ttu-id="cd072-119">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="cd072-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="cd072-120">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="cd072-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="cd072-121">*pLoadInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd072-121">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd072-122">類型： **[ **D3DX11 \_ 映射 \_ 載入 \_ 資訊**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd072-122">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="cd072-123">選擇性。</span><span class="sxs-lookup"><span data-stu-id="cd072-123">Optional.</span></span> <span data-ttu-id="cd072-124">識別材質的特性 (請參閱資料處理器建立時) [**D3DX11 \_ 影像 \_ 載入 \_ 資訊**](d3dx11-image-load-info.md) ; 將此值設定為 **Null** ，以在載入紋理時讀取紋理的特性。</span><span class="sxs-lookup"><span data-stu-id="cd072-124">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="cd072-125">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd072-125">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd072-126">類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="cd072-126">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="cd072-127">執行緒抽取介面的指標 (查看 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="cd072-127">Pointer to a thread-pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="cd072-128">如果指定 **Null** ，此函式會以同步方式運作，直到完成為止才會傳回。</span><span class="sxs-lookup"><span data-stu-id="cd072-128">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="cd072-129">*ppShaderResourceView* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cd072-129">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd072-130">類型： **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="cd072-130">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="cd072-131">指向著色器資源檢視之指標的位址 (參閱 [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)) 。</span><span class="sxs-lookup"><span data-stu-id="cd072-131">Address of a pointer to the shader-resource view (see [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="cd072-132">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cd072-132">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd072-133">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="cd072-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="cd072-134">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="cd072-134">A pointer to the return value.</span></span> <span data-ttu-id="cd072-135">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="cd072-135">May be **NULL**.</span></span> <span data-ttu-id="cd072-136">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="cd072-136">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd072-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd072-137">Return value</span></span>

<span data-ttu-id="cd072-138">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cd072-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cd072-139">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="cd072-139">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cd072-140">備註</span><span class="sxs-lookup"><span data-stu-id="cd072-140">Remarks</span></span>

<span data-ttu-id="cd072-141">如需支援的影像格式清單，請參閱 [**D3DX11 \_ 影像檔案 \_ \_ 格式**](d3dx11-image-file-format.md)。</span><span class="sxs-lookup"><span data-stu-id="cd072-141">For a list of supported image formats, see [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd072-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd072-142">Requirements</span></span>



| <span data-ttu-id="cd072-143">需求</span><span class="sxs-lookup"><span data-stu-id="cd072-143">Requirement</span></span> | <span data-ttu-id="cd072-144">值</span><span class="sxs-lookup"><span data-stu-id="cd072-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd072-145">標頭</span><span class="sxs-lookup"><span data-stu-id="cd072-145">Header</span></span><br/>  | <dl> <span data-ttu-id="cd072-146"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="cd072-146"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="cd072-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="cd072-147">Library</span></span><br/> | <dl> <span data-ttu-id="cd072-148"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd072-148"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="cd072-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd072-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd072-150">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="cd072-150">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

