---
description: D3DXAssembleShader 函式-組合著色器。
ms.assetid: 24c3dcae-9397-4856-b072-0ae340157bf9
title: 'D3DXAssembleShader 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 891281ebc3db970ca61132fe49ba98531ca1d879
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116046"
---
# <a name="d3dxassembleshader-function"></a><span data-ttu-id="4e7c8-103">D3DXAssembleShader 函式</span><span class="sxs-lookup"><span data-stu-id="4e7c8-103">D3DXAssembleShader function</span></span>

<span data-ttu-id="4e7c8-104">組合著色器。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e7c8-105">語法</span><span class="sxs-lookup"><span data-stu-id="4e7c8-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShader(
  _In_        LPCSTR        pSrcData,
  _In_        UINT          SrcDataLen,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="4e7c8-106">參數</span><span class="sxs-lookup"><span data-stu-id="4e7c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e7c8-107">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e7c8-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7c8-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e7c8-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e7c8-109">包含著色器資料之記憶體緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-109">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="4e7c8-110">*SrcDataLen* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e7c8-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7c8-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e7c8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e7c8-112">效果資料的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-112">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4e7c8-113">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e7c8-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7c8-114">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="4e7c8-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="4e7c8-115">[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="4e7c8-116">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4e7c8-117">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e7c8-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7c8-118">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="4e7c8-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="4e7c8-119">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="4e7c8-120">如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="4e7c8-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="4e7c8-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7c8-122">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e7c8-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e7c8-123">不同旗標所識別的編譯選項。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-123">Compile options identified by various flags.</span></span> <span data-ttu-id="4e7c8-124">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="4e7c8-125">如需詳細資料，請參閱 [D3DXSHADER 旗標](d3dxshader-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="4e7c8-126">*ppShader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4e7c8-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7c8-127">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e7c8-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="4e7c8-128">傳回包含已建立之著色器的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="4e7c8-129">這個緩衝區包含已編譯的著色器程式碼，以及任何內嵌的 debug 和 symbol 資料表資訊。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="4e7c8-130">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4e7c8-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7c8-131">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e7c8-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="4e7c8-132">傳回緩衝區，其中包含在編譯期間遇到的錯誤和警告清單。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="4e7c8-133">這些是偵錯工具在偵測模式中執行時所顯示的相同訊息。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="4e7c8-134">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e7c8-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e7c8-135">Return value</span></span>

<span data-ttu-id="4e7c8-136">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4e7c8-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4e7c8-137">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4e7c8-138">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="4e7c8-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e7c8-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e7c8-139">Requirements</span></span>



| <span data-ttu-id="4e7c8-140">需求</span><span class="sxs-lookup"><span data-stu-id="4e7c8-140">Requirement</span></span> | <span data-ttu-id="4e7c8-141">值</span><span class="sxs-lookup"><span data-stu-id="4e7c8-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e7c8-142">標頭</span><span class="sxs-lookup"><span data-stu-id="4e7c8-142">Header</span></span><br/>  | <dl> <span data-ttu-id="4e7c8-143"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="4e7c8-143"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="4e7c8-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="4e7c8-144">Library</span></span><br/> | <dl> <span data-ttu-id="4e7c8-145"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e7c8-145"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4e7c8-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e7c8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e7c8-147">著色器函式</span><span class="sxs-lookup"><span data-stu-id="4e7c8-147">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="4e7c8-148">**D3DXAssembleShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="4e7c8-148">**D3DXAssembleShaderFromFile**</span></span>](d3dxassembleshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="4e7c8-149">**D3DXAssembleShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="4e7c8-149">**D3DXAssembleShaderFromResource**</span></span>](d3dxassembleshaderfromresource.md)
</dt> </dl>

 

 
