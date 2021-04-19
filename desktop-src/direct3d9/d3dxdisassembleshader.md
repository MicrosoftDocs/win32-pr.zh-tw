---
description: 將著色器拆解。
ms.assetid: 30159223-8f88-4929-8ef1-7a6acc13f485
title: 'D3DXDisassembleShader 函式 (D3DX9Shader) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6192b77c190ed73dc6e5038c9119152836eca375
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993882"
---
# <a name="d3dxdisassembleshader-function"></a><span data-ttu-id="3fb69-103">D3DXDisassembleShader 函式</span><span class="sxs-lookup"><span data-stu-id="3fb69-103">D3DXDisassembleShader function</span></span>

<span data-ttu-id="3fb69-104">將著色器拆解。</span><span class="sxs-lookup"><span data-stu-id="3fb69-104">Disassemble a shader.</span></span>

> [!Note]  
> <span data-ttu-id="3fb69-105">我們建議您不要使用此舊版函式，而是使用 [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API。</span><span class="sxs-lookup"><span data-stu-id="3fb69-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3fb69-106">語法</span><span class="sxs-lookup"><span data-stu-id="3fb69-106">Syntax</span></span>


```C++
HRESULT D3DXDisassembleShader(
  _In_  const DWORD        *pShader,
  _In_        BOOL         EnableColorCode,
  _In_        LPCSTR       pComments,
  _Out_       LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="3fb69-107">參數</span><span class="sxs-lookup"><span data-stu-id="3fb69-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fb69-108">*pShader* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3fb69-108">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb69-109">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="3fb69-109">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3fb69-110">包含著色器資料之記憶體緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="3fb69-110">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="3fb69-111">*EnableColorCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3fb69-111">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb69-112">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3fb69-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3fb69-113">啟用色彩代碼，讓您更容易閱讀反組解碼。</span><span class="sxs-lookup"><span data-stu-id="3fb69-113">Enable color code to make it easier to read the disassembly.</span></span>

</dd> <dt>

<span data-ttu-id="3fb69-114">*pComments* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3fb69-114">*pComments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb69-115">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3fb69-115">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3fb69-116">選擇性的 Null 終止批註字串。</span><span class="sxs-lookup"><span data-stu-id="3fb69-116">An optional NULL-terminated comment string.</span></span> <span data-ttu-id="3fb69-117">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3fb69-117">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3fb69-118">*ppDisassembly* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3fb69-118">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb69-119">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3fb69-119">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3fb69-120">傳回包含已拆解著色器的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3fb69-120">Returns a buffer containing the disassembled shader.</span></span> <span data-ttu-id="3fb69-121">請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="3fb69-121">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fb69-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="3fb69-122">Return value</span></span>

<span data-ttu-id="3fb69-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3fb69-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3fb69-124">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="3fb69-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3fb69-125">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="3fb69-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fb69-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fb69-126">Requirements</span></span>



| <span data-ttu-id="3fb69-127">需求</span><span class="sxs-lookup"><span data-stu-id="3fb69-127">Requirement</span></span> | <span data-ttu-id="3fb69-128">值</span><span class="sxs-lookup"><span data-stu-id="3fb69-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb69-129">標頭</span><span class="sxs-lookup"><span data-stu-id="3fb69-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3fb69-130"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="3fb69-130"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="3fb69-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="3fb69-131">Library</span></span><br/> | <dl> <span data-ttu-id="3fb69-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fb69-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3fb69-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3fb69-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb69-134">著色器函式</span><span class="sxs-lookup"><span data-stu-id="3fb69-134">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
