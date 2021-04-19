---
description: 從 ASCII 或二進位效果描述建立效果。 此函式是 D3DXCreateEffectFromFile 的延伸版本，可讓應用程式控制效果系統會忽略哪些參數。
ms.assetid: 963caa1e-bc1a-4d4b-bdb1-50b17d8b4132
title: 'D3DXCreateEffectFromFileEx 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFileEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b3d97c5aa23dd0711cfb00585e5b8ba7d410fc02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976513"
---
# <a name="d3dxcreateeffectfromfileex-function"></a><span data-ttu-id="0ef6d-104">D3DXCreateEffectFromFileEx 函式</span><span class="sxs-lookup"><span data-stu-id="0ef6d-104">D3DXCreateEffectFromFileEx function</span></span>

<span data-ttu-id="0ef6d-105">從 ASCII 或二進位效果描述建立效果。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-105">Create an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="0ef6d-106">此函式是 [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) 的延伸版本，可讓應用程式控制效果系統會忽略哪些參數。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-106">This function is an extended version of [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef6d-107">語法</span><span class="sxs-lookup"><span data-stu-id="0ef6d-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromFileEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="0ef6d-108">參數</span><span class="sxs-lookup"><span data-stu-id="0ef6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ef6d-109">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0ef6d-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef6d-110">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0ef6d-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0ef6d-111">將建立效果之裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-111">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="0ef6d-112">請參閱 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-112">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="0ef6d-113">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0ef6d-113">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef6d-114">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ef6d-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ef6d-115">檔案名的指標。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-115">Pointer to the filename.</span></span> <span data-ttu-id="0ef6d-116">此參數支援 Unicode 和 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-116">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="0ef6d-117">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0ef6d-118">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0ef6d-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef6d-119">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="0ef6d-119">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="0ef6d-120">預處理器巨集定義的選擇性 Null 結束陣列。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-120">Optional NULL-terminated array of preprocessor macro definitions.</span></span> <span data-ttu-id="0ef6d-121">請參閱 [**D3DXMACRO**](d3dxmacro.md)。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-121">See [**D3DXMACRO**](d3dxmacro.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ef6d-122">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0ef6d-122">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef6d-123">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="0ef6d-123">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="0ef6d-124">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-124">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="0ef6d-125">如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-125">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="0ef6d-126">*pSkipConstants* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0ef6d-126">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef6d-127">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ef6d-127">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ef6d-128">效果系統將忽略效果參數的字串。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-128">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="0ef6d-129">字串必須以 **Null** 結束，且必須包含每個應用程式管理的常數名稱（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-129">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="0ef6d-130">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="0ef6d-130">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef6d-131">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ef6d-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ef6d-132">如果 *pSrcFile* 包含文字效果，旗標可以是 [D3DXSHADER 旗標](d3dxshader-flags.md) 和 [D3DXFX](d3dxfx.md) 旗標的組合;否則， *pSrcFile* 會包含二進位效果，而唯一接受的旗標為 D3DXFX 旗標。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-132">If *pSrcFile* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcFile* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="0ef6d-133">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-133">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="0ef6d-134">請參閱 [效果-編譯器工具](../direct3dtools/fxc.md) 以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-134">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="0ef6d-135">*pPool* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0ef6d-135">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef6d-136">類型： **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="0ef6d-136">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="0ef6d-137">要用於共用參數之 [**ID3DXEffectPool**](id3dxeffectpool.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-137">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="0ef6d-138">如果這個值為 **Null**，則不會共用任何參數。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-138">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="0ef6d-139">*ppEffect* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0ef6d-139">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef6d-140">類型： **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ef6d-140">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="0ef6d-141">傳回包含已編譯效果的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-141">Returns a pointer to a buffer containing the compiled effect.</span></span> <span data-ttu-id="0ef6d-142">請參閱 [**ID3DXEffect**](id3dxeffect.md)。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-142">See [**ID3DXEffect**](id3dxeffect.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ef6d-143">*ppCompilationErrors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0ef6d-143">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef6d-144">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ef6d-144">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0ef6d-145">傳回包含編譯錯誤清單的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-145">Returns a pointer to a buffer containing a listing of compile errors.</span></span> <span data-ttu-id="0ef6d-146">請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-146">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ef6d-147">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ef6d-147">Return value</span></span>

<span data-ttu-id="0ef6d-148">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ef6d-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ef6d-149">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0ef6d-150">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-150">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ef6d-151">備註</span><span class="sxs-lookup"><span data-stu-id="0ef6d-151">Remarks</span></span>

<span data-ttu-id="0ef6d-152">此函式是 [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) 的延伸版本，可讓應用程式指定應用程式要管理哪些效果常數。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-152">This function is an extended version of [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="0ef6d-153">效果系統會忽略應用程式所管理的常數。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-153">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="0ef6d-154">也就是說，應用程式會負責初始化常數，並在適當時儲存和還原其狀態。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-154">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="0ef6d-155">此函式會檢查 pSkipConstants 中的每個常數，以查看：</span><span class="sxs-lookup"><span data-stu-id="0ef6d-155">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="0ef6d-156">它會系結至常數暫存器。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-156">It is bound to a constant register.</span></span>
-   <span data-ttu-id="0ef6d-157">它只會在 HLSL 著色器程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-157">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="0ef6d-158">如果常數是在不存在於效果中的字串中命名，則會忽略它。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-158">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

<span data-ttu-id="0ef6d-159">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-159">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="0ef6d-160">否則，LPCTSTR 資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-160">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="0ef6d-161">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-161">The compiler setting also determines the function version.</span></span> <span data-ttu-id="0ef6d-162">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateEffectFromFileW。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-162">If Unicode is defined, the function call resolves to D3DXCreateEffectFromFileW.</span></span> <span data-ttu-id="0ef6d-163">否則，函式呼叫會解析為 D3DXCreateEffectFromFileA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="0ef6d-163">Otherwise, the function call resolves to D3DXCreateEffectFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ef6d-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ef6d-164">Requirements</span></span>



| <span data-ttu-id="0ef6d-165">需求</span><span class="sxs-lookup"><span data-stu-id="0ef6d-165">Requirement</span></span> | <span data-ttu-id="0ef6d-166">值</span><span class="sxs-lookup"><span data-stu-id="0ef6d-166">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef6d-167">標頭</span><span class="sxs-lookup"><span data-stu-id="0ef6d-167">Header</span></span><br/>  | <dl> <span data-ttu-id="0ef6d-168"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="0ef6d-168"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="0ef6d-169">程式庫</span><span class="sxs-lookup"><span data-stu-id="0ef6d-169">Library</span></span><br/> | <dl> <span data-ttu-id="0ef6d-170"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ef6d-170"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0ef6d-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ef6d-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef6d-172">效果函數</span><span class="sxs-lookup"><span data-stu-id="0ef6d-172">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="0ef6d-173">**D3DXCreateEffectEx**</span><span class="sxs-lookup"><span data-stu-id="0ef6d-173">**D3DXCreateEffectEx**</span></span>](d3dxcreateeffectex.md)
</dt> <dt>

[<span data-ttu-id="0ef6d-174">**D3DXCreateEffectFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="0ef6d-174">**D3DXCreateEffectFromResourceEx**</span></span>](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
