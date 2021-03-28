---
title: 'D3DX11GetImageInfoFromResource 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用此函式，而是使用資源函式，然後使用 DirectXTex 程式庫 (工具) 、LoadFromXXXMemory (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。 抓取資源中指定影像的相關資訊。
ms.assetid: e4752eb3-38d5-4922-b3c8-5fdcd0cc0610
keywords:
- D3DX11GetImageInfoFromResource 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967a7b2c2ff03faefc12a48be18a4756e4ed3962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974596"
---
# <a name="d3dx11getimageinfofromresource-function"></a><span data-ttu-id="4686c-106">D3DX11GetImageInfoFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="4686c-106">D3DX11GetImageInfoFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="4686c-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="4686c-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="4686c-108">我們建議您不要使用此函式，而是使用 [資源](/windows/desktop/menurc/resources-functions)函式，然後使用 [DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫 (工具) 、 **LOADFROMXXXMEMORY** (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。</span><span class="sxs-lookup"><span data-stu-id="4686c-108">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then use [DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="4686c-109">抓取資源中指定影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4686c-109">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="4686c-110">語法</span><span class="sxs-lookup"><span data-stu-id="4686c-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="4686c-111">參數</span><span class="sxs-lookup"><span data-stu-id="4686c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4686c-112">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4686c-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4686c-113">類型： **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4686c-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4686c-114">載入資源的模組。</span><span class="sxs-lookup"><span data-stu-id="4686c-114">Module where the resource is loaded.</span></span> <span data-ttu-id="4686c-115">將此參數設定為 **Null** ，以指定與作業系統用來建立目前進程的映射相關聯的模組。</span><span class="sxs-lookup"><span data-stu-id="4686c-115">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="4686c-116">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4686c-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4686c-117">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4686c-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4686c-118">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="4686c-118">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="4686c-119">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="4686c-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="4686c-120">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="4686c-120">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="4686c-121">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="4686c-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4686c-122">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4686c-122">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4686c-123">類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="4686c-123">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="4686c-124">選擇性的執行緒抽取，可用來以非同步方式載入資訊。</span><span class="sxs-lookup"><span data-stu-id="4686c-124">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="4686c-125">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4686c-125">Can be **NULL**.</span></span> <span data-ttu-id="4686c-126">請參閱 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)。</span><span class="sxs-lookup"><span data-stu-id="4686c-126">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="4686c-127">*pSrcInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4686c-127">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4686c-128">類型： **[ **D3DX11 \_ 影像 \_ 資訊**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="4686c-128">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="4686c-129">D3DX11 影像資訊結構的指標，此 \_ \_ 結構會填入原始程式檔中的資料描述。</span><span class="sxs-lookup"><span data-stu-id="4686c-129">Pointer to a D3DX11\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="4686c-130">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4686c-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4686c-131">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="4686c-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="4686c-132">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="4686c-132">A pointer to the return value.</span></span> <span data-ttu-id="4686c-133">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4686c-133">May be **NULL**.</span></span> <span data-ttu-id="4686c-134">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="4686c-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4686c-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="4686c-135">Return value</span></span>

<span data-ttu-id="4686c-136">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4686c-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4686c-137">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="4686c-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4686c-138">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="4686c-138">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="4686c-139">備註</span><span class="sxs-lookup"><span data-stu-id="4686c-139">Remarks</span></span>

<span data-ttu-id="4686c-140">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="4686c-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="4686c-141">如果已定義 Unicode，函式呼叫會解析為 **D3DX11GetImageInfoFromResourceW**。</span><span class="sxs-lookup"><span data-stu-id="4686c-141">If Unicode is defined, the function call resolves to **D3DX11GetImageInfoFromResourceW**.</span></span> <span data-ttu-id="4686c-142">否則，函式呼叫會解析為 **D3DX11GetImageInfoFromResourceA** ，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="4686c-142">Otherwise, the function call resolves to **D3DX11GetImageInfoFromResourceA** because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4686c-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="4686c-143">Requirements</span></span>



| <span data-ttu-id="4686c-144">需求</span><span class="sxs-lookup"><span data-stu-id="4686c-144">Requirement</span></span> | <span data-ttu-id="4686c-145">值</span><span class="sxs-lookup"><span data-stu-id="4686c-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4686c-146">標頭</span><span class="sxs-lookup"><span data-stu-id="4686c-146">Header</span></span><br/>  | <dl> <span data-ttu-id="4686c-147"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="4686c-147"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="4686c-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="4686c-148">Library</span></span><br/> | <dl> <span data-ttu-id="4686c-149"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4686c-149"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4686c-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4686c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4686c-151">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="4686c-151">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

