---
title: 'D3DX11CompileFromFile 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用這個函式，而是使用 Fxc.exe 命令列編譯器，或使用其中一個 HLSL 編譯 Api （例如 D3DCompileFromFile API），以離線方式編譯。 從檔案編譯著色器或效果。
ms.assetid: 91a1a339-50da-4f86-9b55-6af246a60482
keywords:
- D3DX11CompileFromFile 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c9194eb54652304c220e5a4de0ee12a26ea1a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116257"
---
# <a name="d3dx11compilefromfile-function"></a><span data-ttu-id="c030b-106">D3DX11CompileFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="c030b-106">D3DX11CompileFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="c030b-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="c030b-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="c030b-108">我們建議您不要使用這個函式，而是使用 Fxc.exe 命令列編譯器，或使用其中一個 HLSL 編譯 Api （例如 [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) API），以離線方式編譯。</span><span class="sxs-lookup"><span data-stu-id="c030b-108">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) API.</span></span>

 

<span data-ttu-id="c030b-109">從檔案編譯著色器或效果。</span><span class="sxs-lookup"><span data-stu-id="c030b-109">Compile a shader or an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c030b-110">語法</span><span class="sxs-lookup"><span data-stu-id="c030b-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="c030b-111">參數</span><span class="sxs-lookup"><span data-stu-id="c030b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c030b-112">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c030b-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c030b-113">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c030b-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c030b-114">包含著色器程式碼的檔案名。</span><span class="sxs-lookup"><span data-stu-id="c030b-114">The name of the file that contains the shader code.</span></span> <span data-ttu-id="c030b-115">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="c030b-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="c030b-116">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="c030b-116">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="c030b-117">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c030b-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c030b-118">Type： **Const [**D3D10 \_ 著色器 \_ 宏**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="c030b-118">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="c030b-119">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c030b-119">Optional.</span></span> <span data-ttu-id="c030b-120">巨集定義陣列的指標 (參閱 [**D3D10 \_ 著色器 \_ 宏**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) 。</span><span class="sxs-lookup"><span data-stu-id="c030b-120">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="c030b-121">陣列中的最後一個結構作為結束字元，且必須將所有成員設定為0。</span><span class="sxs-lookup"><span data-stu-id="c030b-121">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="c030b-122">如果未使用，請將 *pDefines* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c030b-122">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c030b-123">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c030b-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c030b-124">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="c030b-124">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="c030b-125">選擇性。</span><span class="sxs-lookup"><span data-stu-id="c030b-125">Optional.</span></span> <span data-ttu-id="c030b-126">處理 include 檔之介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c030b-126">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="c030b-127">若將此 **值** 設定為 Null，將會導致編譯錯誤（如果著色器包含） \# 。</span><span class="sxs-lookup"><span data-stu-id="c030b-127">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="c030b-128">*pFunctionName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c030b-128">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c030b-129">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c030b-129">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c030b-130">著色器開始執行的著色器輸入點函式名稱。</span><span class="sxs-lookup"><span data-stu-id="c030b-130">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="c030b-131">當您編譯效果時， **D3DX11CompileFromFile** 會忽略 *pFunctionName*;建議您將 *pFunctionName* 設定為 **null** ，因為如果所呼叫的函式不會使用它，則將指標參數設定為 **null** ，是很好的程式設計作法。</span><span class="sxs-lookup"><span data-stu-id="c030b-131">When you compile an effect, **D3DX11CompileFromFile** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="c030b-132">*pProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c030b-132">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c030b-133">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c030b-133">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c030b-134">指定著色器模型的字串。可以是著色器模型2、著色器模型3、著色器模型4或著色器模型5中的任何設定檔。</span><span class="sxs-lookup"><span data-stu-id="c030b-134">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="c030b-135">設定檔也可以是適用于效果類型 (例如 fx \_ 4 \_ 1) 。</span><span class="sxs-lookup"><span data-stu-id="c030b-135">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="c030b-136">*Flags1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c030b-136">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c030b-137">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c030b-137">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c030b-138">著色器 [**編譯旗標**](/windows/desktop/direct3dhlsl/d3dcompile-constants)。</span><span class="sxs-lookup"><span data-stu-id="c030b-138">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="c030b-139">*Flags2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c030b-139">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c030b-140">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c030b-140">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c030b-141">效果 [**編譯旗標**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)。</span><span class="sxs-lookup"><span data-stu-id="c030b-141">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="c030b-142">當您編譯著色器而非效果檔案時， **D3DX11CompileFromFile** 會忽略 *Flags2*;我們建議您將 *Flags2* 設定為零，因為如果所呼叫的函式不會使用它，則將指標參數設定為零是很好的程式設計作法。</span><span class="sxs-lookup"><span data-stu-id="c030b-142">When you compile a shader and not an effect file, **D3DX11CompileFromFile** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="c030b-143">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c030b-143">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c030b-144">類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="c030b-144">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="c030b-145">執行緒抽取介面的指標 (查看 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="c030b-145">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="c030b-146">使用 **Null** 來指定此函式必須等到完成後才會傳回。</span><span class="sxs-lookup"><span data-stu-id="c030b-146">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="c030b-147">*ppShader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c030b-147">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c030b-148">類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c030b-148">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c030b-149">記憶體的指標，其中包含已編譯的著色器，以及任何內嵌的 debug 和符號表資訊。</span><span class="sxs-lookup"><span data-stu-id="c030b-149">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="c030b-150">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c030b-150">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c030b-151">類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c030b-151">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c030b-152">記憶體的指標，其中包含在編譯期間發生的錯誤和警告清單。</span><span class="sxs-lookup"><span data-stu-id="c030b-152">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="c030b-153">這些錯誤和警告與偵錯工具的偵錯工具輸出完全相同。</span><span class="sxs-lookup"><span data-stu-id="c030b-153">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="c030b-154">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c030b-154">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c030b-155">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="c030b-155">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="c030b-156">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="c030b-156">A pointer to the return value.</span></span> <span data-ttu-id="c030b-157">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c030b-157">May be **NULL**.</span></span> <span data-ttu-id="c030b-158">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="c030b-158">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c030b-159">傳回值</span><span class="sxs-lookup"><span data-stu-id="c030b-159">Return value</span></span>

<span data-ttu-id="c030b-160">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c030b-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c030b-161">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c030b-161">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="c030b-162">如果您將 \_ **null** 提供給 *pPump* 參數，則 D3DX11CompileFromFile 會傳回 E INVALIDARG，如果您提供非 **null** 值給 *pHResult* 參數。</span><span class="sxs-lookup"><span data-stu-id="c030b-162">**D3DX11CompileFromFile** returns E\_INVALIDARG if you supply a non-**NULL** value to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="c030b-163">如需這種情況的詳細資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c030b-163">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="c030b-164">備註</span><span class="sxs-lookup"><span data-stu-id="c030b-164">Remarks</span></span>

<span data-ttu-id="c030b-165">如需 **D3DX11CompileFromFile** 的詳細資訊，請參閱 [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile)。</span><span class="sxs-lookup"><span data-stu-id="c030b-165">For more information about **D3DX11CompileFromFile**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="c030b-166">如果您也提供 **null** 給 *pPump* 參數，則必須將 **null** 提供給 *pHResult* 參數。</span><span class="sxs-lookup"><span data-stu-id="c030b-166">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="c030b-167">否則，您無法使用 **D3DX11CompileFromFile** 在 *ppShader* 參數指向的記憶體中傳回的已編譯著色器程式碼來建立著色器。</span><span class="sxs-lookup"><span data-stu-id="c030b-167">Otherwise, you cannot create a shader by using the compiled shader code that **D3DX11CompileFromFile** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="c030b-168">若要從編譯的著色器程式碼建立著色器，請呼叫下列其中一個 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 介面方法：</span><span class="sxs-lookup"><span data-stu-id="c030b-168">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="c030b-169">**CreateComputeShader**</span><span class="sxs-lookup"><span data-stu-id="c030b-169">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="c030b-170">**CreateDomainShader**</span><span class="sxs-lookup"><span data-stu-id="c030b-170">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="c030b-171">**CreateGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="c030b-171">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="c030b-172">**CreateGeometryShaderWithStreamOutput**</span><span class="sxs-lookup"><span data-stu-id="c030b-172">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="c030b-173">**CreateHullShader**</span><span class="sxs-lookup"><span data-stu-id="c030b-173">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="c030b-174">**CreatePixelShader**</span><span class="sxs-lookup"><span data-stu-id="c030b-174">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="c030b-175">**CreateVertexShader**</span><span class="sxs-lookup"><span data-stu-id="c030b-175">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="c030b-176">此外，如果您在提供 **null** 給 *pPump* 時，將非 **Null** 值提供給 *pHResult* ， **D3DX11CompileFromFile** 就會傳回 E \_ INVALIDARG 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c030b-176">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromFile** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c030b-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="c030b-177">Requirements</span></span>



| <span data-ttu-id="c030b-178">需求</span><span class="sxs-lookup"><span data-stu-id="c030b-178">Requirement</span></span> | <span data-ttu-id="c030b-179">值</span><span class="sxs-lookup"><span data-stu-id="c030b-179">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c030b-180">標頭</span><span class="sxs-lookup"><span data-stu-id="c030b-180">Header</span></span><br/>  | <dl> <span data-ttu-id="c030b-181"><dt>D3DX11async。h</dt></span><span class="sxs-lookup"><span data-stu-id="c030b-181"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="c030b-182">程式庫</span><span class="sxs-lookup"><span data-stu-id="c030b-182">Library</span></span><br/> | <dl> <span data-ttu-id="c030b-183"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c030b-183"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c030b-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c030b-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c030b-185">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="c030b-185">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

