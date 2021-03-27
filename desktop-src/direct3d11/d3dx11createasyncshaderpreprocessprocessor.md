---
title: 'D3DX11CreateAsyncShaderPreprocessProcessor 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。 以非同步方式建立著色器的資料處理器。
ms.assetid: a7e9754b-acc1-49d0-bd8e-b116bc3c7e3a
keywords:
- D3DX11CreateAsyncShaderPreprocessProcessor 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderPreprocessProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e58b267f186e5fd0104b10e9f9423f407aaf13
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946180"
---
# <a name="d3dx11createasyncshaderpreprocessprocessor-function"></a><span data-ttu-id="af184-106">D3DX11CreateAsyncShaderPreprocessProcessor 函式</span><span class="sxs-lookup"><span data-stu-id="af184-106">D3DX11CreateAsyncShaderPreprocessProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="af184-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="af184-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="af184-108">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="af184-108">See Remarks.</span></span>

 

<span data-ttu-id="af184-109">以非同步方式建立著色器的資料處理器。</span><span class="sxs-lookup"><span data-stu-id="af184-109">Create a data processor for a shader asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="af184-110">語法</span><span class="sxs-lookup"><span data-stu-id="af184-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncShaderPreprocessProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _Out_       ID3D10Blob           **ppShaderText,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="af184-111">參數</span><span class="sxs-lookup"><span data-stu-id="af184-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af184-112">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af184-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af184-113">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="af184-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="af184-114">包含著色器檔案名的字串。</span><span class="sxs-lookup"><span data-stu-id="af184-114">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="af184-115">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af184-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af184-116">Type： **CONST D3D11 \_ 著色 \_ 器 \* 宏**</span><span class="sxs-lookup"><span data-stu-id="af184-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="af184-117">以 Null 結束的著色器宏陣列;將此設為 **Null** ，以指定無宏。</span><span class="sxs-lookup"><span data-stu-id="af184-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="af184-118">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af184-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af184-119">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="af184-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="af184-120">包含介面的指標;將此設為 **Null** ，以指定沒有包含檔。</span><span class="sxs-lookup"><span data-stu-id="af184-120">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="af184-121">*ppShaderText* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="af184-121">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af184-122">類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="af184-122">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="af184-123">緩衝區指標的位址，其中包含著色器的 ASCII 文字。</span><span class="sxs-lookup"><span data-stu-id="af184-123">Address of a pointer to a buffer that contains the ASCII text of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="af184-124">*ppErrorBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="af184-124">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af184-125">類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="af184-125">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="af184-126">包含編譯錯誤之緩衝區的指標位址。</span><span class="sxs-lookup"><span data-stu-id="af184-126">Address of a pointer to a buffer that contains compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="af184-127">*ppDataProcessor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="af184-127">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af184-128">類型： **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="af184-128">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="af184-129">緩衝區指標的位址，其中包含建立的資料處理器 (請參閱 [**ID3DX11DataProcessor 介面**](id3dx11dataprocessor.md)) 。</span><span class="sxs-lookup"><span data-stu-id="af184-129">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af184-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="af184-130">Return value</span></span>

<span data-ttu-id="af184-131">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af184-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af184-132">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="af184-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="af184-133">備註</span><span class="sxs-lookup"><span data-stu-id="af184-133">Remarks</span></span>

<span data-ttu-id="af184-134">D3DX 10 和 D3DX 11 以外的非同步載入器不會執行。</span><span class="sxs-lookup"><span data-stu-id="af184-134">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="af184-135">針對 Windows Store 應用程式， (的 DirectX 範例，例如 [Direct3D 教學課程範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) 包含使用 Windows 執行階段非同步程式設計模型 ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) 的 **BasicLoader** 模組。</span><span class="sxs-lookup"><span data-stu-id="af184-135">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="af184-136">針對 Win32 傳統型應用程式，您可以使用 [並行執行階段](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) 來執行類似于 Windows 執行階段非同步程式設計模型的內容。</span><span class="sxs-lookup"><span data-stu-id="af184-136">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="af184-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="af184-137">Requirements</span></span>



| <span data-ttu-id="af184-138">需求</span><span class="sxs-lookup"><span data-stu-id="af184-138">Requirement</span></span> | <span data-ttu-id="af184-139">值</span><span class="sxs-lookup"><span data-stu-id="af184-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="af184-140">標頭</span><span class="sxs-lookup"><span data-stu-id="af184-140">Header</span></span><br/>  | <dl> <span data-ttu-id="af184-141"><dt>D3DX11async。h</dt></span><span class="sxs-lookup"><span data-stu-id="af184-141"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="af184-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="af184-142">Library</span></span><br/> | <dl> <span data-ttu-id="af184-143"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="af184-143"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="af184-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af184-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af184-145">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="af184-145">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

