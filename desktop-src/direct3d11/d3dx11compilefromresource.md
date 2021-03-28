---
title: 'D3DX11CompileFromResource 函式 (D3DX11async) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 請注意，我們建議您不要使用此函式，而是使用資源函式，然後使用 Fxc.exe 命令列編譯器或使用其中一個 HLSL 編譯 Api （例如 D3DCompile API），以離線方式編譯。 從資源編譯著色器或效果。
ms.assetid: ececa469-f5e3-4cb3-befe-0ed1a5a57671
keywords:
- D3DX11CompileFromResource 函式 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b26eeb825a1d3b6bcda9f77eae24c99c3cec168b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946182"
---
# <a name="d3dx11compilefromresource-function"></a><span data-ttu-id="39d8d-106">D3DX11CompileFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="39d8d-106">D3DX11CompileFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="39d8d-107">D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="39d8d-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="39d8d-108">我們建議您不要使用此函式，而是使用 [資源](/windows/desktop/menurc/resources-functions)函式，然後使用 Fxc.exe 命令列編譯器或使用其中一個 HLSL 編譯 api （例如 [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API），以離線方式編譯。</span><span class="sxs-lookup"><span data-stu-id="39d8d-108">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API.</span></span>

 

<span data-ttu-id="39d8d-109">從資源編譯著色器或效果。</span><span class="sxs-lookup"><span data-stu-id="39d8d-109">Compile a shader or an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="39d8d-110">語法</span><span class="sxs-lookup"><span data-stu-id="39d8d-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
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



## <a name="parameters"></a><span data-ttu-id="39d8d-111">參數</span><span class="sxs-lookup"><span data-stu-id="39d8d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39d8d-112">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39d8d-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d8d-113">類型： **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="39d8d-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="39d8d-114">包含著色器之資源模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="39d8d-114">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="39d8d-115">您可以使用 [GetModuleHandle 函數](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)來取得 HMODULE。</span><span class="sxs-lookup"><span data-stu-id="39d8d-115">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="39d8d-116">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39d8d-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d8d-117">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="39d8d-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="39d8d-118">包含著色器之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="39d8d-118">Name of the resource containing the shader.</span></span> <span data-ttu-id="39d8d-119">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="39d8d-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="39d8d-120">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="39d8d-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="39d8d-121">*pSrcFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39d8d-121">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d8d-122">類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="39d8d-122">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="39d8d-123">選擇性。</span><span class="sxs-lookup"><span data-stu-id="39d8d-123">Optional.</span></span> <span data-ttu-id="39d8d-124">效果檔案名，只用于錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="39d8d-124">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="39d8d-125">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="39d8d-125">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="39d8d-126">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39d8d-126">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d8d-127">Type： **Const [**D3D10 \_ 著色器 \_ 宏**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="39d8d-127">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="39d8d-128">選擇性。</span><span class="sxs-lookup"><span data-stu-id="39d8d-128">Optional.</span></span> <span data-ttu-id="39d8d-129">巨集定義陣列的指標 (參閱 [**D3D10 \_ 著色器 \_ 宏**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) 。</span><span class="sxs-lookup"><span data-stu-id="39d8d-129">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="39d8d-130">陣列中的最後一個結構作為結束字元，且必須將所有成員設定為0。</span><span class="sxs-lookup"><span data-stu-id="39d8d-130">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="39d8d-131">如果未使用，請將 *pDefines* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="39d8d-131">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="39d8d-132">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39d8d-132">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d8d-133">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="39d8d-133">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="39d8d-134">選擇性。</span><span class="sxs-lookup"><span data-stu-id="39d8d-134">Optional.</span></span> <span data-ttu-id="39d8d-135">處理 include 檔之介面的指標。</span><span class="sxs-lookup"><span data-stu-id="39d8d-135">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="39d8d-136">若將此 **值** 設定為 Null，將會導致編譯錯誤（如果著色器包含） \# 。</span><span class="sxs-lookup"><span data-stu-id="39d8d-136">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="39d8d-137">*pFunctionName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39d8d-137">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d8d-138">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="39d8d-138">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="39d8d-139">著色器開始執行的著色器輸入點函式名稱。</span><span class="sxs-lookup"><span data-stu-id="39d8d-139">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="39d8d-140">當您編譯效果時， **D3DX11CompileFromResource** 會忽略 *pFunctionName*;建議您將 *pFunctionName* 設定為 **null** ，因為如果所呼叫的函式不會使用它，則將指標參數設定為 **null** ，是很好的程式設計作法。</span><span class="sxs-lookup"><span data-stu-id="39d8d-140">When you compile an effect, **D3DX11CompileFromResource** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="39d8d-141">*pProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39d8d-141">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d8d-142">類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="39d8d-142">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="39d8d-143">指定著色器模型的字串。可以是著色器模型2、著色器模型3、著色器模型4或著色器模型5中的任何設定檔。</span><span class="sxs-lookup"><span data-stu-id="39d8d-143">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="39d8d-144">設定檔也可以是適用于效果類型 (例如 fx \_ 4 \_ 1) 。</span><span class="sxs-lookup"><span data-stu-id="39d8d-144">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="39d8d-145">*Flags1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39d8d-145">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d8d-146">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="39d8d-146">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="39d8d-147">著色器 [**編譯旗標**](/windows/desktop/direct3dhlsl/d3dcompile-constants)。</span><span class="sxs-lookup"><span data-stu-id="39d8d-147">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="39d8d-148">*Flags2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39d8d-148">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d8d-149">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="39d8d-149">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="39d8d-150">效果 [**編譯旗標**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)。</span><span class="sxs-lookup"><span data-stu-id="39d8d-150">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="39d8d-151">當您編譯著色器而非效果檔案時， **D3DX11CompileFromResource** 會忽略 *Flags2*;我們建議您將 *Flags2* 設定為零，因為如果所呼叫的函式不會使用它，則將指標參數設定為零是很好的程式設計作法。</span><span class="sxs-lookup"><span data-stu-id="39d8d-151">When you compile a shader and not an effect file, **D3DX11CompileFromResource** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="39d8d-152">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39d8d-152">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d8d-153">類型： **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="39d8d-153">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="39d8d-154">執行緒抽取介面的指標 (查看 [**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="39d8d-154">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="39d8d-155">使用 **Null** 來指定此函式必須等到完成後才會傳回。</span><span class="sxs-lookup"><span data-stu-id="39d8d-155">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="39d8d-156">*ppShader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="39d8d-156">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39d8d-157">類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="39d8d-157">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="39d8d-158">記憶體的指標，其中包含已編譯的著色器，以及任何內嵌的 debug 和符號表資訊。</span><span class="sxs-lookup"><span data-stu-id="39d8d-158">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="39d8d-159">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="39d8d-159">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39d8d-160">類型： **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="39d8d-160">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="39d8d-161">記憶體的指標，其中包含在編譯期間發生的錯誤和警告清單。</span><span class="sxs-lookup"><span data-stu-id="39d8d-161">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="39d8d-162">這些錯誤和警告與偵錯工具的偵錯工具輸出完全相同。</span><span class="sxs-lookup"><span data-stu-id="39d8d-162">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="39d8d-163">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="39d8d-163">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39d8d-164">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="39d8d-164">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="39d8d-165">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="39d8d-165">A pointer to the return value.</span></span> <span data-ttu-id="39d8d-166">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="39d8d-166">May be **NULL**.</span></span> <span data-ttu-id="39d8d-167">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="39d8d-167">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39d8d-168">傳回值</span><span class="sxs-lookup"><span data-stu-id="39d8d-168">Return value</span></span>

<span data-ttu-id="39d8d-169">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="39d8d-169">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="39d8d-170">傳回值是 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="39d8d-170">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="39d8d-171">如果您將 \_ **null** 提供給 *pPump* 參數，則 D3DX11CompileFromResource 會傳回 E INVALIDARG，如果您將非 **null** 提供給 *pHResult* 參數。</span><span class="sxs-lookup"><span data-stu-id="39d8d-171">**D3DX11CompileFromResource** returns E\_INVALIDARG if you supply non-**NULL** to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="39d8d-172">如需這種情況的詳細資訊，請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="39d8d-172">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="39d8d-173">備註</span><span class="sxs-lookup"><span data-stu-id="39d8d-173">Remarks</span></span>

<span data-ttu-id="39d8d-174">如需 **D3DX11CompileFromResource** 的詳細資訊，請參閱 [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile)。</span><span class="sxs-lookup"><span data-stu-id="39d8d-174">For more information about **D3DX11CompileFromResource**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="39d8d-175">如果您也提供 **null** 給 *pPump* 參數，則必須將 **null** 提供給 *pHResult* 參數。</span><span class="sxs-lookup"><span data-stu-id="39d8d-175">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="39d8d-176">否則，您接著無法使用 **D3DX11CompileFromResource** 在 *ppShader* 參數指向的記憶體中傳回的已編譯著色器程式碼來建立著色器。</span><span class="sxs-lookup"><span data-stu-id="39d8d-176">Otherwise, you cannot subsequently create a shader by using the compiled shader code that **D3DX11CompileFromResource** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="39d8d-177">若要從編譯的著色器程式碼建立著色器，請呼叫下列其中一個 [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) 介面方法：</span><span class="sxs-lookup"><span data-stu-id="39d8d-177">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="39d8d-178">**CreateComputeShader**</span><span class="sxs-lookup"><span data-stu-id="39d8d-178">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="39d8d-179">**CreateDomainShader**</span><span class="sxs-lookup"><span data-stu-id="39d8d-179">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="39d8d-180">**CreateGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="39d8d-180">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="39d8d-181">**CreateGeometryShaderWithStreamOutput**</span><span class="sxs-lookup"><span data-stu-id="39d8d-181">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="39d8d-182">**CreateHullShader**</span><span class="sxs-lookup"><span data-stu-id="39d8d-182">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="39d8d-183">**CreatePixelShader**</span><span class="sxs-lookup"><span data-stu-id="39d8d-183">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="39d8d-184">**CreateVertexShader**</span><span class="sxs-lookup"><span data-stu-id="39d8d-184">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="39d8d-185">此外，如果您在提供 **null** 給 *pPump* 時，將非 **Null** 值提供給 *pHResult* ， **D3DX11CompileFromResource** 就會傳回 E \_ INVALIDARG 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="39d8d-185">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromResource** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="39d8d-186">規格需求</span><span class="sxs-lookup"><span data-stu-id="39d8d-186">Requirements</span></span>



| <span data-ttu-id="39d8d-187">需求</span><span class="sxs-lookup"><span data-stu-id="39d8d-187">Requirement</span></span> | <span data-ttu-id="39d8d-188">值</span><span class="sxs-lookup"><span data-stu-id="39d8d-188">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="39d8d-189">標頭</span><span class="sxs-lookup"><span data-stu-id="39d8d-189">Header</span></span><br/>  | <dl> <span data-ttu-id="39d8d-190"><dt>D3DX11async。h</dt></span><span class="sxs-lookup"><span data-stu-id="39d8d-190"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="39d8d-191">程式庫</span><span class="sxs-lookup"><span data-stu-id="39d8d-191">Library</span></span><br/> | <dl> <span data-ttu-id="39d8d-192"><dt>D3DX11 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="39d8d-192"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="39d8d-193">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39d8d-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39d8d-194">D3DX 函式</span><span class="sxs-lookup"><span data-stu-id="39d8d-194">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

