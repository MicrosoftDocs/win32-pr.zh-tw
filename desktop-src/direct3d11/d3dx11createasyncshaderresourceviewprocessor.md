---
title: 'D3DX11CreateAsyncShaderResourceViewProcessor 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。
ms.assetid: bd9349af-f433-47f9-b443-3049c32fc286
keywords:
- D3DX11CreateAsyncShaderResourceViewProcessor 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderResourceViewProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3164aac5ddaec3d61108a2cf129b76991b8f76a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992287"
---
# <a name="d3dx11createasyncshaderresourceviewprocessor-function"></a><span data-ttu-id="c7b7b-104">D3DX11CreateAsyncShaderResourceViewProcessor 函式</span><span class="sxs-lookup"><span data-stu-id="c7b7b-104">D3DX11CreateAsyncShaderResourceViewProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="c7b7b-105">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="c7b7b-105">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="c7b7b-106">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="c7b7b-106">See Remarks.</span></span>

 

<span data-ttu-id="c7b7b-107">建立會載入資源的資料處理器，然後為其建立著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="c7b7b-107">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="c7b7b-108">資料處理器是 D3DX11 中使用 [**執行緒抽取**](id3dx11threadpump.md)的非同步資料載入功能的元件。</span><span class="sxs-lookup"><span data-stu-id="c7b7b-108">Data processors are a component of the asynchronous data loading feature in D3DX11 that uses [**thread pumps**](id3dx11threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7b7b-109">語法</span><span class="sxs-lookup"><span data-stu-id="c7b7b-109">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="c7b7b-110">參數</span><span class="sxs-lookup"><span data-stu-id="c7b7b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7b7b-111">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7b7b-111">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7b7b-112">類型： **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="c7b7b-112">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="c7b7b-113">Direct3D 裝置的指標 (請參閱將用來建立資源的 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) ，以及該資源的著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="c7b7b-113">Pointer to the Direct3D device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will be used to create a resource and a shader-resource view for that resource.</span></span>

</dd> <dt>

<span data-ttu-id="c7b7b-114">*pLoadInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c7b7b-114">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7b7b-115">類型： **[ **D3DX11 \_ 映射 \_ 載入 \_ 資訊**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="c7b7b-115">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="c7b7b-116">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c7b7b-116">Optional.</span></span> <span data-ttu-id="c7b7b-117">識別材質的特性 (請參閱資料處理器建立時) [**D3DX11 \_ 影像 \_ 載入 \_ 資訊**](d3dx11-image-load-info.md) ; 將此值設定為 **Null** ，以在載入紋理時讀取紋理的特性。</span><span class="sxs-lookup"><span data-stu-id="c7b7b-117">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="c7b7b-118">*ppDataProcessor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c7b7b-118">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7b7b-119">類型： **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c7b7b-119">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="c7b7b-120">緩衝區指標的位址，其中包含建立的資料處理器 (請參閱 [**ID3DX11DataProcessor 介面**](id3dx11dataprocessor.md)) 。</span><span class="sxs-lookup"><span data-stu-id="c7b7b-120">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7b7b-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7b7b-121">Return value</span></span>

<span data-ttu-id="c7b7b-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c7b7b-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c7b7b-123">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c7b7b-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c7b7b-124">備註</span><span class="sxs-lookup"><span data-stu-id="c7b7b-124">Remarks</span></span>

<span data-ttu-id="c7b7b-125">D3DX 10 和 D3DX 11 以外的非同步載入器不會執行。</span><span class="sxs-lookup"><span data-stu-id="c7b7b-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="c7b7b-126">針對 Windows Store 應用程式， (的 DirectX 範例，例如 [Direct3D 教學課程範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) 包含使用 Windows 執行階段非同步程式設計模型 ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) 的 **BasicLoader** 模組。</span><span class="sxs-lookup"><span data-stu-id="c7b7b-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="c7b7b-127">針對 Win32 傳統型應用程式，您可以使用 [並行執行階段](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) 來執行類似于 Windows 執行階段非同步程式設計模型的內容。</span><span class="sxs-lookup"><span data-stu-id="c7b7b-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7b7b-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7b7b-128">Requirements</span></span>



| <span data-ttu-id="c7b7b-129">需求</span><span class="sxs-lookup"><span data-stu-id="c7b7b-129">Requirement</span></span> | <span data-ttu-id="c7b7b-130">值</span><span class="sxs-lookup"><span data-stu-id="c7b7b-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7b7b-131">標頭</span><span class="sxs-lookup"><span data-stu-id="c7b7b-131">Header</span></span><br/>  | <dl> <span data-ttu-id="c7b7b-132"><dt>D3DX11async。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7b7b-132"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="c7b7b-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="c7b7b-133">Library</span></span><br/> | <dl> <span data-ttu-id="c7b7b-134"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7b7b-134"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c7b7b-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7b7b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7b7b-136">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="c7b7b-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

