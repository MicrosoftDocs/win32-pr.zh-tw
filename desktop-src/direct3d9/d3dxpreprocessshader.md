---
description: 在不執行編譯的情況下，進行著色器的前置。 這會解析所有的 \# 定義和 \# 包含，提供適用于後續編譯的獨立著色器。
ms.assetid: d91258ed-6206-487a-aa81-e7c2bcea21ea
title: 'D3DXPreprocessShader 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 042cebe4e678ac1715a37ec3425ec0f21561797c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514561"
---
# <a name="d3dxpreprocessshader-function"></a><span data-ttu-id="1da38-104">D3DXPreprocessShader 函式</span><span class="sxs-lookup"><span data-stu-id="1da38-104">D3DXPreprocessShader function</span></span>

<span data-ttu-id="1da38-105">在不執行編譯的情況下，進行著色器的前置。</span><span class="sxs-lookup"><span data-stu-id="1da38-105">Preprocesses a shader without performing compilation.</span></span> <span data-ttu-id="1da38-106">這會解析所有的 \# 定義和 \# 包含，提供適用于後續編譯的獨立著色器。</span><span class="sxs-lookup"><span data-stu-id="1da38-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="1da38-107">我們建議您不要使用此舊版函式，而是使用 [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API。</span><span class="sxs-lookup"><span data-stu-id="1da38-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1da38-108">語法</span><span class="sxs-lookup"><span data-stu-id="1da38-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShader(
  _In_        LPCSTR        pSrcData,
  _In_        UINT          SrcDataSize,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="1da38-109">參數</span><span class="sxs-lookup"><span data-stu-id="1da38-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1da38-110">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1da38-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1da38-111">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1da38-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1da38-112">包含著色器之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="1da38-112">Pointer to a string that contains the shader.</span></span>

</dd> <dt>

<span data-ttu-id="1da38-113">*SrcDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1da38-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1da38-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1da38-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1da38-115">資料的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1da38-115">Length of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1da38-116">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1da38-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1da38-117">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="1da38-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="1da38-118">[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列。</span><span class="sxs-lookup"><span data-stu-id="1da38-118">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="1da38-119">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1da38-119">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1da38-120">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1da38-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1da38-121">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="1da38-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="1da38-122">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="1da38-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="1da38-123">如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="1da38-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="1da38-124">*ppShaderText* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1da38-124">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1da38-125">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1da38-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1da38-126">傳回包含單一大型字串的緩衝區，代表產生的格式化權杖資料流程。</span><span class="sxs-lookup"><span data-stu-id="1da38-126">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="1da38-127">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1da38-127">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1da38-128">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1da38-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1da38-129">傳回緩衝區，其中包含在編譯期間遇到的錯誤和警告清單。</span><span class="sxs-lookup"><span data-stu-id="1da38-129">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="1da38-130">這些是偵錯工具在偵測模式中執行時所顯示的相同訊息。</span><span class="sxs-lookup"><span data-stu-id="1da38-130">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="1da38-131">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1da38-131">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1da38-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="1da38-132">Return value</span></span>

<span data-ttu-id="1da38-133">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1da38-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1da38-134">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="1da38-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1da38-135">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="1da38-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1da38-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="1da38-136">Requirements</span></span>



| <span data-ttu-id="1da38-137">需求</span><span class="sxs-lookup"><span data-stu-id="1da38-137">Requirement</span></span> | <span data-ttu-id="1da38-138">值</span><span class="sxs-lookup"><span data-stu-id="1da38-138">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1da38-139">標頭</span><span class="sxs-lookup"><span data-stu-id="1da38-139">Header</span></span><br/>  | <dl> <span data-ttu-id="1da38-140"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="1da38-140"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1da38-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="1da38-141">Library</span></span><br/> | <dl> <span data-ttu-id="1da38-142"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1da38-142"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1da38-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1da38-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1da38-144">著色器函式</span><span class="sxs-lookup"><span data-stu-id="1da38-144">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="1da38-145">**D3DXPreprocessShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="1da38-145">**D3DXPreprocessShaderFromFile**</span></span>](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="1da38-146">**D3DXPreprocessShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="1da38-146">**D3DXPreprocessShaderFromResource**</span></span>](d3dxpreprocessshaderfromresource.md)
</dt> </dl>

 

 
