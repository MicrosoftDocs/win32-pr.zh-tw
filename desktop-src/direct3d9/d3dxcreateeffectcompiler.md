---
description: D3DXCreateEffectCompiler 函式-從 ASCII 效果描述建立效果編譯器。
ms.assetid: 96e883f4-4055-4b8b-940a-164bbf893af4
title: 'D3DXCreateEffectCompiler 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompiler
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 38ab58ed15609d468d25f4406353448e4fd6adb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115766"
---
# <a name="d3dxcreateeffectcompiler-function"></a><span data-ttu-id="b7d99-103">D3DXCreateEffectCompiler 函式</span><span class="sxs-lookup"><span data-stu-id="b7d99-103">D3DXCreateEffectCompiler function</span></span>

<span data-ttu-id="b7d99-104">從 ASCII 效果描述建立效果編譯器。</span><span class="sxs-lookup"><span data-stu-id="b7d99-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d99-105">語法</span><span class="sxs-lookup"><span data-stu-id="b7d99-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompiler(
  _In_        LPCSTR               pSrcData,
  _In_        UINT                 SrcDataLen,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="b7d99-106">參數</span><span class="sxs-lookup"><span data-stu-id="b7d99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7d99-107">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7d99-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d99-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7d99-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7d99-109">包含效果描述之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="b7d99-109">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="b7d99-110">*SrcDataLen* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7d99-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d99-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7d99-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7d99-112">效果資料的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b7d99-112">Length, in bytes, of the effect data.</span></span>

</dd> <dt>

<span data-ttu-id="b7d99-113">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7d99-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d99-114">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="b7d99-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="b7d99-115">[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列，描述預處理器定義。</span><span class="sxs-lookup"><span data-stu-id="b7d99-115">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="b7d99-116">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b7d99-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b7d99-117">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7d99-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d99-118">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="b7d99-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="b7d99-119">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="b7d99-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="b7d99-120">如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7d99-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="b7d99-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b7d99-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d99-122">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7d99-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7d99-123">不同旗標所識別的編譯選項 (參閱 [D3DXSHADER 旗標](d3dxshader-flags.md)) 。</span><span class="sxs-lookup"><span data-stu-id="b7d99-123">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="b7d99-124">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="b7d99-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="b7d99-125">請參閱 [效果-編譯器工具](../direct3dtools/fxc.md) 以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b7d99-125">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="b7d99-126">*ppEffectCompiler* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b7d99-126">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d99-127">類型： **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="b7d99-127">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="b7d99-128">包含效果編譯器之 [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) 介面的指標位址。</span><span class="sxs-lookup"><span data-stu-id="b7d99-128">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="b7d99-129">*ppParseErrors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b7d99-129">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d99-130">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b7d99-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b7d99-131">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址，其中包含在編譯期間發生的任何錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="b7d99-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="b7d99-132">這個參數可以設定為 **Null** ，以忽略錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="b7d99-132">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7d99-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7d99-133">Return value</span></span>

<span data-ttu-id="b7d99-134">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7d99-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7d99-135">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="b7d99-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b7d99-136">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="b7d99-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d99-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7d99-137">Requirements</span></span>



| <span data-ttu-id="b7d99-138">需求</span><span class="sxs-lookup"><span data-stu-id="b7d99-138">Requirement</span></span> | <span data-ttu-id="b7d99-139">值</span><span class="sxs-lookup"><span data-stu-id="b7d99-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d99-140">標頭</span><span class="sxs-lookup"><span data-stu-id="b7d99-140">Header</span></span><br/>  | <dl> <span data-ttu-id="b7d99-141"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7d99-141"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b7d99-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="b7d99-142">Library</span></span><br/> | <dl> <span data-ttu-id="b7d99-143"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7d99-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b7d99-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7d99-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d99-145">效果函數</span><span class="sxs-lookup"><span data-stu-id="b7d99-145">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="b7d99-146">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="b7d99-146">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="b7d99-147">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="b7d99-147">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
