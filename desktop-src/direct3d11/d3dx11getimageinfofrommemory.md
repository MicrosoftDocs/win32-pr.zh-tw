---
title: 'D3DX11GetImageInfoFromMemory 函式 (D3DX11tex) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用 DirectXTex 程式庫 GetMetadataFromXXXMemory (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。 取得已載入記憶體之映射的相關資訊。
ms.assetid: b13192fa-4235-4c38-ba46-e14ffab2f653
keywords:
- D3DX11GetImageInfoFromMemory 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11GetImageInfoFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c5f1f04c9540614541b9f63b7833967d6ce959
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974593"
---
# <a name="d3dx11getimageinfofrommemory-function"></a><span data-ttu-id="a6720-106">D3DX11GetImageInfoFromMemory 函式</span><span class="sxs-lookup"><span data-stu-id="a6720-106">D3DX11GetImageInfoFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="a6720-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a6720-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="a6720-108">我們建議您不要使用這個函式，而是使用 [DirectXTex](https://github.com/Microsoft/DirectXTex) 程式庫 **GETMETADATAFROMXXXMEMORY** (其中 XXX 是 WIC、DDS 或 TGA;WIC 不支援 DDS 和 TGA;D3DX 9 支援 TGA 作為遊戲) 的常用藝術來源格式。</span><span class="sxs-lookup"><span data-stu-id="a6720-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **GetMetadataFromXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="a6720-109">取得已載入記憶體之映射的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a6720-109">Get information about an image already loaded into memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6720-110">語法</span><span class="sxs-lookup"><span data-stu-id="a6720-110">Syntax</span></span>


```C++
HRESULT D3DX11GetImageInfoFromMemory(
  _In_  LPCVOID           pSrcData,
  _In_  SIZE_T            SrcDataSize,
  _In_  ID3DX11ThreadPump *pPump,
  _In_  D3DX11_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="a6720-111">參數</span><span class="sxs-lookup"><span data-stu-id="a6720-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6720-112">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6720-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6720-113">類型： **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a6720-113">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a6720-114">記憶體中影像的指標。</span><span class="sxs-lookup"><span data-stu-id="a6720-114">Pointer to the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="a6720-115">*SrcDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6720-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6720-116">類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a6720-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a6720-117">記憶體中影像的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a6720-117">Size of the image in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a6720-118">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6720-118">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6720-119">類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="a6720-119">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="a6720-120">選擇性的執行緒抽取，可用來以非同步方式載入資訊。</span><span class="sxs-lookup"><span data-stu-id="a6720-120">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="a6720-121">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a6720-121">Can be **NULL**.</span></span> <span data-ttu-id="a6720-122">請參閱 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)。</span><span class="sxs-lookup"><span data-stu-id="a6720-122">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6720-123">*pSrcInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6720-123">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6720-124">類型： **[ **D3DX11 \_ 影像 \_ 資訊**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a6720-124">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="a6720-125">記憶體中影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a6720-125">Information about the image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="a6720-126">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a6720-126">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6720-127">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="a6720-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="a6720-128">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="a6720-128">A pointer to the return value.</span></span> <span data-ttu-id="a6720-129">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a6720-129">May be **NULL**.</span></span> <span data-ttu-id="a6720-130">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="a6720-130">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6720-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="a6720-131">Return value</span></span>

<span data-ttu-id="a6720-132">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a6720-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a6720-133">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a6720-133">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6720-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6720-134">Requirements</span></span>



| <span data-ttu-id="a6720-135">需求</span><span class="sxs-lookup"><span data-stu-id="a6720-135">Requirement</span></span> | <span data-ttu-id="a6720-136">值</span><span class="sxs-lookup"><span data-stu-id="a6720-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6720-137">標頭</span><span class="sxs-lookup"><span data-stu-id="a6720-137">Header</span></span><br/>  | <dl> <span data-ttu-id="a6720-138"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="a6720-138"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a6720-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="a6720-139">Library</span></span><br/> | <dl> <span data-ttu-id="a6720-140"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6720-140"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a6720-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6720-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6720-142">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="a6720-142">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

