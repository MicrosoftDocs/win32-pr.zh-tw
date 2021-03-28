---
title: 'D3DX11CompileFromMemory 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用 Fxc.exe 命令列編譯器，或使用其中一個 HLSL 編譯 Api （例如 D3DCompile API），以離線方式編譯。 編譯已載入記憶體中的著色器或效果。
ms.assetid: 3396560f-f411-4c66-9f22-03c0050c74b0
keywords:
- D3DX11CompileFromMemory 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e10590c3db458a23bf4d52b6507146884630087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974616"
---
# <a name="d3dx11compilefrommemory-function"></a><span data-ttu-id="d381c-106">D3DX11CompileFromMemory 函式</span><span class="sxs-lookup"><span data-stu-id="d381c-106">D3DX11CompileFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="d381c-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d381c-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="d381c-108">我們建議您不要使用這個函式，而是使用 Fxc.exe 命令列編譯器，或使用其中一個 HLSL 編譯 Api （例如 [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API），以離線方式編譯。</span><span class="sxs-lookup"><span data-stu-id="d381c-108">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API.</span></span>

 

<span data-ttu-id="d381c-109">編譯已載入記憶體中的著色器或效果。</span><span class="sxs-lookup"><span data-stu-id="d381c-109">Compile a shader or an effect that is loaded in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="d381c-110">語法</span><span class="sxs-lookup"><span data-stu-id="d381c-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="d381c-111">參數</span><span class="sxs-lookup"><span data-stu-id="d381c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d381c-112">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d381c-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d381c-113">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d381c-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d381c-114">記憶體中著色器的指標。</span><span class="sxs-lookup"><span data-stu-id="d381c-114">Pointer to the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="d381c-115">*SrcDataLen* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d381c-115">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d381c-116">類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d381c-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d381c-117">記憶體中的著色器大小。</span><span class="sxs-lookup"><span data-stu-id="d381c-117">Size of the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="d381c-118">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d381c-118">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d381c-119">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d381c-119">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d381c-120">包含著色器程式碼的檔案名。</span><span class="sxs-lookup"><span data-stu-id="d381c-120">The name of the file that contains the shader code.</span></span>

</dd> <dt>

<span data-ttu-id="d381c-121">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d381c-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d381c-122">Type： **Const [**D3D10 \_ 著色器 \_ 宏**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="d381c-122">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="d381c-123">選擇性。</span><span class="sxs-lookup"><span data-stu-id="d381c-123">Optional.</span></span> <span data-ttu-id="d381c-124">巨集定義陣列的指標 (參閱 [**D3D10 \_ 著色器 \_ 宏**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) 。</span><span class="sxs-lookup"><span data-stu-id="d381c-124">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="d381c-125">陣列中的最後一個結構作為結束字元，且必須將所有成員設定為0。</span><span class="sxs-lookup"><span data-stu-id="d381c-125">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="d381c-126">如果未使用，請將 *pDefines* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d381c-126">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d381c-127">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d381c-127">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d381c-128">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="d381c-128">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="d381c-129">選擇性。</span><span class="sxs-lookup"><span data-stu-id="d381c-129">Optional.</span></span> <span data-ttu-id="d381c-130">處理 include 檔之介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d381c-130">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="d381c-131">若將此 **值** 設定為 Null，將會導致編譯錯誤（如果著色器包含） \# 。</span><span class="sxs-lookup"><span data-stu-id="d381c-131">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="d381c-132">*pFunctionName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d381c-132">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d381c-133">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d381c-133">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d381c-134">著色器開始執行的著色器輸入點函式名稱。</span><span class="sxs-lookup"><span data-stu-id="d381c-134">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="d381c-135">當您編譯效果時， **D3DX11CompileFromMemory** 會忽略 *pFunctionName*;建議您將 *pFunctionName* 設定為 **null** ，因為如果所呼叫的函式不會使用它，則將指標參數設定為 **null** ，是很好的程式設計作法。</span><span class="sxs-lookup"><span data-stu-id="d381c-135">When you compile an effect, **D3DX11CompileFromMemory** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="d381c-136">*pProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d381c-136">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d381c-137">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d381c-137">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d381c-138">指定著色器模型的字串。可以是著色器模型2、著色器模型3、著色器模型4或著色器模型5中的任何設定檔。</span><span class="sxs-lookup"><span data-stu-id="d381c-138">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="d381c-139">設定檔也可以是適用于效果類型 (例如 fx \_ 4 \_ 1) 。</span><span class="sxs-lookup"><span data-stu-id="d381c-139">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="d381c-140">*Flags1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d381c-140">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d381c-141">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d381c-141">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d381c-142">著色器 [**編譯旗標**](/windows/desktop/direct3dhlsl/d3dcompile-constants)。</span><span class="sxs-lookup"><span data-stu-id="d381c-142">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="d381c-143">*Flags2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d381c-143">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d381c-144">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d381c-144">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d381c-145">效果 [**編譯旗標**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)。</span><span class="sxs-lookup"><span data-stu-id="d381c-145">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="d381c-146">當您編譯著色器而非效果檔案時， **D3DX11CompileFromMemory** 會忽略 *Flags2*;我們建議您將 *Flags2* 設定為零，因為如果所呼叫的函式不會使用它，則將指標參數設定為零是很好的程式設計作法。</span><span class="sxs-lookup"><span data-stu-id="d381c-146">When you compile a shader and not an effect file, **D3DX11CompileFromMemory** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="d381c-147">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d381c-147">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d381c-148">類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="d381c-148">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="d381c-149">執行緒抽取介面的指標 (查看 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="d381c-149">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="d381c-150">使用 **Null** 來指定此函式必須等到完成後才會傳回。</span><span class="sxs-lookup"><span data-stu-id="d381c-150">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="d381c-151">*ppShader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d381c-151">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d381c-152">類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d381c-152">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d381c-153">記憶體的指標，其中包含已編譯的著色器，以及任何內嵌的 debug 和符號表資訊。</span><span class="sxs-lookup"><span data-stu-id="d381c-153">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="d381c-154">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d381c-154">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d381c-155">類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d381c-155">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d381c-156">記憶體的指標，其中包含在編譯期間發生的錯誤和警告清單。</span><span class="sxs-lookup"><span data-stu-id="d381c-156">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="d381c-157">這些錯誤和警告與偵錯工具的偵錯工具輸出完全相同。</span><span class="sxs-lookup"><span data-stu-id="d381c-157">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="d381c-158">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d381c-158">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d381c-159">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="d381c-159">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="d381c-160">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="d381c-160">A pointer to the return value.</span></span> <span data-ttu-id="d381c-161">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d381c-161">May be **NULL**.</span></span> <span data-ttu-id="d381c-162">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="d381c-162">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d381c-163">傳回值</span><span class="sxs-lookup"><span data-stu-id="d381c-163">Return value</span></span>

<span data-ttu-id="d381c-164">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d381c-164">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d381c-165">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d381c-165">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="d381c-166">如果您將 \_ **null** 提供給 *pPump* 參數，則 D3DX11CompileFromMemory 會傳回 E INVALIDARG，如果您將非 **null** 提供給 *pHResult* 參數。</span><span class="sxs-lookup"><span data-stu-id="d381c-166">**D3DX11CompileFromMemory** returns E\_INVALIDARG if you supply non-**NULL** to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="d381c-167">如需這種情況的詳細資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="d381c-167">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="d381c-168">備註</span><span class="sxs-lookup"><span data-stu-id="d381c-168">Remarks</span></span>

<span data-ttu-id="d381c-169">如需 **D3DX11CompileFromMemory** 的詳細資訊，請參閱 [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile)。</span><span class="sxs-lookup"><span data-stu-id="d381c-169">For more information about **D3DX11CompileFromMemory**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="d381c-170">如果您也提供 **null** 給 *pPump* 參數，則必須將 **null** 提供給 *pHResult* 參數。</span><span class="sxs-lookup"><span data-stu-id="d381c-170">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="d381c-171">否則，您接著無法使用 **D3DX11CompileFromMemory** 在 *ppShader* 參數指向的記憶體中傳回的已編譯著色器程式碼來建立著色器。</span><span class="sxs-lookup"><span data-stu-id="d381c-171">Otherwise, you cannot subsequently create a shader by using the compiled shader code that **D3DX11CompileFromMemory** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="d381c-172">若要從編譯的著色器程式碼建立著色器，請呼叫下列其中一個 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 介面方法：</span><span class="sxs-lookup"><span data-stu-id="d381c-172">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="d381c-173">**CreateComputeShader**</span><span class="sxs-lookup"><span data-stu-id="d381c-173">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="d381c-174">**CreateDomainShader**</span><span class="sxs-lookup"><span data-stu-id="d381c-174">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="d381c-175">**CreateGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="d381c-175">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="d381c-176">**CreateGeometryShaderWithStreamOutput**</span><span class="sxs-lookup"><span data-stu-id="d381c-176">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="d381c-177">**CreateHullShader**</span><span class="sxs-lookup"><span data-stu-id="d381c-177">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="d381c-178">**CreatePixelShader**</span><span class="sxs-lookup"><span data-stu-id="d381c-178">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="d381c-179">**CreateVertexShader**</span><span class="sxs-lookup"><span data-stu-id="d381c-179">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="d381c-180">此外，如果您在提供 **null** 給 *pPump* 時，將非 **Null** 值提供給 *pHResult* ， **D3DX11CompileFromMemory** 就會傳回 E \_ INVALIDARG 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d381c-180">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromMemory** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d381c-181">規格需求</span><span class="sxs-lookup"><span data-stu-id="d381c-181">Requirements</span></span>



| <span data-ttu-id="d381c-182">需求</span><span class="sxs-lookup"><span data-stu-id="d381c-182">Requirement</span></span> | <span data-ttu-id="d381c-183">值</span><span class="sxs-lookup"><span data-stu-id="d381c-183">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d381c-184">標頭</span><span class="sxs-lookup"><span data-stu-id="d381c-184">Header</span></span><br/>  | <dl> <span data-ttu-id="d381c-185"><dt>D3DX11async。h</dt></span><span class="sxs-lookup"><span data-stu-id="d381c-185"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="d381c-186">程式庫</span><span class="sxs-lookup"><span data-stu-id="d381c-186">Library</span></span><br/> | <dl> <span data-ttu-id="d381c-187"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d381c-187"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d381c-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d381c-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d381c-189">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="d381c-189">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

