---
description: 在不執行編譯的情況下，預處理著色器資源。 這會解析所有的 \# 定義和 \# 包含，提供適用于後續編譯的獨立著色器。
ms.assetid: a00c2db9-d7ba-48ab-80e3-dc20774e1b1e
title: 'D3DXPreprocessShaderFromResource 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c45073d0b84ef6fb33d378c4c18f862f55c6b84a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322839"
---
# <a name="d3dxpreprocessshaderfromresource-function"></a><span data-ttu-id="9722c-104">D3DXPreprocessShaderFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="9722c-104">D3DXPreprocessShaderFromResource function</span></span>

<span data-ttu-id="9722c-105">在不執行編譯的情況下，預處理著色器資源。</span><span class="sxs-lookup"><span data-stu-id="9722c-105">Preprocesses a shader resource without performing compilation.</span></span> <span data-ttu-id="9722c-106">這會解析所有的 \# 定義和 \# 包含，提供適用于後續編譯的獨立著色器。</span><span class="sxs-lookup"><span data-stu-id="9722c-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="9722c-107">我們建議您不要使用此舊版函式，而是使用 [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API。</span><span class="sxs-lookup"><span data-stu-id="9722c-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9722c-108">語法</span><span class="sxs-lookup"><span data-stu-id="9722c-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCSTR        pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="9722c-109">參數</span><span class="sxs-lookup"><span data-stu-id="9722c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9722c-110">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9722c-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9722c-111">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9722c-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9722c-112">保存著色器資源之模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="9722c-112">Handle to the module that holds the shader resource.</span></span> <span data-ttu-id="9722c-113">如果這個值為 **Null**，則會使用目前的模組。</span><span class="sxs-lookup"><span data-stu-id="9722c-113">If this value is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="9722c-114">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9722c-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9722c-115">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9722c-115">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9722c-116">代表模組中資源名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="9722c-116">String that represents the name of the resource in the module.</span></span>

</dd> <dt>

<span data-ttu-id="9722c-117">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9722c-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9722c-118">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="9722c-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="9722c-119">[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列。</span><span class="sxs-lookup"><span data-stu-id="9722c-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="9722c-120">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9722c-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9722c-121">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9722c-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9722c-122">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="9722c-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="9722c-123">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="9722c-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="9722c-124">如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="9722c-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="9722c-125">*ppShaderText* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9722c-125">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9722c-126">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9722c-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9722c-127">傳回包含單一大型字串的緩衝區，代表產生的格式化權杖資料流程。</span><span class="sxs-lookup"><span data-stu-id="9722c-127">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="9722c-128">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9722c-128">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9722c-129">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9722c-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9722c-130">傳回緩衝區，其中包含在編譯期間遇到的錯誤和警告清單。</span><span class="sxs-lookup"><span data-stu-id="9722c-130">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="9722c-131">這些是偵錯工具在偵測模式中執行時所顯示的相同訊息。</span><span class="sxs-lookup"><span data-stu-id="9722c-131">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="9722c-132">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9722c-132">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9722c-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="9722c-133">Return value</span></span>

<span data-ttu-id="9722c-134">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9722c-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9722c-135">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="9722c-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9722c-136">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="9722c-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="9722c-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="9722c-137">Requirements</span></span>



| <span data-ttu-id="9722c-138">需求</span><span class="sxs-lookup"><span data-stu-id="9722c-138">Requirement</span></span> | <span data-ttu-id="9722c-139">值</span><span class="sxs-lookup"><span data-stu-id="9722c-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9722c-140">標頭</span><span class="sxs-lookup"><span data-stu-id="9722c-140">Header</span></span><br/>  | <dl> <span data-ttu-id="9722c-141"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="9722c-141"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9722c-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="9722c-142">Library</span></span><br/> | <dl> <span data-ttu-id="9722c-143"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9722c-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9722c-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9722c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9722c-145">著色器函式</span><span class="sxs-lookup"><span data-stu-id="9722c-145">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="9722c-146">**D3DXPreprocessShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="9722c-146">**D3DXPreprocessShaderFromFile**</span></span>](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="9722c-147">**D3DXPreprocessShader**</span><span class="sxs-lookup"><span data-stu-id="9722c-147">**D3DXPreprocessShader**</span></span>](d3dxpreprocessshader.md)
</dt> </dl>

 

 
