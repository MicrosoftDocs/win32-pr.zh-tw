---
description: 請注意，我們建議您不要使用此舊版函式，而是使用 Fxc.exe 命令列編譯器或使用 D3DCompile API，以離線方式編譯。 從檔案編譯著色器或效果。
ms.assetid: b0ca0b6a-3ff0-49ee-83de-14c4686a7104
title: D3DX10CompileFromFile 函式 (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 571f8123a9834c95ecca6043c3495fb18fbaca47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000617"
---
# <a name="d3dx10compilefromfile-function"></a><span data-ttu-id="71a6e-104">D3DX10CompileFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="71a6e-104">D3DX10CompileFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="71a6e-105">我們建議您不要使用此舊版函式，而是使用 Fxc.exe 命令列編譯器或使用 [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API，以離線方式編譯。</span><span class="sxs-lookup"><span data-stu-id="71a6e-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="71a6e-106">從檔案編譯著色器或效果。</span><span class="sxs-lookup"><span data-stu-id="71a6e-106">Compile a shader or an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="71a6e-107">語法</span><span class="sxs-lookup"><span data-stu-id="71a6e-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="71a6e-108">參數</span><span class="sxs-lookup"><span data-stu-id="71a6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71a6e-109">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="71a6e-109">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71a6e-110">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71a6e-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71a6e-111">包含著色器程式碼的檔案名。</span><span class="sxs-lookup"><span data-stu-id="71a6e-111">The name of the file that contains the shader code.</span></span> <span data-ttu-id="71a6e-112">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="71a6e-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="71a6e-113">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="71a6e-113">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="71a6e-114">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="71a6e-114">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71a6e-115">Type： **Const [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="71a6e-115">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="71a6e-116">選擇性。</span><span class="sxs-lookup"><span data-stu-id="71a6e-116">Optional.</span></span> <span data-ttu-id="71a6e-117">巨集定義陣列的指標 (參閱 [**D3D \_ 著色器 \_ 宏**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)) 。</span><span class="sxs-lookup"><span data-stu-id="71a6e-117">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="71a6e-118">陣列中的最後一個結構作為結束字元，且必須將所有成員設定為0。</span><span class="sxs-lookup"><span data-stu-id="71a6e-118">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="71a6e-119">如果未使用，請將 *pDefines* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="71a6e-119">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="71a6e-120">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="71a6e-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71a6e-121">類型： **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="71a6e-121">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="71a6e-122">選擇性。</span><span class="sxs-lookup"><span data-stu-id="71a6e-122">Optional.</span></span> <span data-ttu-id="71a6e-123">用來處理 include 檔案的 [**ID3D10Include 介面**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="71a6e-123">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="71a6e-124">若將此 **值** 設定為 Null，將會導致編譯錯誤（如果著色器包含） \# 。</span><span class="sxs-lookup"><span data-stu-id="71a6e-124">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="71a6e-125">*pFunctionName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="71a6e-125">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71a6e-126">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71a6e-126">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71a6e-127">著色器開始執行的著色器輸入點函式名稱。</span><span class="sxs-lookup"><span data-stu-id="71a6e-127">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="71a6e-128">當您編譯效果時， **D3DX10CompileFromFile** 會忽略 *pFunctionName*;建議您將 *pFunctionName* 設定為 **null** ，因為如果所呼叫的函式不會使用它，則將指標參數設定為 **null** ，是很好的程式設計作法。</span><span class="sxs-lookup"><span data-stu-id="71a6e-128">When you compile an effect, **D3DX10CompileFromFile** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="71a6e-129">*pProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="71a6e-129">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71a6e-130">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71a6e-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71a6e-131">指定著色器模型的字串。可以是 [著色器模型 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md)、 [著色器模型 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)或 [著色器模型 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md)中的任何設定檔。</span><span class="sxs-lookup"><span data-stu-id="71a6e-131">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="71a6e-132">*Flags1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="71a6e-132">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71a6e-133">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71a6e-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71a6e-134">[著色器編譯旗標](d3d10-shader.md)。</span><span class="sxs-lookup"><span data-stu-id="71a6e-134">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="71a6e-135">*Flags2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="71a6e-135">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71a6e-136">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71a6e-136">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71a6e-137">[效果編譯旗標](d3d10-graphics-reference-effect-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="71a6e-137">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="71a6e-138">當您編譯著色器而非效果檔案時， **D3DX10CompileFromFile** 會忽略 *Flags2*;我們建議您將 *Flags2* 設定為零，因為如果所呼叫的函式不會使用它，則將指標參數設定為零是很好的程式設計作法。</span><span class="sxs-lookup"><span data-stu-id="71a6e-138">When you compile a shader and not an effect file, **D3DX10CompileFromFile** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="71a6e-139">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="71a6e-139">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71a6e-140">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="71a6e-140">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="71a6e-141">執行緒抽取介面的指標 (查看 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="71a6e-141">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="71a6e-142">使用 **Null** 來指定此函式必須等到完成後才會傳回。</span><span class="sxs-lookup"><span data-stu-id="71a6e-142">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="71a6e-143">*ppShader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="71a6e-143">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71a6e-144">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="71a6e-144">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="71a6e-145">[**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)的指標，其中包含已編譯的著色器，以及任何內嵌的 debug 和符號表資訊。</span><span class="sxs-lookup"><span data-stu-id="71a6e-145">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="71a6e-146">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="71a6e-146">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71a6e-147">類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="71a6e-147">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="71a6e-148">[**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)的指標，其中包含在編譯期間發生的錯誤和警告清單。</span><span class="sxs-lookup"><span data-stu-id="71a6e-148">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="71a6e-149">這些錯誤和警告與偵錯工具的偵錯工具輸出完全相同。</span><span class="sxs-lookup"><span data-stu-id="71a6e-149">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="71a6e-150">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="71a6e-150">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71a6e-151">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="71a6e-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="71a6e-152">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="71a6e-152">A pointer to the return value.</span></span> <span data-ttu-id="71a6e-153">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="71a6e-153">May be **NULL**.</span></span> <span data-ttu-id="71a6e-154">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="71a6e-154">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71a6e-155">傳回值</span><span class="sxs-lookup"><span data-stu-id="71a6e-155">Return value</span></span>

<span data-ttu-id="71a6e-156">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="71a6e-156">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="71a6e-157">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="71a6e-157">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="71a6e-158">備註</span><span class="sxs-lookup"><span data-stu-id="71a6e-158">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="71a6e-159">需求</span><span class="sxs-lookup"><span data-stu-id="71a6e-159">Requirements</span></span>



| <span data-ttu-id="71a6e-160">需求</span><span class="sxs-lookup"><span data-stu-id="71a6e-160">Requirement</span></span> | <span data-ttu-id="71a6e-161">值</span><span class="sxs-lookup"><span data-stu-id="71a6e-161">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="71a6e-162">標頭</span><span class="sxs-lookup"><span data-stu-id="71a6e-162">Header</span></span><br/> | <dl> <span data-ttu-id="71a6e-163"><dt>D3DX10Async。h</dt></span><span class="sxs-lookup"><span data-stu-id="71a6e-163"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71a6e-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71a6e-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71a6e-165">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="71a6e-165">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
