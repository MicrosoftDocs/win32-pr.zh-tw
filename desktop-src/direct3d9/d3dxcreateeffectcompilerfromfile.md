---
description: 從 ASCII 效果描述建立效果編譯器。
ms.assetid: 87438a1e-4149-42ef-aa7a-9f0549eb7982
title: 'D3DXCreateEffectCompilerFromFile 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fe27683078f77d7d444bd3a763fc326e749f7517
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988595"
---
# <a name="d3dxcreateeffectcompilerfromfile-function"></a><span data-ttu-id="a019f-103">D3DXCreateEffectCompilerFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="a019f-103">D3DXCreateEffectCompilerFromFile function</span></span>

<span data-ttu-id="a019f-104">從 ASCII 效果描述建立效果編譯器。</span><span class="sxs-lookup"><span data-stu-id="a019f-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a019f-105">語法</span><span class="sxs-lookup"><span data-stu-id="a019f-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompilerFromFile(
  _In_        LPCTSTR              pSrcFile,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="a019f-106">參數</span><span class="sxs-lookup"><span data-stu-id="a019f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a019f-107">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a019f-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a019f-108">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a019f-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a019f-109">檔案名的指標。</span><span class="sxs-lookup"><span data-stu-id="a019f-109">Pointer to the filename.</span></span> <span data-ttu-id="a019f-110">此參數支援 Unicode 和 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="a019f-110">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="a019f-111">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="a019f-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a019f-112">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a019f-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a019f-113">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="a019f-113">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="a019f-114">[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列，描述預處理器定義。</span><span class="sxs-lookup"><span data-stu-id="a019f-114">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="a019f-115">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a019f-115">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a019f-116">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a019f-116">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a019f-117">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="a019f-117">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="a019f-118">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="a019f-118">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="a019f-119">如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="a019f-119">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="a019f-120">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="a019f-120">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a019f-121">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a019f-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a019f-122">不同旗標所識別的編譯選項 (參閱 [D3DXSHADER 旗標](d3dxshader-flags.md)) 。</span><span class="sxs-lookup"><span data-stu-id="a019f-122">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="a019f-123">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="a019f-123">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="a019f-124">請參閱 [效果-編譯器工具](../direct3dtools/fxc.md) 以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a019f-124">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="a019f-125">*ppEffectCompiler* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a019f-125">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a019f-126">類型： **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="a019f-126">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="a019f-127">[**ID3DXEffectCompiler**](id3dxeffectcompiler.md)介面指標的位址，其中包含效果編譯器。</span><span class="sxs-lookup"><span data-stu-id="a019f-127">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="a019f-128">*ppParseErrors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a019f-128">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a019f-129">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a019f-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a019f-130">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址，其中包含在編譯期間發生的任何錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="a019f-130">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="a019f-131">這個參數可以設定為 **Null** ，以忽略錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="a019f-131">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a019f-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="a019f-132">Return value</span></span>

<span data-ttu-id="a019f-133">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a019f-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a019f-134">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="a019f-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a019f-135">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="a019f-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a019f-136">備註</span><span class="sxs-lookup"><span data-stu-id="a019f-136">Remarks</span></span>

<span data-ttu-id="a019f-137">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="a019f-137">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="a019f-138">否則，LPCTSTR 資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="a019f-138">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="a019f-139">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="a019f-139">The compiler setting also determines the function version.</span></span> <span data-ttu-id="a019f-140">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateEffectCompilerFromFileW。</span><span class="sxs-lookup"><span data-stu-id="a019f-140">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromFileW.</span></span> <span data-ttu-id="a019f-141">否則，函式呼叫會解析為 D3DXCreateEffectCompilerFromFileA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="a019f-141">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="a019f-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="a019f-142">Requirements</span></span>



| <span data-ttu-id="a019f-143">需求</span><span class="sxs-lookup"><span data-stu-id="a019f-143">Requirement</span></span> | <span data-ttu-id="a019f-144">值</span><span class="sxs-lookup"><span data-stu-id="a019f-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a019f-145">標頭</span><span class="sxs-lookup"><span data-stu-id="a019f-145">Header</span></span><br/>  | <dl> <span data-ttu-id="a019f-146"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="a019f-146"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="a019f-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="a019f-147">Library</span></span><br/> | <dl> <span data-ttu-id="a019f-148"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a019f-148"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a019f-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a019f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a019f-150">效果函數</span><span class="sxs-lookup"><span data-stu-id="a019f-150">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="a019f-151">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="a019f-151">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="a019f-152">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="a019f-152">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
