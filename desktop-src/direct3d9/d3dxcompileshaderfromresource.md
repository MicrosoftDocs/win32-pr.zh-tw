---
description: D3DXCompileShaderFromResource 函式-編譯著色器檔。
ms.assetid: e944ae61-0c27-4795-8381-0ec9b3d8c3f4
title: 'D3DXCompileShaderFromResource 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de94754004cc42bcc6914d9513588a71a1a593dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115806"
---
# <a name="d3dxcompileshaderfromresource-function"></a><span data-ttu-id="fe951-103">D3DXCompileShaderFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="fe951-103">D3DXCompileShaderFromResource function</span></span>

<span data-ttu-id="fe951-104">編譯著色器檔。</span><span class="sxs-lookup"><span data-stu-id="fe951-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="fe951-105">我們建議您不要使用此舊版函式，而是使用 Fxc.exe 命令列編譯器或使用 [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API，以離線方式編譯。</span><span class="sxs-lookup"><span data-stu-id="fe951-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fe951-106">語法</span><span class="sxs-lookup"><span data-stu-id="fe951-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShaderFromResource(
  _In_        HMODULE             hSrcModule,
  _In_        LPCSTR              pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="fe951-107">參數</span><span class="sxs-lookup"><span data-stu-id="fe951-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe951-108">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe951-108">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe951-109">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe951-109">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe951-110">包含效果描述之模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fe951-110">Handle to a module containing the effect description.</span></span> <span data-ttu-id="fe951-111">如果這個參數為 **Null**，則會使用目前的模組。</span><span class="sxs-lookup"><span data-stu-id="fe951-111">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="fe951-112">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe951-112">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe951-113">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe951-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe951-114">指定資源名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="fe951-114">Pointer to a string that specifies the resource name.</span></span>

</dd> <dt>

<span data-ttu-id="fe951-115">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe951-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe951-116">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe951-116">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="fe951-117">[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列。</span><span class="sxs-lookup"><span data-stu-id="fe951-117">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="fe951-118">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fe951-118">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fe951-119">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe951-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe951-120">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="fe951-120">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="fe951-121">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="fe951-121">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="fe951-122">如果這個值為 **Null**，就會在從檔案進行 \# 編譯時接受包含，或從資源或記憶體編譯時，就會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="fe951-122">If this value is **NULL**, \#includes will either be honored when compiling from a file, or will error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="fe951-123">*pFunctionName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe951-123">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe951-124">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe951-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe951-125">著色器進入點函式的指標，該函式會開始執行。</span><span class="sxs-lookup"><span data-stu-id="fe951-125">Pointer to the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="fe951-126">*pProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe951-126">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe951-127">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe951-127">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe951-128">著色器設定檔的指標，此設定檔可決定著色器指令集。</span><span class="sxs-lookup"><span data-stu-id="fe951-128">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="fe951-129">如需可用的配置檔案清單，請參閱 [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) 或 [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) 。</span><span class="sxs-lookup"><span data-stu-id="fe951-129">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="fe951-130">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="fe951-130">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe951-131">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe951-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe951-132">不同旗標所識別的編譯選項。</span><span class="sxs-lookup"><span data-stu-id="fe951-132">Compile options identified by various flags.</span></span> <span data-ttu-id="fe951-133">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="fe951-133">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="fe951-134">如需詳細資料，請參閱 [D3DXSHADER 旗標](d3dxshader-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="fe951-134">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="fe951-135">*ppShader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe951-135">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe951-136">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe951-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="fe951-137">傳回包含已建立之著色器的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="fe951-137">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="fe951-138">這個緩衝區包含已編譯的著色器程式碼，以及任何內嵌的 debug 和 symbol 資料表資訊。</span><span class="sxs-lookup"><span data-stu-id="fe951-138">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="fe951-139">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe951-139">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe951-140">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe951-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="fe951-141">傳回緩衝區，其中包含在編譯期間遇到的錯誤和警告清單。</span><span class="sxs-lookup"><span data-stu-id="fe951-141">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="fe951-142">這些是偵錯工具在偵測模式中執行時所顯示的相同訊息。</span><span class="sxs-lookup"><span data-stu-id="fe951-142">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="fe951-143">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fe951-143">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fe951-144">*ppConstantTable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe951-144">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe951-145">類型： **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe951-145">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="fe951-146">傳回 [**ID3DXConstantTable**](id3dxconstanttable.md) 介面，這個介面可以用來存取著色器常數。</span><span class="sxs-lookup"><span data-stu-id="fe951-146">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="fe951-147">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fe951-147">This value can be **NULL**.</span></span> <span data-ttu-id="fe951-148">如果您將應用程式編譯為大型位址感知 (也就是說，您可以使用/LARGEADDRESSAWARE 連結器選項來處理大於 2 GB 的位址) ，您無法使用此參數，而且必須將它設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="fe951-148">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="fe951-149">相反地，您必須使用 [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) 函式來取出內嵌于著色器中的著色器常數資料表。</span><span class="sxs-lookup"><span data-stu-id="fe951-149">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="fe951-150">在這個 **D3DXGetShaderConstantTableEx** 呼叫中，您必須將 **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** 旗標傳遞給 *Flags* 參數，以指定最多可存取 4 GB 的虛擬位址空間。</span><span class="sxs-lookup"><span data-stu-id="fe951-150">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe951-151">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe951-151">Return value</span></span>

<span data-ttu-id="fe951-152">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe951-152">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe951-153">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="fe951-153">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fe951-154">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="fe951-154">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe951-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe951-155">Requirements</span></span>



| <span data-ttu-id="fe951-156">需求</span><span class="sxs-lookup"><span data-stu-id="fe951-156">Requirement</span></span> | <span data-ttu-id="fe951-157">值</span><span class="sxs-lookup"><span data-stu-id="fe951-157">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe951-158">標頭</span><span class="sxs-lookup"><span data-stu-id="fe951-158">Header</span></span><br/>  | <dl> <span data-ttu-id="fe951-159"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe951-159"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fe951-160">程式庫</span><span class="sxs-lookup"><span data-stu-id="fe951-160">Library</span></span><br/> | <dl> <span data-ttu-id="fe951-161"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe951-161"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fe951-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe951-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe951-163">著色器函式</span><span class="sxs-lookup"><span data-stu-id="fe951-163">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="fe951-164">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="fe951-164">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="fe951-165">**D3DXCompileShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="fe951-165">**D3DXCompileShaderFromFile**</span></span>](d3dxcompileshaderfromfile.md)
</dt> </dl>

 

 
