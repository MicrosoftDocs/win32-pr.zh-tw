---
description: 從 ASCII 或二進位效果描述建立效果。
ms.assetid: b5868ba3-0869-46f7-804f-3103358a3ef5
title: 'D3DXCreateEffectFromFile 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f34d0cdb3ae19772f21d8307fffb395c4d1ac9ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696796"
---
# <a name="d3dxcreateeffectfromfile-function"></a><span data-ttu-id="535e3-103">D3DXCreateEffectFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="535e3-103">D3DXCreateEffectFromFile function</span></span>

<span data-ttu-id="535e3-104">從 ASCII 或二進位效果描述建立效果。</span><span class="sxs-lookup"><span data-stu-id="535e3-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="535e3-105">語法</span><span class="sxs-lookup"><span data-stu-id="535e3-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromFile(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="535e3-106">參數</span><span class="sxs-lookup"><span data-stu-id="535e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="535e3-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="535e3-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="535e3-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="535e3-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="535e3-109">將建立效果之裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="535e3-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="535e3-110">請參閱 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)。</span><span class="sxs-lookup"><span data-stu-id="535e3-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="535e3-111">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="535e3-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="535e3-112">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="535e3-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="535e3-113">檔案名的指標。</span><span class="sxs-lookup"><span data-stu-id="535e3-113">Pointer to the filename.</span></span> <span data-ttu-id="535e3-114">此參數支援 Unicode 和 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="535e3-114">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="535e3-115">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="535e3-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="535e3-116">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="535e3-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="535e3-117">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="535e3-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="535e3-118">預處理器巨集定義的選擇性 Null 結束陣列。</span><span class="sxs-lookup"><span data-stu-id="535e3-118">Optional NULL-terminated array of preprocessor macro definitions.</span></span> <span data-ttu-id="535e3-119">請參閱 [**D3DXMACRO**](d3dxmacro.md)。</span><span class="sxs-lookup"><span data-stu-id="535e3-119">See [**D3DXMACRO**](d3dxmacro.md).</span></span>

</dd> <dt>

<span data-ttu-id="535e3-120">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="535e3-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="535e3-121">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="535e3-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="535e3-122">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="535e3-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="535e3-123">如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="535e3-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="535e3-124">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="535e3-124">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="535e3-125">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="535e3-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="535e3-126">如果 *pSrcFile* 包含文字效果，旗標可以是 [D3DXSHADER 旗標](d3dxshader-flags.md) 和 [D3DXFX](d3dxfx.md) 旗標的組合;否則， *pSrcFile* 會包含二進位效果，而唯一接受的旗標為 D3DXFX 旗標。</span><span class="sxs-lookup"><span data-stu-id="535e3-126">If *pSrcFile* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcFile* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="535e3-127">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="535e3-127">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="535e3-128">請參閱 [效果-編譯器工具](../direct3dtools/fxc.md) 以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="535e3-128">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="535e3-129">*pPool* \[在\]</span><span class="sxs-lookup"><span data-stu-id="535e3-129">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="535e3-130">類型： **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="535e3-130">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="535e3-131">要用於共用參數之 [**ID3DXEffectPool**](id3dxeffectpool.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="535e3-131">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="535e3-132">如果這個值為 **Null**，則不會共用任何參數。</span><span class="sxs-lookup"><span data-stu-id="535e3-132">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="535e3-133">*ppEffect* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="535e3-133">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="535e3-134">類型： **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="535e3-134">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="535e3-135">傳回包含已編譯效果的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="535e3-135">Returns a pointer to a buffer containing the compiled effect.</span></span> <span data-ttu-id="535e3-136">請參閱 [**ID3DXEffect**](id3dxeffect.md)。</span><span class="sxs-lookup"><span data-stu-id="535e3-136">See [**ID3DXEffect**](id3dxeffect.md).</span></span>

</dd> <dt>

<span data-ttu-id="535e3-137">*ppCompilationErrors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="535e3-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="535e3-138">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="535e3-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="535e3-139">傳回包含編譯錯誤清單的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="535e3-139">Returns a pointer to a buffer containing a listing of compile errors.</span></span> <span data-ttu-id="535e3-140">請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="535e3-140">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="535e3-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="535e3-141">Return value</span></span>

<span data-ttu-id="535e3-142">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="535e3-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="535e3-143">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="535e3-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="535e3-144">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="535e3-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="535e3-145">備註</span><span class="sxs-lookup"><span data-stu-id="535e3-145">Remarks</span></span>

<span data-ttu-id="535e3-146">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="535e3-146">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="535e3-147">否則，LPCTSTR 資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="535e3-147">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="535e3-148">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="535e3-148">The compiler setting also determines the function version.</span></span> <span data-ttu-id="535e3-149">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateEffectFromFileW。</span><span class="sxs-lookup"><span data-stu-id="535e3-149">If Unicode is defined, the function call resolves to D3DXCreateEffectFromFileW.</span></span> <span data-ttu-id="535e3-150">否則，函式呼叫會解析為 D3DXCreateEffectFromFileA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="535e3-150">Otherwise, the function call resolves to D3DXCreateEffectFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="535e3-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="535e3-151">Requirements</span></span>



| <span data-ttu-id="535e3-152">需求</span><span class="sxs-lookup"><span data-stu-id="535e3-152">Requirement</span></span> | <span data-ttu-id="535e3-153">值</span><span class="sxs-lookup"><span data-stu-id="535e3-153">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="535e3-154">標頭</span><span class="sxs-lookup"><span data-stu-id="535e3-154">Header</span></span><br/>  | <dl> <span data-ttu-id="535e3-155"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="535e3-155"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="535e3-156">程式庫</span><span class="sxs-lookup"><span data-stu-id="535e3-156">Library</span></span><br/> | <dl> <span data-ttu-id="535e3-157"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="535e3-157"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="535e3-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="535e3-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="535e3-159">效果函數</span><span class="sxs-lookup"><span data-stu-id="535e3-159">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="535e3-160">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="535e3-160">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="535e3-161">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="535e3-161">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
