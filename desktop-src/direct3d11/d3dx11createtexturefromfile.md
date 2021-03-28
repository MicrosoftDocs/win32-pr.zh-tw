---
title: 'D3DX11CreateTextureFromFile 函式 (D3DX11) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用這些 DirectXTK 程式庫 (runtime) 、CreateXXXTextureFromFile (其中 XXX 是 DDS 或 WIC) DirectXTex 程式庫 (工具) 、LoadFromXXXFile (，其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 CreateTexture 從檔案建立材質資源。
ms.assetid: a84ea166-2296-48d9-a028-b65fd68f2371
keywords:
- D3DX11CreateTextureFromFile 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6ab9bedcfe44238938e47ccb402738d2694b061
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992274"
---
# <a name="d3dx11createtexturefromfile-function"></a><span data-ttu-id="a62d2-105">D3DX11CreateTextureFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="a62d2-105">D3DX11CreateTextureFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="a62d2-106">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a62d2-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="a62d2-107">我們建議您不要使用這個函式，而是使用下列功能：</span><span class="sxs-lookup"><span data-stu-id="a62d2-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="a62d2-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) 程式庫 (runtime) 、 **CreateXXXTextureFromFile** (，其中 XXX 是 DDS 或 WIC) </span><span class="sxs-lookup"><span data-stu-id="a62d2-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromFile** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="a62d2-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫 (工具) 、 **LOADFROMXXXFILE** (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 **CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="a62d2-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateTexture**</span></span>

 

<span data-ttu-id="a62d2-110">從檔案建立材質資源。</span><span class="sxs-lookup"><span data-stu-id="a62d2-110">Create a texture resource from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a62d2-111">語法</span><span class="sxs-lookup"><span data-stu-id="a62d2-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateTextureFromFile(
  _In_  ID3D11Device           *pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="a62d2-112">參數</span><span class="sxs-lookup"><span data-stu-id="a62d2-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a62d2-113">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a62d2-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a62d2-114">類型： **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="a62d2-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="a62d2-115">裝置的指標 (查看將使用該資源的 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) 。</span><span class="sxs-lookup"><span data-stu-id="a62d2-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="a62d2-116">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a62d2-116">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a62d2-117">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a62d2-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a62d2-118">包含資源的檔案名。</span><span class="sxs-lookup"><span data-stu-id="a62d2-118">The name of the file containing the resource.</span></span> <span data-ttu-id="a62d2-119">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="a62d2-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="a62d2-120">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="a62d2-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="a62d2-121">*pLoadInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a62d2-121">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a62d2-122">類型： **[ **D3DX11 \_ 映射 \_ 載入 \_ 資訊**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a62d2-122">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="a62d2-123">選擇性。</span><span class="sxs-lookup"><span data-stu-id="a62d2-123">Optional.</span></span> <span data-ttu-id="a62d2-124">識別材質的特性 (請參閱資料處理器建立時) [**D3DX11 \_ 影像 \_ 載入 \_ 資訊**](d3dx11-image-load-info.md) ; 將此值設定為 **Null** ，以在載入紋理時讀取紋理的特性。</span><span class="sxs-lookup"><span data-stu-id="a62d2-124">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="a62d2-125">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a62d2-125">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a62d2-126">類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="a62d2-126">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="a62d2-127">執行緒抽取介面的指標 (查看 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="a62d2-127">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="a62d2-128">如果指定 **Null** ，此函式會以同步方式運作，直到完成為止才會傳回。</span><span class="sxs-lookup"><span data-stu-id="a62d2-128">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="a62d2-129">*ppTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a62d2-129">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a62d2-130">類型： **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="a62d2-130">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span></span>

<span data-ttu-id="a62d2-131">材質資源指標的位址 (參閱 [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)) 。</span><span class="sxs-lookup"><span data-stu-id="a62d2-131">The address of a pointer to the texture resource (see [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)).</span></span>

</dd> <dt>

<span data-ttu-id="a62d2-132">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a62d2-132">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a62d2-133">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="a62d2-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="a62d2-134">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="a62d2-134">A pointer to the return value.</span></span> <span data-ttu-id="a62d2-135">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a62d2-135">May be **NULL**.</span></span> <span data-ttu-id="a62d2-136">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="a62d2-136">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a62d2-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="a62d2-137">Return value</span></span>

<span data-ttu-id="a62d2-138">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a62d2-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a62d2-139">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a62d2-139">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a62d2-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="a62d2-140">Requirements</span></span>



| <span data-ttu-id="a62d2-141">需求</span><span class="sxs-lookup"><span data-stu-id="a62d2-141">Requirement</span></span> | <span data-ttu-id="a62d2-142">值</span><span class="sxs-lookup"><span data-stu-id="a62d2-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a62d2-143">標頭</span><span class="sxs-lookup"><span data-stu-id="a62d2-143">Header</span></span><br/>  | <dl> <span data-ttu-id="a62d2-144"><dt>D3DX11。h</dt></span><span class="sxs-lookup"><span data-stu-id="a62d2-144"><dt>D3DX11.h</dt></span></span> </dl>   |
| <span data-ttu-id="a62d2-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="a62d2-145">Library</span></span><br/> | <dl> <span data-ttu-id="a62d2-146"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a62d2-146"><dt>D3DX11.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a62d2-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a62d2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a62d2-148">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="a62d2-148">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

