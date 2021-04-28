---
description: D3DXCompileShaderFromFile 函式-編譯著色器檔。
ms.assetid: 2ad6042f-3601-4f4a-9624-6319a3372355
title: 'D3DXCompileShaderFromFile 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4392a3c36b31deb4071c215ad9b41e7f40c21ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115846"
---
# <a name="d3dxcompileshaderfromfile-function"></a><span data-ttu-id="76787-103">D3DXCompileShaderFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="76787-103">D3DXCompileShaderFromFile function</span></span>

<span data-ttu-id="76787-104">編譯著色器檔。</span><span class="sxs-lookup"><span data-stu-id="76787-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="76787-105">我們建議您不要使用此舊版函式，而是使用 Fxc.exe 命令列編譯器或使用 [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API，以離線方式編譯。</span><span class="sxs-lookup"><span data-stu-id="76787-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="76787-106">語法</span><span class="sxs-lookup"><span data-stu-id="76787-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShaderFromFile(
  _In_        LPCTSTR             pSrcFile,
  _In_  const D3DXMACRO           *pDefines,
  _In_        LPD3DXINCLUDE       pInclude,
  _In_        LPCSTR              pFunctionName,
  _In_        LPCSTR              pProfile,
  _In_        DWORD               Flags,
  _Out_       LPD3DXBUFFER        *ppShader,
  _Out_       LPD3DXBUFFER        *ppErrorMsgs,
  _Out_       LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="76787-107">參數</span><span class="sxs-lookup"><span data-stu-id="76787-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76787-108">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="76787-108">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76787-109">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76787-109">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76787-110">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="76787-110">Pointer to a string that specifies the filename.</span></span>

</dd> <dt>

<span data-ttu-id="76787-111">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="76787-111">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76787-112">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="76787-112">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="76787-113">[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列。</span><span class="sxs-lookup"><span data-stu-id="76787-113">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="76787-114">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="76787-114">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="76787-115">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="76787-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76787-116">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="76787-116">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="76787-117">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="76787-117">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="76787-118">如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="76787-118">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="76787-119">*pFunctionName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="76787-119">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76787-120">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76787-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76787-121">著色器進入點函式的指標，該函式會開始執行。</span><span class="sxs-lookup"><span data-stu-id="76787-121">Pointer to the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="76787-122">*pProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="76787-122">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76787-123">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76787-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76787-124">著色器設定檔的指標，此設定檔可決定著色器指令集。</span><span class="sxs-lookup"><span data-stu-id="76787-124">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="76787-125">如需可用的配置檔案清單，請參閱 [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) 或 [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) 。</span><span class="sxs-lookup"><span data-stu-id="76787-125">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="76787-126">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="76787-126">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76787-127">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="76787-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="76787-128">不同旗標所識別的編譯選項。</span><span class="sxs-lookup"><span data-stu-id="76787-128">Compile options identified by various flags.</span></span> <span data-ttu-id="76787-129">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="76787-129">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="76787-130">如需詳細資料，請參閱 [D3DXSHADER 旗標](d3dxshader-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="76787-130">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="76787-131">*ppShader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="76787-131">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76787-132">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="76787-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="76787-133">傳回包含已建立之著色器的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="76787-133">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="76787-134">這個緩衝區包含已編譯的著色器程式碼，以及任何內嵌的 debug 和 symbol 資料表資訊。</span><span class="sxs-lookup"><span data-stu-id="76787-134">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="76787-135">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="76787-135">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76787-136">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="76787-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="76787-137">傳回緩衝區，其中包含在編譯期間遇到的錯誤和警告清單。</span><span class="sxs-lookup"><span data-stu-id="76787-137">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="76787-138">這些是偵錯工具在偵測模式中執行時所顯示的相同訊息。</span><span class="sxs-lookup"><span data-stu-id="76787-138">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="76787-139">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="76787-139">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="76787-140">*ppConstantTable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="76787-140">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76787-141">類型： **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="76787-141">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="76787-142">傳回 [**ID3DXConstantTable**](id3dxconstanttable.md) 介面，這個介面可以用來存取著色器常數。</span><span class="sxs-lookup"><span data-stu-id="76787-142">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="76787-143">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="76787-143">This value can be **NULL**.</span></span> <span data-ttu-id="76787-144">如果您將應用程式編譯為大型位址感知 (也就是說，您可以使用/LARGEADDRESSAWARE 連結器選項來處理大於 2 GB 的位址) ，您無法使用此參數，而且必須將它設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="76787-144">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="76787-145">相反地，您必須使用 [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) 函式來取出內嵌于著色器中的著色器常數資料表。</span><span class="sxs-lookup"><span data-stu-id="76787-145">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="76787-146">在這個 **D3DXGetShaderConstantTableEx** 呼叫中，您必須將 **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** 旗標傳遞給 *Flags* 參數，以指定最多可存取 4 GB 的虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="76787-146">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76787-147">傳回值</span><span class="sxs-lookup"><span data-stu-id="76787-147">Return value</span></span>

<span data-ttu-id="76787-148">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="76787-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="76787-149">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="76787-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="76787-150">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、e \_ >notimpl、e \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="76787-150">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_NOTIMPL, E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="76787-151">\_如果您要使用1.1 著色器 (vs \_ 1 \_ 1 和 ps \_ 1 \_ 1) ，則會傳回 E >notimpl。</span><span class="sxs-lookup"><span data-stu-id="76787-151">E\_NOTIMPL is returned if you're using 1.1 shaders (vs\_1\_1 and ps\_1\_1).</span></span>

## <a name="requirements"></a><span data-ttu-id="76787-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="76787-152">Requirements</span></span>



| <span data-ttu-id="76787-153">需求</span><span class="sxs-lookup"><span data-stu-id="76787-153">Requirement</span></span> | <span data-ttu-id="76787-154">值</span><span class="sxs-lookup"><span data-stu-id="76787-154">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76787-155">標頭</span><span class="sxs-lookup"><span data-stu-id="76787-155">Header</span></span><br/>  | <dl> <span data-ttu-id="76787-156"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="76787-156"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="76787-157">程式庫</span><span class="sxs-lookup"><span data-stu-id="76787-157">Library</span></span><br/> | <dl> <span data-ttu-id="76787-158"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="76787-158"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="76787-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76787-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76787-160">著色器函式</span><span class="sxs-lookup"><span data-stu-id="76787-160">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="76787-161">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="76787-161">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="76787-162">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="76787-162">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
