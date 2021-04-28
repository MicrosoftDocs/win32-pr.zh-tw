---
description: D3DXAssembleShaderFromFile 函式-組合著色器。
ms.assetid: 2977b64a-b8cc-454b-8e28-291f6f2c6fc1
title: 'D3DXAssembleShaderFromFile 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91aaf2924638b1db5b0e8ec0782b90fa964a9543
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116026"
---
# <a name="d3dxassembleshaderfromfile-function"></a><span data-ttu-id="ed75a-103">D3DXAssembleShaderFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="ed75a-103">D3DXAssembleShaderFromFile function</span></span>

<span data-ttu-id="ed75a-104">組合著色器。</span><span class="sxs-lookup"><span data-stu-id="ed75a-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed75a-105">語法</span><span class="sxs-lookup"><span data-stu-id="ed75a-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShaderFromFile(
  _In_        LPCTSTR       pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="ed75a-106">參數</span><span class="sxs-lookup"><span data-stu-id="ed75a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed75a-107">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ed75a-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed75a-108">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed75a-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed75a-109">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="ed75a-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="ed75a-110">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="ed75a-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ed75a-111">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="ed75a-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="ed75a-112">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="ed75a-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ed75a-113">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ed75a-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed75a-114">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="ed75a-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="ed75a-115">[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列。</span><span class="sxs-lookup"><span data-stu-id="ed75a-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="ed75a-116">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ed75a-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ed75a-117">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ed75a-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed75a-118">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="ed75a-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="ed75a-119">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="ed75a-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="ed75a-120">如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="ed75a-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="ed75a-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="ed75a-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed75a-122">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed75a-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed75a-123">不同旗標所識別的編譯選項。</span><span class="sxs-lookup"><span data-stu-id="ed75a-123">Compile options identified by various flags.</span></span> <span data-ttu-id="ed75a-124">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="ed75a-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="ed75a-125">如需詳細資料，請參閱 [D3DXSHADER 旗標](d3dxshader-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="ed75a-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="ed75a-126">*ppShader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ed75a-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed75a-127">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed75a-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ed75a-128">傳回包含已建立之著色器的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="ed75a-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="ed75a-129">這個緩衝區包含已編譯的著色器程式碼，以及任何內嵌的 debug 和 symbol 資料表資訊。</span><span class="sxs-lookup"><span data-stu-id="ed75a-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="ed75a-130">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ed75a-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed75a-131">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ed75a-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ed75a-132">傳回緩衝區，其中包含在編譯期間遇到的錯誤和警告清單。</span><span class="sxs-lookup"><span data-stu-id="ed75a-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="ed75a-133">這些是偵錯工具在偵測模式中執行時所顯示的相同訊息。</span><span class="sxs-lookup"><span data-stu-id="ed75a-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="ed75a-134">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ed75a-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed75a-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed75a-135">Return value</span></span>

<span data-ttu-id="ed75a-136">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed75a-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed75a-137">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="ed75a-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ed75a-138">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="ed75a-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed75a-139">備註</span><span class="sxs-lookup"><span data-stu-id="ed75a-139">Remarks</span></span>

<span data-ttu-id="ed75a-140">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="ed75a-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ed75a-141">如果已定義 Unicode，函式呼叫會解析為 D3DXAssembleShaderFromFileW。</span><span class="sxs-lookup"><span data-stu-id="ed75a-141">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromFileW.</span></span> <span data-ttu-id="ed75a-142">否則，函式呼叫會解析為 D3DXAssembleShaderFromFileA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="ed75a-142">Otherwise, the function call resolves to D3DXAssembleShaderFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed75a-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed75a-143">Requirements</span></span>



| <span data-ttu-id="ed75a-144">需求</span><span class="sxs-lookup"><span data-stu-id="ed75a-144">Requirement</span></span> | <span data-ttu-id="ed75a-145">值</span><span class="sxs-lookup"><span data-stu-id="ed75a-145">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed75a-146">標頭</span><span class="sxs-lookup"><span data-stu-id="ed75a-146">Header</span></span><br/>  | <dl> <span data-ttu-id="ed75a-147"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="ed75a-147"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ed75a-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="ed75a-148">Library</span></span><br/> | <dl> <span data-ttu-id="ed75a-149"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed75a-149"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ed75a-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed75a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed75a-151">著色器函式</span><span class="sxs-lookup"><span data-stu-id="ed75a-151">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="ed75a-152">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="ed75a-152">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="ed75a-153">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="ed75a-153">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
