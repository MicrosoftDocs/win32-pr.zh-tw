---
title: 'D3DX11CreateAsyncTextureProcessor 函式 (D3DX11tex) '
description: '請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。 建立要搭配執行緒抽取使用的資料處理器。 |D3DX11CreateAsyncTextureProcessor 函式 (D3DX11tex) '
ms.assetid: 4f23d265-b326-4449-b7ca-dd0596511b35
keywords:
- D3DX11CreateAsyncTextureProcessor 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncTextureProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612be6da4dce05ccae368edc4effea83a823dcff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992283"
---
# <a name="d3dx11createasynctextureprocessor-function"></a><span data-ttu-id="f958e-107">D3DX11CreateAsyncTextureProcessor 函式</span><span class="sxs-lookup"><span data-stu-id="f958e-107">D3DX11CreateAsyncTextureProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="f958e-108">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="f958e-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="f958e-109">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="f958e-109">See Remarks.</span></span>

 

<span data-ttu-id="f958e-110">建立要搭配 [**執行緒抽取**](id3dx11threadpump.md)使用的資料處理器。</span><span class="sxs-lookup"><span data-stu-id="f958e-110">Create a data processor to be used with a [**thread pump**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f958e-111">語法</span><span class="sxs-lookup"><span data-stu-id="f958e-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncTextureProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="f958e-112">參數</span><span class="sxs-lookup"><span data-stu-id="f958e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f958e-113">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f958e-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f958e-114">類型： **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="f958e-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="f958e-115">Devive 的指標 (請參閱 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) 。</span><span class="sxs-lookup"><span data-stu-id="f958e-115">A pointer to the devive (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)).</span></span>

</dd> <dt>

<span data-ttu-id="f958e-116">*pLoadInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f958e-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f958e-117">類型： **[ **D3DX11 \_ 映射 \_ 載入 \_ 資訊**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="f958e-117">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="f958e-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="f958e-118">Optional.</span></span> <span data-ttu-id="f958e-119">識別材質的特性 (請參閱資料處理器建立時) [**D3DX11 \_ 影像 \_ 載入 \_ 資訊**](d3dx11-image-load-info.md) ; 將此值設定為 **Null** ，以在載入紋理時讀取紋理的特性。</span><span class="sxs-lookup"><span data-stu-id="f958e-119">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="f958e-120">*ppDataProcessor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f958e-120">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f958e-121">類型： **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f958e-121">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="f958e-122">緩衝區指標的位址，其中包含建立的資料處理器 (請參閱 [**ID3DX11DataProcessor 介面**](id3dx11dataprocessor.md)) 。</span><span class="sxs-lookup"><span data-stu-id="f958e-122">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f958e-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="f958e-123">Return value</span></span>

<span data-ttu-id="f958e-124">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f958e-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f958e-125">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f958e-125">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f958e-126">備註</span><span class="sxs-lookup"><span data-stu-id="f958e-126">Remarks</span></span>

<span data-ttu-id="f958e-127">此 API 會建立資料處理器介面並載入紋理; [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) 會建立資料處理器介面。</span><span class="sxs-lookup"><span data-stu-id="f958e-127">This API does creates a data-processor interface and loads the texture; [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) creates the data-processor interface.</span></span>

<span data-ttu-id="f958e-128">D3DX 10 和 D3DX 11 以外的非同步載入器不會執行。</span><span class="sxs-lookup"><span data-stu-id="f958e-128">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="f958e-129">針對 Windows Store 應用程式， (的 DirectX 範例，例如 [Direct3D 教學課程範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) 包含使用 Windows 執行階段非同步程式設計模型 ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) 的 **BasicLoader** 模組。</span><span class="sxs-lookup"><span data-stu-id="f958e-129">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="f958e-130">針對 Win32 傳統型應用程式，您可以使用 [並行執行階段](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) 來執行類似于 Windows 執行階段非同步程式設計模型的內容。</span><span class="sxs-lookup"><span data-stu-id="f958e-130">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="f958e-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="f958e-131">Requirements</span></span>



| <span data-ttu-id="f958e-132">需求</span><span class="sxs-lookup"><span data-stu-id="f958e-132">Requirement</span></span> | <span data-ttu-id="f958e-133">值</span><span class="sxs-lookup"><span data-stu-id="f958e-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f958e-134">標頭</span><span class="sxs-lookup"><span data-stu-id="f958e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="f958e-135"><dt>D3DX11tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="f958e-135"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f958e-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="f958e-136">Library</span></span><br/> | <dl> <span data-ttu-id="f958e-137"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f958e-137"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f958e-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f958e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f958e-139">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="f958e-139">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

