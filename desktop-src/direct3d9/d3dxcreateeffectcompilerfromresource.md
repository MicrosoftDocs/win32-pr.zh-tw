---
description: 從 ASCII 效果描述建立 ID3DXEffectCompiler。
ms.assetid: 041e0a3f-3dc6-4cc3-8380-d4a79a3f647a
title: 'D3DXCreateEffectCompilerFromResource 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1a3dabe0a2690c84e125af6d321397cbe3765f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196307"
---
# <a name="d3dxcreateeffectcompilerfromresource-function"></a><span data-ttu-id="46e59-103">D3DXCreateEffectCompilerFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="46e59-103">D3DXCreateEffectCompilerFromResource function</span></span>

<span data-ttu-id="46e59-104">從 ASCII 效果描述建立 [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) 。</span><span class="sxs-lookup"><span data-stu-id="46e59-104">Creates an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="46e59-105">語法</span><span class="sxs-lookup"><span data-stu-id="46e59-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompilerFromResource(
  _In_        HMODULE              hSrcModule,
  _In_        LPCTSTR              pSrcResource,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="46e59-106">參數</span><span class="sxs-lookup"><span data-stu-id="46e59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46e59-107">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46e59-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e59-108">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46e59-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46e59-109">包含效果描述之模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="46e59-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="46e59-110">如果這個參數為 **Null**，則會使用目前的模組。</span><span class="sxs-lookup"><span data-stu-id="46e59-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="46e59-111">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46e59-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e59-112">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46e59-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46e59-113">資源的指標。</span><span class="sxs-lookup"><span data-stu-id="46e59-113">Pointer to the resource.</span></span> <span data-ttu-id="46e59-114">此參數支援 Unicode 和 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="46e59-114">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="46e59-115">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="46e59-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="46e59-116">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46e59-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e59-117">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="46e59-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="46e59-118">[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列，描述預處理器定義。</span><span class="sxs-lookup"><span data-stu-id="46e59-118">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="46e59-119">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="46e59-119">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="46e59-120">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="46e59-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e59-121">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="46e59-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="46e59-122">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="46e59-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="46e59-123">如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="46e59-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="46e59-124">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="46e59-124">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e59-125">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46e59-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46e59-126">不同旗標所識別的編譯選項 (參閱 [D3DXSHADER 旗標](d3dxshader-flags.md)) 。</span><span class="sxs-lookup"><span data-stu-id="46e59-126">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="46e59-127">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="46e59-127">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="46e59-128">請參閱 [效果-編譯器工具](../direct3dtools/fxc.md) 以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="46e59-128">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="46e59-129">*ppEffectCompiler* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="46e59-129">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46e59-130">類型： **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="46e59-130">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="46e59-131">[**ID3DXEffectCompiler**](id3dxeffectcompiler.md)介面指標的位址，其中包含效果編譯器。</span><span class="sxs-lookup"><span data-stu-id="46e59-131">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="46e59-132">*ppParseErrors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="46e59-132">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46e59-133">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="46e59-133">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="46e59-134">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址，其中包含在編譯期間發生的任何錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="46e59-134">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="46e59-135">這個參數可以設定為 **Null** ，以忽略錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="46e59-135">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46e59-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="46e59-136">Return value</span></span>

<span data-ttu-id="46e59-137">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46e59-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46e59-138">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="46e59-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="46e59-139">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="46e59-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="46e59-140">備註</span><span class="sxs-lookup"><span data-stu-id="46e59-140">Remarks</span></span>

<span data-ttu-id="46e59-141">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="46e59-141">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="46e59-142">否則，LPCTSTR 資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="46e59-142">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="46e59-143">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="46e59-143">The compiler setting also determines the function version.</span></span> <span data-ttu-id="46e59-144">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateEffectCompilerFromResourceW。</span><span class="sxs-lookup"><span data-stu-id="46e59-144">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromResourceW.</span></span> <span data-ttu-id="46e59-145">否則，函式呼叫會解析為 D3DXCreateEffectCompilerFromResourceA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="46e59-145">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="46e59-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="46e59-146">Requirements</span></span>



| <span data-ttu-id="46e59-147">需求</span><span class="sxs-lookup"><span data-stu-id="46e59-147">Requirement</span></span> | <span data-ttu-id="46e59-148">值</span><span class="sxs-lookup"><span data-stu-id="46e59-148">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="46e59-149">標頭</span><span class="sxs-lookup"><span data-stu-id="46e59-149">Header</span></span><br/>  | <dl> <span data-ttu-id="46e59-150"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="46e59-150"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="46e59-151">程式庫</span><span class="sxs-lookup"><span data-stu-id="46e59-151">Library</span></span><br/> | <dl> <span data-ttu-id="46e59-152"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="46e59-152"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="46e59-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="46e59-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46e59-154">效果函數</span><span class="sxs-lookup"><span data-stu-id="46e59-154">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="46e59-155">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="46e59-155">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="46e59-156">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="46e59-156">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> </dl>

 

 
