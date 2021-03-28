---
title: 'D3DX11CreateAsyncCompilerProcessor 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請參閱＜備註＞。 建立著色器的非同步資料處理器。
ms.assetid: 90756ac3-946d-49fa-9f97-70dc5da812c6
keywords:
- D3DX11CreateAsyncCompilerProcessor 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncCompilerProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533e487e65640b8c17a0ff8d061388e8b5a6c0f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992306"
---
# <a name="d3dx11createasynccompilerprocessor-function"></a><span data-ttu-id="c6fee-106">D3DX11CreateAsyncCompilerProcessor 函式</span><span class="sxs-lookup"><span data-stu-id="c6fee-106">D3DX11CreateAsyncCompilerProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="c6fee-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="c6fee-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="c6fee-108">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="c6fee-108">See Remarks.</span></span>

 

<span data-ttu-id="c6fee-109">建立著色器的非同步資料處理器。</span><span class="sxs-lookup"><span data-stu-id="c6fee-109">Create an asynchronous-data processor for a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6fee-110">語法</span><span class="sxs-lookup"><span data-stu-id="c6fee-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="c6fee-111">參數</span><span class="sxs-lookup"><span data-stu-id="c6fee-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6fee-112">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6fee-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fee-113">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c6fee-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c6fee-114">包含著色器檔案名的字串。</span><span class="sxs-lookup"><span data-stu-id="c6fee-114">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="c6fee-115">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6fee-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fee-116">Type： **CONST D3D11 \_ 著色 \_ 器 \* 宏**</span><span class="sxs-lookup"><span data-stu-id="c6fee-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="c6fee-117">以 Null 結束的著色器宏陣列;將此設為 **Null** ，以指定無宏。</span><span class="sxs-lookup"><span data-stu-id="c6fee-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="c6fee-118">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6fee-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fee-119">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="c6fee-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="c6fee-120">包含介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c6fee-120">A pointer to an include interface.</span></span> <span data-ttu-id="c6fee-121">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c6fee-121">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c6fee-122">*pFunctionName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6fee-122">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fee-123">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c6fee-123">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c6fee-124">著色器開始執行的著色器輸入點函式名稱。</span><span class="sxs-lookup"><span data-stu-id="c6fee-124">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="c6fee-125">當您編譯效果時， **D3DX11CreateAsyncCompilerProcessor** 會忽略 *pFunctionName*;建議您將 *pFunctionName* 設定為 **null** ，因為如果所呼叫的函式不會使用它，則將指標參數設定為 **null** ，是很好的程式設計作法。</span><span class="sxs-lookup"><span data-stu-id="c6fee-125">When you compile an effect, **D3DX11CreateAsyncCompilerProcessor** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it..</span></span>

</dd> <dt>

<span data-ttu-id="c6fee-126">*pProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6fee-126">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fee-127">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c6fee-127">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c6fee-128">指定著色器設定檔或著色器模型的字串;可以是著色器模型2、著色器模型3、著色器模型4或著色器模型5中的任何設定檔。</span><span class="sxs-lookup"><span data-stu-id="c6fee-128">A string that specifies the shader profile or shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="c6fee-129">設定檔也可以是適用于效果類型 (例如 fx \_ 4 \_ 1) 。</span><span class="sxs-lookup"><span data-stu-id="c6fee-129">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="c6fee-130">*Flags1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6fee-130">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fee-131">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c6fee-131">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c6fee-132">著色器編譯旗標。</span><span class="sxs-lookup"><span data-stu-id="c6fee-132">Shader compile flags.</span></span>

</dd> <dt>

<span data-ttu-id="c6fee-133">*Flags2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c6fee-133">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fee-134">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c6fee-134">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c6fee-135">效果編譯旗標。</span><span class="sxs-lookup"><span data-stu-id="c6fee-135">Effect compile flags.</span></span> <span data-ttu-id="c6fee-136">當您編譯著色器而非效果檔案時， **D3DX11CreateAsyncCompilerProcessor** 會忽略 *Flags2*;我們建議您將 *Flags2* 設定為零，因為如果所呼叫的函式不會使用它，則將指標參數設定為零是很好的程式設計作法。</span><span class="sxs-lookup"><span data-stu-id="c6fee-136">When you compile a shader and not an effect file, **D3DX11CreateAsyncCompilerProcessor** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="c6fee-137">*ppCompiledShader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c6fee-137">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fee-138">類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c6fee-138">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c6fee-139">已編譯效果之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="c6fee-139">Address of a pointer to the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="c6fee-140">*ppErrorBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c6fee-140">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fee-141">類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c6fee-141">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c6fee-142">編譯錯誤之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="c6fee-142">Address of a pointer to compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="c6fee-143">*ppDataProcessor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c6fee-143">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6fee-144">類型： **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c6fee-144">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="c6fee-145">緩衝區指標的位址，其中包含建立的資料處理器 (請參閱 [**ID3DX11DataProcessor 介面**](id3dx11dataprocessor.md)) 。</span><span class="sxs-lookup"><span data-stu-id="c6fee-145">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6fee-146">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6fee-146">Return value</span></span>

<span data-ttu-id="c6fee-147">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c6fee-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c6fee-148">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c6fee-148">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c6fee-149">備註</span><span class="sxs-lookup"><span data-stu-id="c6fee-149">Remarks</span></span>

<span data-ttu-id="c6fee-150">D3DX 10 和 D3DX 11 以外的非同步載入器不會執行。</span><span class="sxs-lookup"><span data-stu-id="c6fee-150">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="c6fee-151">針對 Windows Store 應用程式， (的 DirectX 範例，例如 [Direct3D 教學課程範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) 包含使用 Windows 執行階段非同步程式設計模型 ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) 的 **BasicLoader** 模組。</span><span class="sxs-lookup"><span data-stu-id="c6fee-151">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="c6fee-152">針對 Win32 傳統型應用程式，您可以使用 [並行執行階段](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) 來執行類似于 Windows 執行階段非同步程式設計模型的內容。</span><span class="sxs-lookup"><span data-stu-id="c6fee-152">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6fee-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6fee-153">Requirements</span></span>



| <span data-ttu-id="c6fee-154">需求</span><span class="sxs-lookup"><span data-stu-id="c6fee-154">Requirement</span></span> | <span data-ttu-id="c6fee-155">值</span><span class="sxs-lookup"><span data-stu-id="c6fee-155">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6fee-156">標頭</span><span class="sxs-lookup"><span data-stu-id="c6fee-156">Header</span></span><br/>  | <dl> <span data-ttu-id="c6fee-157"><dt>D3DX11async。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6fee-157"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="c6fee-158">程式庫</span><span class="sxs-lookup"><span data-stu-id="c6fee-158">Library</span></span><br/> | <dl> <span data-ttu-id="c6fee-159"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6fee-159"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c6fee-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6fee-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6fee-161">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="c6fee-161">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

