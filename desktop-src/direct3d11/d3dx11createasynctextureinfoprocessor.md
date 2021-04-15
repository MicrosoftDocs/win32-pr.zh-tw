---
title: 'D3DX11CreateAsyncTextureInfoProcessor 函式 (D3DX11tex) '
description: '請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。 建立要搭配執行緒抽取使用的資料處理器。 |D3DX11CreateAsyncTextureInfoProcessor 函式 (D3DX11tex) '
ms.assetid: 87de73a5-21f7-4abd-b83a-65c6761681c3
keywords:
- D3DX11CreateAsyncTextureInfoProcessor 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureInfoProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aac60b1d496e0f1d4ecb604b18a8ef71cac8b5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992291"
---
# <a name="d3dx11createasynctextureinfoprocessor-function"></a><span data-ttu-id="abe0b-107">D3DX11CreateAsyncTextureInfoProcessor 函式</span><span class="sxs-lookup"><span data-stu-id="abe0b-107">D3DX11CreateAsyncTextureInfoProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="abe0b-108">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="abe0b-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="abe0b-109">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="abe0b-109">See Remarks.</span></span>

 

<span data-ttu-id="abe0b-110">建立要搭配 [**執行緒抽取**](id3dx11threadpump.md)使用的資料處理器。</span><span class="sxs-lookup"><span data-stu-id="abe0b-110">Create a data processor to be used with a [**thread pump**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="abe0b-111">語法</span><span class="sxs-lookup"><span data-stu-id="abe0b-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncTextureInfoProcessor(
  _In_  D3DX11_IMAGE_INFO    *pImageInfo,
  _Out_ ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="abe0b-112">參數</span><span class="sxs-lookup"><span data-stu-id="abe0b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abe0b-113">*pImageInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="abe0b-113">*pImageInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abe0b-114">類型： **[ **D3DX11 \_ 影像 \_ 資訊**](d3dx11-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="abe0b-114">Type: **[**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)\***</span></span>

<span data-ttu-id="abe0b-115">選擇性。</span><span class="sxs-lookup"><span data-stu-id="abe0b-115">Optional.</span></span> <span data-ttu-id="abe0b-116">識別材質的特性 (請參閱資料處理器建立時) 的 [**D3DX11 \_ 影像 \_ 資訊**](d3dx11-image-info.md) ; 將此值設定為 **Null** ，以在載入紋理時讀取材質的特性。</span><span class="sxs-lookup"><span data-stu-id="abe0b-116">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_INFO**](d3dx11-image-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="abe0b-117">*ppDataProcessor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="abe0b-117">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abe0b-118">類型： **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="abe0b-118">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="abe0b-119">緩衝區指標的位址，其中包含建立的資料處理器 (請參閱 [**ID3DX11DataProcessor 介面**](id3dx11dataprocessor.md)) 。</span><span class="sxs-lookup"><span data-stu-id="abe0b-119">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abe0b-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="abe0b-120">Return value</span></span>

<span data-ttu-id="abe0b-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="abe0b-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="abe0b-122">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="abe0b-122">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="abe0b-123">備註</span><span class="sxs-lookup"><span data-stu-id="abe0b-123">Remarks</span></span>

<span data-ttu-id="abe0b-124">此 API 會建立資料處理器介面; [**D3DX11CreateAsyncTextureProcessor**](d3dx11createasynctextureprocessor.md) 會建立資料處理器介面並載入紋理。</span><span class="sxs-lookup"><span data-stu-id="abe0b-124">This API does creates a data-processor interface; [**D3DX11CreateAsyncTextureProcessor**](d3dx11createasynctextureprocessor.md) creates the data-processor interface and loads the texture.</span></span>

<span data-ttu-id="abe0b-125">D3DX 10 和 D3DX 11 以外的非同步載入器不會執行。</span><span class="sxs-lookup"><span data-stu-id="abe0b-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="abe0b-126">針對 Windows Store 應用程式， (的 DirectX 範例，例如 [Direct3D 教學課程範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) 包含使用 Windows 執行階段非同步程式設計模型 ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) 的 **BasicLoader** 模組。</span><span class="sxs-lookup"><span data-stu-id="abe0b-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="abe0b-127">針對 Win32 傳統型應用程式，您可以使用 [並行執行階段](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) 來執行類似于 Windows 執行階段非同步程式設計模型的內容。</span><span class="sxs-lookup"><span data-stu-id="abe0b-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="abe0b-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="abe0b-128">Requirements</span></span>



| <span data-ttu-id="abe0b-129">需求</span><span class="sxs-lookup"><span data-stu-id="abe0b-129">Requirement</span></span> | <span data-ttu-id="abe0b-130">值</span><span class="sxs-lookup"><span data-stu-id="abe0b-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abe0b-131">標頭</span><span class="sxs-lookup"><span data-stu-id="abe0b-131">Header</span></span><br/>  | <dl> <span data-ttu-id="abe0b-132"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="abe0b-132"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="abe0b-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="abe0b-133">Library</span></span><br/> | <dl> <span data-ttu-id="abe0b-134"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="abe0b-134"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="abe0b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abe0b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe0b-136">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="abe0b-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

