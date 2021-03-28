---
title: 'D3DX11GetImageInfoFromFile 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用 DirectXTex 程式庫 GetMetadataFromXXXFile (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。 抓取指定影像檔案的相關資訊。
ms.assetid: 57768604-3672-49a0-8120-f09240b8fc98
keywords:
- D3DX11GetImageInfoFromFile 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8448d31a3f4fdb14855ea2c9456da87f9df1de4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035394"
---
# <a name="d3dx11getimageinfofromfile-function"></a><span data-ttu-id="97d19-106">D3DX11GetImageInfoFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="97d19-106">D3DX11GetImageInfoFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="97d19-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="97d19-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="97d19-108">我們建議您不要使用這個函式，而是使用 [DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫 **GETMETADATAFROMXXXFILE** (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。</span><span class="sxs-lookup"><span data-stu-id="97d19-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GetMetadataFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="97d19-109">抓取指定影像檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="97d19-109">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="97d19-110">語法</span><span class="sxs-lookup"><span data-stu-id="97d19-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="97d19-111">參數</span><span class="sxs-lookup"><span data-stu-id="97d19-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97d19-112">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97d19-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97d19-113">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="97d19-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="97d19-114">要取得相關資訊之影像的檔案名。</span><span class="sxs-lookup"><span data-stu-id="97d19-114">File name of image to retrieve information about.</span></span> <span data-ttu-id="97d19-115">如果 \_ 已定義 unicode 或 unicode，則此參數類型為 LPCWSTR，否則為 LPCSTR 類型。</span><span class="sxs-lookup"><span data-stu-id="97d19-115">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="97d19-116">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97d19-116">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97d19-117">類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="97d19-117">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="97d19-118">選擇性的執行緒抽取，可用來以非同步方式載入資訊。</span><span class="sxs-lookup"><span data-stu-id="97d19-118">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="97d19-119">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="97d19-119">Can be **NULL**.</span></span> <span data-ttu-id="97d19-120">請參閱 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)。</span><span class="sxs-lookup"><span data-stu-id="97d19-120">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="97d19-121">*pSrcInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97d19-121">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97d19-122">類型： **[ **D3DX11 \_ 影像 \_ 資訊**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="97d19-122">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="97d19-123">要填入原始程式檔中資料描述的 [**D3DX11 \_ 影像 \_ 資訊**](d3dx11-image-info.md) 指標。</span><span class="sxs-lookup"><span data-stu-id="97d19-123">Pointer to a [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md) to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="97d19-124">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="97d19-124">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97d19-125">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="97d19-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="97d19-126">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="97d19-126">A pointer to the return value.</span></span> <span data-ttu-id="97d19-127">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="97d19-127">May be **NULL**.</span></span> <span data-ttu-id="97d19-128">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="97d19-128">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97d19-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="97d19-129">Return value</span></span>

<span data-ttu-id="97d19-130">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="97d19-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="97d19-131">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="97d19-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="97d19-132">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="97d19-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="97d19-133">備註</span><span class="sxs-lookup"><span data-stu-id="97d19-133">Remarks</span></span>

<span data-ttu-id="97d19-134">此函數支援 Unicode 和 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="97d19-134">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="97d19-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="97d19-135">Requirements</span></span>



| <span data-ttu-id="97d19-136">需求</span><span class="sxs-lookup"><span data-stu-id="97d19-136">Requirement</span></span> | <span data-ttu-id="97d19-137">值</span><span class="sxs-lookup"><span data-stu-id="97d19-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97d19-138">標頭</span><span class="sxs-lookup"><span data-stu-id="97d19-138">Header</span></span><br/>  | <dl> <span data-ttu-id="97d19-139"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="97d19-139"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="97d19-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="97d19-140">Library</span></span><br/> | <dl> <span data-ttu-id="97d19-141"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="97d19-141"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="97d19-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97d19-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97d19-143">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="97d19-143">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

