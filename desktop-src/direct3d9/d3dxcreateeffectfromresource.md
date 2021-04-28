---
description: D3DXCreateEffectFromResource 函式-從 ASCII 或二進位效果描述建立效果。
ms.assetid: 8385512c-e93d-4c07-b353-87717eb58bcd
title: 'D3DXCreateEffectFromResource 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f2a84d2da1f3ca88a117c0150e7b27485838c300
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107686"
---
# <a name="d3dxcreateeffectfromresource-function"></a><span data-ttu-id="eb5c5-103">D3DXCreateEffectFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="eb5c5-103">D3DXCreateEffectFromResource function</span></span>

<span data-ttu-id="eb5c5-104">從 ASCII 或二進位效果描述建立效果。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb5c5-105">語法</span><span class="sxs-lookup"><span data-stu-id="eb5c5-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromResource(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="eb5c5-106">參數</span><span class="sxs-lookup"><span data-stu-id="eb5c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb5c5-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb5c5-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb5c5-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="eb5c5-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="eb5c5-109">裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-109">Pointer to the device.</span></span>

</dd> <dt>

<span data-ttu-id="eb5c5-110">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb5c5-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb5c5-111">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb5c5-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb5c5-112">包含效果描述之模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-112">Handle to a module containing the effect description.</span></span> <span data-ttu-id="eb5c5-113">如果這個參數為 **Null**，則會使用目前的模組。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-113">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="eb5c5-114">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb5c5-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb5c5-115">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb5c5-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb5c5-116">資源的指標。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-116">Pointer to the resource.</span></span> <span data-ttu-id="eb5c5-117">此參數支援 Unicode 和 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-117">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="eb5c5-118">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="eb5c5-119">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb5c5-119">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb5c5-120">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="eb5c5-120">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="eb5c5-121">[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列，描述預處理器定義。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-121">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="eb5c5-122">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-122">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="eb5c5-123">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb5c5-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb5c5-124">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="eb5c5-124">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="eb5c5-125">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-125">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="eb5c5-126">如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-126">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="eb5c5-127">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="eb5c5-127">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb5c5-128">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb5c5-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb5c5-129">如果 *hSrcModule* 包含文字效果，旗標可以是 [D3DXSHADER 旗標](d3dxshader-flags.md) 和 [D3DXFX](d3dxfx.md) 旗標的組合;否則， *hSrcModule* 會包含二進位效果，而唯一接受的旗標為 D3DXFX 旗標。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-129">If *hSrcModule* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *hSrcModule* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="eb5c5-130">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-130">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="eb5c5-131">請參閱 [效果-編譯器工具](../direct3dtools/fxc.md) 以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-131">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="eb5c5-132">*pPool* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eb5c5-132">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb5c5-133">類型： **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="eb5c5-133">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="eb5c5-134">要用於共用參數之 [**ID3DXEffectPool**](id3dxeffectpool.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-134">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="eb5c5-135">如果這個值為 **Null**，則不會共用任何參數。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-135">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="eb5c5-136">*ppEffect* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="eb5c5-136">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb5c5-137">類型： **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb5c5-137">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="eb5c5-138">傳回包含已編譯效果的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-138">Returns a buffer containing the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="eb5c5-139">*ppCompilationErrors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="eb5c5-139">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb5c5-140">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb5c5-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="eb5c5-141">傳回包含編譯錯誤清單的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-141">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb5c5-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb5c5-142">Return value</span></span>

<span data-ttu-id="eb5c5-143">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eb5c5-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eb5c5-144">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-144">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="eb5c5-145">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-145">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb5c5-146">備註</span><span class="sxs-lookup"><span data-stu-id="eb5c5-146">Remarks</span></span>

<span data-ttu-id="eb5c5-147">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-147">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="eb5c5-148">否則，LPCTSTR 資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-148">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="eb5c5-149">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-149">The compiler setting also determines the function version.</span></span> <span data-ttu-id="eb5c5-150">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateEffectFromResourceW。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-150">If Unicode is defined, the function call resolves to D3DXCreateEffectFromResourceW.</span></span> <span data-ttu-id="eb5c5-151">否則，函式呼叫會解析為 D3DXCreateEffectFromResourceA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-151">Otherwise, the function call resolves to D3DXCreateEffectFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="eb5c5-152">D3DXCreateEffectFromResource 會從 RT RCDATA 類型的資源載入資料 \_ 。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-152">D3DXCreateEffectFromResource loads data from a resource of type RT\_RCDATA.</span></span> <span data-ttu-id="eb5c5-153">如需 Windows 資源的詳細資訊，請參閱 MSDN。</span><span class="sxs-lookup"><span data-stu-id="eb5c5-153">See MSDN for more information about Windows resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb5c5-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb5c5-154">Requirements</span></span>



| <span data-ttu-id="eb5c5-155">需求</span><span class="sxs-lookup"><span data-stu-id="eb5c5-155">Requirement</span></span> | <span data-ttu-id="eb5c5-156">值</span><span class="sxs-lookup"><span data-stu-id="eb5c5-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb5c5-157">標頭</span><span class="sxs-lookup"><span data-stu-id="eb5c5-157">Header</span></span><br/>  | <dl> <span data-ttu-id="eb5c5-158"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="eb5c5-158"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="eb5c5-159">程式庫</span><span class="sxs-lookup"><span data-stu-id="eb5c5-159">Library</span></span><br/> | <dl> <span data-ttu-id="eb5c5-160"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb5c5-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="eb5c5-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb5c5-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb5c5-162">效果函數</span><span class="sxs-lookup"><span data-stu-id="eb5c5-162">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="eb5c5-163">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="eb5c5-163">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="eb5c5-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="eb5c5-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
