---
description: 組合著色器。
ms.assetid: a0d31b15-db79-4aa8-afd8-fa1e20c61725
title: 'D3DXAssembleShaderFromResource 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e748764eec94ea1f555c225c34680392610c9f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982045"
---
# <a name="d3dxassembleshaderfromresource-function"></a><span data-ttu-id="464d8-103">D3DXAssembleShaderFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="464d8-103">D3DXAssembleShaderFromResource function</span></span>

<span data-ttu-id="464d8-104">組合著色器。</span><span class="sxs-lookup"><span data-stu-id="464d8-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="464d8-105">語法</span><span class="sxs-lookup"><span data-stu-id="464d8-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCTSTR       pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="464d8-106">參數</span><span class="sxs-lookup"><span data-stu-id="464d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="464d8-107">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="464d8-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="464d8-108">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="464d8-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="464d8-109">包含效果描述之模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="464d8-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="464d8-110">如果這個參數為 **Null**，則會使用目前的模組。</span><span class="sxs-lookup"><span data-stu-id="464d8-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="464d8-111">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="464d8-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="464d8-112">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="464d8-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="464d8-113">指定資源名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="464d8-113">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="464d8-114">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="464d8-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="464d8-115">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="464d8-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="464d8-116">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="464d8-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="464d8-117">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="464d8-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="464d8-118">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="464d8-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="464d8-119">[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列。</span><span class="sxs-lookup"><span data-stu-id="464d8-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="464d8-120">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="464d8-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="464d8-121">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="464d8-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="464d8-122">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="464d8-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="464d8-123">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="464d8-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="464d8-124">如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="464d8-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="464d8-125">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="464d8-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="464d8-126">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="464d8-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="464d8-127">不同旗標所識別的編譯選項。</span><span class="sxs-lookup"><span data-stu-id="464d8-127">Compile options identified by various flags.</span></span> <span data-ttu-id="464d8-128">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="464d8-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="464d8-129">如需詳細資料，請參閱 [D3DXSHADER 旗標](d3dxshader-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="464d8-129">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="464d8-130">*ppShader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="464d8-130">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="464d8-131">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="464d8-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="464d8-132">傳回包含已建立之著色器的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="464d8-132">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="464d8-133">這個緩衝區包含已編譯的著色器程式碼，以及任何內嵌的 debug 和 symbol 資料表資訊。</span><span class="sxs-lookup"><span data-stu-id="464d8-133">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="464d8-134">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="464d8-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="464d8-135">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="464d8-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="464d8-136">傳回緩衝區，其中包含在編譯期間遇到的錯誤和警告清單。</span><span class="sxs-lookup"><span data-stu-id="464d8-136">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="464d8-137">這些是偵錯工具在偵測模式中執行時所顯示的相同訊息。</span><span class="sxs-lookup"><span data-stu-id="464d8-137">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="464d8-138">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="464d8-138">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="464d8-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="464d8-139">Return value</span></span>

<span data-ttu-id="464d8-140">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="464d8-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="464d8-141">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="464d8-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="464d8-142">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="464d8-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="464d8-143">備註</span><span class="sxs-lookup"><span data-stu-id="464d8-143">Remarks</span></span>

<span data-ttu-id="464d8-144">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="464d8-144">The compiler setting also determines the function version.</span></span> <span data-ttu-id="464d8-145">如果已定義 Unicode，函式呼叫會解析為 D3DXAssembleShaderFromResourceW。</span><span class="sxs-lookup"><span data-stu-id="464d8-145">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromResourceW.</span></span> <span data-ttu-id="464d8-146">否則，函式呼叫會解析為 D3DXAssembleShaderFromResourceA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="464d8-146">Otherwise, the function call resolves to D3DXAssembleShaderFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="464d8-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="464d8-147">Requirements</span></span>



| <span data-ttu-id="464d8-148">需求</span><span class="sxs-lookup"><span data-stu-id="464d8-148">Requirement</span></span> | <span data-ttu-id="464d8-149">值</span><span class="sxs-lookup"><span data-stu-id="464d8-149">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="464d8-150">標頭</span><span class="sxs-lookup"><span data-stu-id="464d8-150">Header</span></span><br/>  | <dl> <span data-ttu-id="464d8-151"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="464d8-151"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="464d8-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="464d8-152">Library</span></span><br/> | <dl> <span data-ttu-id="464d8-153"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="464d8-153"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="464d8-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="464d8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="464d8-155">著色器函式</span><span class="sxs-lookup"><span data-stu-id="464d8-155">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="464d8-156">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="464d8-156">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="464d8-157">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="464d8-157">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
