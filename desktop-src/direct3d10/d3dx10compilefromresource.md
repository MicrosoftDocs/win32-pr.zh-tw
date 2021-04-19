---
description: 請注意，我們建議您不要使用此舊版函式，而是使用 Fxc.exe 命令列編譯器或使用 D3DCompile API，以離線方式編譯。 從資源編譯著色器或效果。
ms.assetid: d291e47d-e04f-4e2d-9d05-9aef8e4fcf7e
title: D3DX10CompileFromResource 函式 (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 6b698700804ca767c953343e6d5a5e540ca77555
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992304"
---
# <a name="d3dx10compilefromresource-function"></a><span data-ttu-id="06f6d-104">D3DX10CompileFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="06f6d-104">D3DX10CompileFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="06f6d-105">我們建議您不要使用此舊版函式，而是使用 Fxc.exe 命令列編譯器或使用 [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API，以離線方式編譯。</span><span class="sxs-lookup"><span data-stu-id="06f6d-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="06f6d-106">從資源編譯著色器或效果。</span><span class="sxs-lookup"><span data-stu-id="06f6d-106">Compile a shader or an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="06f6d-107">語法</span><span class="sxs-lookup"><span data-stu-id="06f6d-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="06f6d-108">參數</span><span class="sxs-lookup"><span data-stu-id="06f6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06f6d-109">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06f6d-109">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06f6d-110">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06f6d-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06f6d-111">包含著色器之資源模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="06f6d-111">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="06f6d-112">您可以使用 [GetModuleHandle 函數](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)來取得 HMODULE。</span><span class="sxs-lookup"><span data-stu-id="06f6d-112">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="06f6d-113">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06f6d-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06f6d-114">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06f6d-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06f6d-115">包含著色器之資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="06f6d-115">Name of the resource containing the shader.</span></span> <span data-ttu-id="06f6d-116">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="06f6d-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="06f6d-117">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="06f6d-117">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="06f6d-118">*pSrcFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06f6d-118">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06f6d-119">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06f6d-119">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06f6d-120">選擇性。</span><span class="sxs-lookup"><span data-stu-id="06f6d-120">Optional.</span></span> <span data-ttu-id="06f6d-121">效果檔案名，只用于錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="06f6d-121">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="06f6d-122">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="06f6d-122">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="06f6d-123">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06f6d-123">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06f6d-124">Type： **Const [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="06f6d-124">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="06f6d-125">選擇性。</span><span class="sxs-lookup"><span data-stu-id="06f6d-125">Optional.</span></span> <span data-ttu-id="06f6d-126">巨集定義陣列的指標 (參閱 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) 。</span><span class="sxs-lookup"><span data-stu-id="06f6d-126">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="06f6d-127">陣列中的最後一個結構作為結束字元，且必須將所有成員設定為0。</span><span class="sxs-lookup"><span data-stu-id="06f6d-127">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="06f6d-128">如果未使用，請將 *pDefines* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="06f6d-128">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="06f6d-129">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06f6d-129">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06f6d-130">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="06f6d-130">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="06f6d-131">選擇性。</span><span class="sxs-lookup"><span data-stu-id="06f6d-131">Optional.</span></span> <span data-ttu-id="06f6d-132">用來處理 include 檔案的 [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="06f6d-132">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="06f6d-133">若將此 **值** 設定為 Null，將會導致編譯錯誤（如果著色器包含） \# 。</span><span class="sxs-lookup"><span data-stu-id="06f6d-133">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="06f6d-134">*pFunctionName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06f6d-134">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06f6d-135">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06f6d-135">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06f6d-136">著色器開始執行的著色器輸入點函式名稱。</span><span class="sxs-lookup"><span data-stu-id="06f6d-136">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="06f6d-137">當您編譯效果時， **D3DX10CompileFromResource** 會忽略 *pFunctionName*;建議您將 *pFunctionName* 設定為 **null** ，因為如果所呼叫的函式不會使用它，則將指標參數設定為 **null** ，是很好的程式設計作法。</span><span class="sxs-lookup"><span data-stu-id="06f6d-137">When you compile an effect, **D3DX10CompileFromResource** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="06f6d-138">*pProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06f6d-138">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06f6d-139">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06f6d-139">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06f6d-140">指定著色器模型的字串。可以是 [著色器模型 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md)、 [著色器模型 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)或 [著色器模型 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md)中的任何設定檔。</span><span class="sxs-lookup"><span data-stu-id="06f6d-140">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="06f6d-141">*Flags1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06f6d-141">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06f6d-142">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06f6d-142">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06f6d-143">[著色器編譯旗標](d3d10-shader.md)。</span><span class="sxs-lookup"><span data-stu-id="06f6d-143">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="06f6d-144">*Flags2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06f6d-144">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06f6d-145">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06f6d-145">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="06f6d-146">[效果編譯旗標](d3d10-graphics-reference-effect-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="06f6d-146">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="06f6d-147">當您編譯著色器而非效果檔案時， **D3DX10CompileFromResource** 會忽略 *Flags2*;我們建議您將 *Flags2* 設定為零，因為如果所呼叫的函式不會使用它，則將指標參數設定為零是很好的程式設計作法。</span><span class="sxs-lookup"><span data-stu-id="06f6d-147">When you compile a shader and not an effect file, **D3DX10CompileFromResource** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="06f6d-148">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="06f6d-148">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06f6d-149">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="06f6d-149">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="06f6d-150">執行緒抽取介面的指標 (查看 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="06f6d-150">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="06f6d-151">使用 **Null** 來指定此函式必須等到完成後才會傳回。</span><span class="sxs-lookup"><span data-stu-id="06f6d-151">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="06f6d-152">*ppShader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="06f6d-152">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06f6d-153">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="06f6d-153">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="06f6d-154">[**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)的指標，其中包含已編譯的著色器，以及任何內嵌的 debug 和符號表資訊。</span><span class="sxs-lookup"><span data-stu-id="06f6d-154">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="06f6d-155">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="06f6d-155">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06f6d-156">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="06f6d-156">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="06f6d-157">[**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)的指標，其中包含在編譯期間發生的錯誤和警告清單。</span><span class="sxs-lookup"><span data-stu-id="06f6d-157">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="06f6d-158">這些錯誤和警告與偵錯工具的偵錯工具輸出完全相同。</span><span class="sxs-lookup"><span data-stu-id="06f6d-158">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="06f6d-159">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="06f6d-159">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06f6d-160">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="06f6d-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="06f6d-161">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="06f6d-161">A pointer to the return value.</span></span> <span data-ttu-id="06f6d-162">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="06f6d-162">May be **NULL**.</span></span> <span data-ttu-id="06f6d-163">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="06f6d-163">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06f6d-164">傳回值</span><span class="sxs-lookup"><span data-stu-id="06f6d-164">Return value</span></span>

<span data-ttu-id="06f6d-165">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06f6d-165">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06f6d-166">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="06f6d-166">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="06f6d-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="06f6d-167">Requirements</span></span>



| <span data-ttu-id="06f6d-168">需求</span><span class="sxs-lookup"><span data-stu-id="06f6d-168">Requirement</span></span> | <span data-ttu-id="06f6d-169">值</span><span class="sxs-lookup"><span data-stu-id="06f6d-169">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="06f6d-170">標頭</span><span class="sxs-lookup"><span data-stu-id="06f6d-170">Header</span></span><br/> | <dl> <span data-ttu-id="06f6d-171"><dt>D3DX10Async。h</dt></span><span class="sxs-lookup"><span data-stu-id="06f6d-171"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06f6d-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06f6d-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06f6d-173">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="06f6d-173">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
