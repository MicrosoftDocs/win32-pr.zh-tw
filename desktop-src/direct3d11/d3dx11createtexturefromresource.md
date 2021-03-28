---
title: 'D3DX11CreateTextureFromResource 函式 (D3DX11) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用此函式，而是使用資源函式，然後這些 DirectXTK 程式庫 (runtime) 、CreateXXXTextureFromMemory (其中 XXX 是 DDS 或 WIC) DirectXTex 程式庫 (工具) 、LoadFromXXXMemory (，其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲的常見藝術來源格式) 然後 CreateTexture 從另一個資源建立紋理。
ms.assetid: 2b62239a-c19b-4d4f-9fd2-afcd87ba0fac
keywords:
- D3DX11CreateTextureFromResource 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bea89fe4f8bf6632ada9461b048195335c72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196372"
---
# <a name="d3dx11createtexturefromresource-function"></a><span data-ttu-id="eb722-105">D3DX11CreateTextureFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="eb722-105">D3DX11CreateTextureFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="eb722-106">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="eb722-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="eb722-107">我們建議您不要使用此函式，而是使用 [資源](/windows/desktop/menurc/resources-functions)函式，如下所示：</span><span class="sxs-lookup"><span data-stu-id="eb722-107">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then these:</span></span>
>
> -   <span data-ttu-id="eb722-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) 程式庫 (runtime) 、 **CreateXXXTextureFromMemory** (，其中 XXX 是 DDS 或 WIC) </span><span class="sxs-lookup"><span data-stu-id="eb722-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromMemory** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="eb722-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫 (工具) 、 **LOADFROMXXXMEMORY** (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 **CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="eb722-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateTexture**</span></span>

 

<span data-ttu-id="eb722-110">建立另一個資源的材質。</span><span class="sxs-lookup"><span data-stu-id="eb722-110">Create a texture from another resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb722-111">語法</span><span class="sxs-lookup"><span data-stu-id="eb722-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateTextureFromResource(
  _In_  ID3D11Device           *pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="eb722-112">參數</span><span class="sxs-lookup"><span data-stu-id="eb722-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb722-113">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb722-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb722-114">類型： **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="eb722-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="eb722-115">裝置的指標 (查看將使用該資源的 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) 。</span><span class="sxs-lookup"><span data-stu-id="eb722-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="eb722-116">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb722-116">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb722-117">類型： **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eb722-117">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eb722-118">來源資源的控制碼。</span><span class="sxs-lookup"><span data-stu-id="eb722-118">A handle to the source resource.</span></span> <span data-ttu-id="eb722-119">您可以使用 [GetModuleHandle 函數](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)來取得 HMODULE。</span><span class="sxs-lookup"><span data-stu-id="eb722-119">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="eb722-120">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb722-120">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb722-121">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="eb722-121">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="eb722-122">包含來源資源名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="eb722-122">A string that contains the name of the source resource.</span></span> <span data-ttu-id="eb722-123">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="eb722-123">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="eb722-124">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="eb722-124">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="eb722-125">*pLoadInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb722-125">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb722-126">類型： **[ **D3DX11 \_ 映射 \_ 載入 \_ 資訊**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb722-126">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="eb722-127">選擇性。</span><span class="sxs-lookup"><span data-stu-id="eb722-127">Optional.</span></span> <span data-ttu-id="eb722-128">識別材質的特性 (請參閱資料處理器建立時) [**D3DX11 \_ 影像 \_ 載入 \_ 資訊**](d3dx11-image-load-info.md) ; 將此值設定為 **Null** ，以在載入紋理時讀取紋理的特性。</span><span class="sxs-lookup"><span data-stu-id="eb722-128">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="eb722-129">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb722-129">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb722-130">類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb722-130">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="eb722-131">執行緒抽取介面的指標 (查看 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="eb722-131">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="eb722-132">如果指定 **Null** ，此函式會以同步方式運作，直到完成為止才會傳回。</span><span class="sxs-lookup"><span data-stu-id="eb722-132">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="eb722-133">*ppTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="eb722-133">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb722-134">類型： **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="eb722-134">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span></span>

<span data-ttu-id="eb722-135">材質資源指標的位址 (參閱 [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)) 。</span><span class="sxs-lookup"><span data-stu-id="eb722-135">The address of a pointer to the texture resource (see [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)).</span></span>

</dd> <dt>

<span data-ttu-id="eb722-136">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="eb722-136">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb722-137">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="eb722-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="eb722-138">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="eb722-138">A pointer to the return value.</span></span> <span data-ttu-id="eb722-139">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="eb722-139">May be **NULL**.</span></span> <span data-ttu-id="eb722-140">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="eb722-140">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb722-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb722-141">Return value</span></span>

<span data-ttu-id="eb722-142">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eb722-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eb722-143">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="eb722-143">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb722-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb722-144">Requirements</span></span>



| <span data-ttu-id="eb722-145">需求</span><span class="sxs-lookup"><span data-stu-id="eb722-145">Requirement</span></span> | <span data-ttu-id="eb722-146">值</span><span class="sxs-lookup"><span data-stu-id="eb722-146">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb722-147">標頭</span><span class="sxs-lookup"><span data-stu-id="eb722-147">Header</span></span><br/>  | <dl> <span data-ttu-id="eb722-148"><dt>D3DX11。h</dt></span><span class="sxs-lookup"><span data-stu-id="eb722-148"><dt>D3DX11.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb722-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="eb722-149">Library</span></span><br/> | <dl> <span data-ttu-id="eb722-150"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb722-150"><dt>D3DX11.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb722-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb722-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb722-152">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="eb722-152">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

