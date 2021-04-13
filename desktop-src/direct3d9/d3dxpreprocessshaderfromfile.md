---
description: 在不執行編譯的情況下，將著色器檔案進行前置檔 這會解析所有的 \# 定義和 \# 包含，提供適用于後續編譯的獨立著色器。
ms.assetid: 1be68cc0-b4a3-41b4-b956-b96ed439be9e
title: 'D3DXPreprocessShaderFromFile 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba9cf35418bbbe6fe4b39341031fd1e056b27dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322888"
---
# <a name="d3dxpreprocessshaderfromfile-function"></a><span data-ttu-id="0dc6f-104">D3DXPreprocessShaderFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="0dc6f-104">D3DXPreprocessShaderFromFile function</span></span>

<span data-ttu-id="0dc6f-105">在不執行編譯的情況下，將著色器檔案進行前置檔</span><span class="sxs-lookup"><span data-stu-id="0dc6f-105">Preprocesses a shader file without performing compilation.</span></span> <span data-ttu-id="0dc6f-106">這會解析所有的 \# 定義和 \# 包含，提供適用于後續編譯的獨立著色器。</span><span class="sxs-lookup"><span data-stu-id="0dc6f-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="0dc6f-107">我們建議您不要使用此舊版函式，而是使用 [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API。</span><span class="sxs-lookup"><span data-stu-id="0dc6f-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0dc6f-108">語法</span><span class="sxs-lookup"><span data-stu-id="0dc6f-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShaderFromFile(
  _In_        LPCSTR        pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="0dc6f-109">參數</span><span class="sxs-lookup"><span data-stu-id="0dc6f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dc6f-110">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0dc6f-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc6f-111">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0dc6f-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0dc6f-112">指定著色器檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="0dc6f-112">Pointer to a string that specifies the filename of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="0dc6f-113">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0dc6f-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc6f-114">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="0dc6f-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="0dc6f-115">[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列。</span><span class="sxs-lookup"><span data-stu-id="0dc6f-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="0dc6f-116">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0dc6f-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0dc6f-117">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0dc6f-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc6f-118">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="0dc6f-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="0dc6f-119">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="0dc6f-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="0dc6f-120">如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="0dc6f-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="0dc6f-121">*ppShaderText* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0dc6f-121">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc6f-122">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0dc6f-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0dc6f-123">傳回包含單一大型字串的緩衝區，代表產生的格式化權杖資料流程。</span><span class="sxs-lookup"><span data-stu-id="0dc6f-123">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="0dc6f-124">*ppErrorMsgs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0dc6f-124">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc6f-125">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0dc6f-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0dc6f-126">傳回緩衝區，其中包含在編譯期間遇到的錯誤和警告清單。</span><span class="sxs-lookup"><span data-stu-id="0dc6f-126">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="0dc6f-127">這些是偵錯工具在偵測模式中執行時所顯示的相同訊息。</span><span class="sxs-lookup"><span data-stu-id="0dc6f-127">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="0dc6f-128">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0dc6f-128">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dc6f-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="0dc6f-129">Return value</span></span>

<span data-ttu-id="0dc6f-130">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0dc6f-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0dc6f-131">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="0dc6f-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0dc6f-132">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="0dc6f-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dc6f-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="0dc6f-133">Requirements</span></span>



| <span data-ttu-id="0dc6f-134">需求</span><span class="sxs-lookup"><span data-stu-id="0dc6f-134">Requirement</span></span> | <span data-ttu-id="0dc6f-135">值</span><span class="sxs-lookup"><span data-stu-id="0dc6f-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc6f-136">標頭</span><span class="sxs-lookup"><span data-stu-id="0dc6f-136">Header</span></span><br/>  | <dl> <span data-ttu-id="0dc6f-137"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="0dc6f-137"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0dc6f-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="0dc6f-138">Library</span></span><br/> | <dl> <span data-ttu-id="0dc6f-139"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0dc6f-139"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0dc6f-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0dc6f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dc6f-141">著色器函式</span><span class="sxs-lookup"><span data-stu-id="0dc6f-141">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="0dc6f-142">**D3DXPreprocessShader**</span><span class="sxs-lookup"><span data-stu-id="0dc6f-142">**D3DXPreprocessShader**</span></span>](d3dxpreprocessshader.md)
</dt> <dt>

[<span data-ttu-id="0dc6f-143">**D3DXPreprocessShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="0dc6f-143">**D3DXPreprocessShaderFromResource**</span></span>](d3dxpreprocessshaderfromresource.md)
</dt> </dl>

 

 
