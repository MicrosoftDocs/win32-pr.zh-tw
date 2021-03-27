---
title: 'D3DX11CreateTextureFromMemory 函式 (D3DX11) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用這些 DirectXTK 程式庫 (runtime) 、CreateXXXTextureFromMemory (其中 XXX 是 DDS 或 WIC) DirectXTex 程式庫 (工具) 、LoadFromXXXMemory (，其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲的常見藝術來源格式) 然後 CreateTexture 從位於系統記憶體中的檔案建立材質資源。
ms.assetid: 1b07653e-8dc8-40b2-b591-bd25a54cfaa2
keywords:
- D3DX11CreateTextureFromMemory 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateTextureFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99987e882430da7f5e884f1b22e890947f7105e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946178"
---
# <a name="d3dx11createtexturefrommemory-function"></a><span data-ttu-id="b7726-105">D3DX11CreateTextureFromMemory 函式</span><span class="sxs-lookup"><span data-stu-id="b7726-105">D3DX11CreateTextureFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="b7726-106">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="b7726-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="b7726-107">我們建議您不要使用這個函式，而是使用下列功能：</span><span class="sxs-lookup"><span data-stu-id="b7726-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="b7726-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) 程式庫 (runtime) 、 **CreateXXXTextureFromMemory** (，其中 XXX 是 DDS 或 WIC) </span><span class="sxs-lookup"><span data-stu-id="b7726-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromMemory** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="b7726-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫 (工具) 、 **LOADFROMXXXMEMORY** (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援的 TGA 做為遊戲的常用藝術來源格式) 然後 **CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="b7726-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateTexture**</span></span>

 

<span data-ttu-id="b7726-110">從位於系統記憶體中的檔案建立材質資源。</span><span class="sxs-lookup"><span data-stu-id="b7726-110">Create a texture resource from a file residing in system memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7726-111">語法</span><span class="sxs-lookup"><span data-stu-id="b7726-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateTextureFromMemory(
  _In_  ID3D11Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX11ThreadPump      *pPump,
  _Out_ ID3D11Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="b7726-112">參數</span><span class="sxs-lookup"><span data-stu-id="b7726-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7726-113">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7726-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7726-114">類型： **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="b7726-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="b7726-115">裝置的指標 (查看將使用該資源的 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) 。</span><span class="sxs-lookup"><span data-stu-id="b7726-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="b7726-116">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7726-116">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7726-117">類型： **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b7726-117">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b7726-118">系統記憶體中資源的指標。</span><span class="sxs-lookup"><span data-stu-id="b7726-118">Pointer to the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="b7726-119">*SrcDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7726-119">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7726-120">類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b7726-120">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b7726-121">系統記憶體中資源的大小。</span><span class="sxs-lookup"><span data-stu-id="b7726-121">Size of the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="b7726-122">*pLoadInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7726-122">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7726-123">類型： **[ **D3DX11 \_ 映射 \_ 載入 \_ 資訊**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="b7726-123">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="b7726-124">選擇性。</span><span class="sxs-lookup"><span data-stu-id="b7726-124">Optional.</span></span> <span data-ttu-id="b7726-125">識別材質的特性 (請參閱資料處理器建立時) [**D3DX11 \_ 影像 \_ 載入 \_ 資訊**](d3dx11-image-load-info.md) ; 將此值設定為 **Null** ，以在載入紋理時讀取紋理的特性。</span><span class="sxs-lookup"><span data-stu-id="b7726-125">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="b7726-126">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7726-126">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7726-127">類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="b7726-127">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="b7726-128">執行緒抽取介面的指標 (查看 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="b7726-128">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="b7726-129">如果指定 **Null** ，此函式會以同步方式運作，直到完成為止才會傳回。</span><span class="sxs-lookup"><span data-stu-id="b7726-129">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="b7726-130">*ppTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b7726-130">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7726-131">類型： **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="b7726-131">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\*\***</span></span>

<span data-ttu-id="b7726-132">所建立資源指標的位址。</span><span class="sxs-lookup"><span data-stu-id="b7726-132">Address of a pointer to the created resource.</span></span> <span data-ttu-id="b7726-133">請參閱 [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)。</span><span class="sxs-lookup"><span data-stu-id="b7726-133">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="b7726-134">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b7726-134">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7726-135">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="b7726-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="b7726-136">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="b7726-136">A pointer to the return value.</span></span> <span data-ttu-id="b7726-137">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b7726-137">May be **NULL**.</span></span> <span data-ttu-id="b7726-138">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="b7726-138">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7726-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7726-139">Return value</span></span>

<span data-ttu-id="b7726-140">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7726-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7726-141">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b7726-141">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7726-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7726-142">Requirements</span></span>



| <span data-ttu-id="b7726-143">需求</span><span class="sxs-lookup"><span data-stu-id="b7726-143">Requirement</span></span> | <span data-ttu-id="b7726-144">值</span><span class="sxs-lookup"><span data-stu-id="b7726-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7726-145">標頭</span><span class="sxs-lookup"><span data-stu-id="b7726-145">Header</span></span><br/>  | <dl> <span data-ttu-id="b7726-146"><dt>D3DX11。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7726-146"><dt>D3DX11.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7726-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="b7726-147">Library</span></span><br/> | <dl> <span data-ttu-id="b7726-148"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7726-148"><dt>D3DX11.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7726-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7726-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7726-150">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="b7726-150">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

