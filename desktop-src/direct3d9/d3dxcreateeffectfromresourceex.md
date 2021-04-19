---
description: 從 ASCII 或二進位效果描述建立效果。 這是 D3DXCreateEffectFromResource 的延伸版本，可讓應用程式控制效果系統會忽略哪些參數。
ms.assetid: 5937bdb1-750a-41f8-a49d-3643427f3e3c
title: 'D3DXCreateEffectFromResourceEx 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResourceEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d0ae7a0ee43f93019f3c4c1f6145b3d8aa0e4367
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985899"
---
# <a name="d3dxcreateeffectfromresourceex-function"></a><span data-ttu-id="13748-104">D3DXCreateEffectFromResourceEx 函式</span><span class="sxs-lookup"><span data-stu-id="13748-104">D3DXCreateEffectFromResourceEx function</span></span>

<span data-ttu-id="13748-105">從 ASCII 或二進位效果描述建立效果。</span><span class="sxs-lookup"><span data-stu-id="13748-105">Create an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="13748-106">這是 [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) 的延伸版本，可讓應用程式控制效果系統會忽略哪些參數。</span><span class="sxs-lookup"><span data-stu-id="13748-106">This is an extended version of [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="13748-107">語法</span><span class="sxs-lookup"><span data-stu-id="13748-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromResourceEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="13748-108">參數</span><span class="sxs-lookup"><span data-stu-id="13748-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13748-109">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13748-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13748-110">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="13748-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="13748-111">裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="13748-111">Pointer to the device.</span></span>

</dd> <dt>

<span data-ttu-id="13748-112">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13748-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13748-113">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13748-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13748-114">包含效果描述之模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="13748-114">Handle to a module containing the effect description.</span></span> <span data-ttu-id="13748-115">如果這個參數為 **Null**，則會使用目前的模組。</span><span class="sxs-lookup"><span data-stu-id="13748-115">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="13748-116">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13748-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13748-117">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13748-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13748-118">資源的指標。</span><span class="sxs-lookup"><span data-stu-id="13748-118">Pointer to the resource.</span></span> <span data-ttu-id="13748-119">此參數支援 Unicode 和 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="13748-119">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="13748-120">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="13748-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="13748-121">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13748-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13748-122">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="13748-122">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="13748-123">[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列，描述預處理器定義。</span><span class="sxs-lookup"><span data-stu-id="13748-123">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="13748-124">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="13748-124">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="13748-125">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13748-125">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13748-126">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="13748-126">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="13748-127">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="13748-127">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="13748-128">如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="13748-128">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="13748-129">*pSkipConstants* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13748-129">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13748-130">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13748-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13748-131">效果系統將忽略效果參數的字串。</span><span class="sxs-lookup"><span data-stu-id="13748-131">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="13748-132">字串必須以 **Null** 結束，且必須包含每個應用程式管理的常數名稱（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="13748-132">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="13748-133">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="13748-133">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13748-134">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13748-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13748-135">如果 *pSrcResource* 包含文字效果，旗標可以是 [D3DXSHADER 旗標](d3dxshader-flags.md) 和 [D3DXFX](d3dxfx.md) 旗標的組合;否則， *pSrcResource* 會包含二進位效果，而唯一接受的旗標為 D3DXFX 旗標。</span><span class="sxs-lookup"><span data-stu-id="13748-135">If *pSrcResource* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcResource* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="13748-136">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="13748-136">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="13748-137">請參閱 [效果-編譯器工具](../direct3dtools/fxc.md) 以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="13748-137">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="13748-138">*pPool* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13748-138">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13748-139">類型： **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="13748-139">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="13748-140">要用於共用參數之 [**ID3DXEffectPool**](id3dxeffectpool.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="13748-140">Pointer to an [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="13748-141">如果這個值為 **Null**，則不會共用任何參數。</span><span class="sxs-lookup"><span data-stu-id="13748-141">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="13748-142">*ppEffect* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="13748-142">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13748-143">類型： **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="13748-143">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="13748-144">傳回包含已編譯效果的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="13748-144">Returns a buffer containing the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="13748-145">*ppCompilationErrors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="13748-145">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13748-146">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="13748-146">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="13748-147">傳回包含編譯錯誤清單的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="13748-147">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13748-148">傳回值</span><span class="sxs-lookup"><span data-stu-id="13748-148">Return value</span></span>

<span data-ttu-id="13748-149">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="13748-149">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="13748-150">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="13748-150">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="13748-151">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="13748-151">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="13748-152">備註</span><span class="sxs-lookup"><span data-stu-id="13748-152">Remarks</span></span>

<span data-ttu-id="13748-153">此函式是 [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) 的延伸版本，可讓應用程式指定應用程式要管理哪些效果常數。</span><span class="sxs-lookup"><span data-stu-id="13748-153">This function is an extended version of [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="13748-154">效果系統會忽略應用程式所管理的常數。</span><span class="sxs-lookup"><span data-stu-id="13748-154">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="13748-155">也就是說，應用程式會負責初始化常數，並在適當時儲存和還原其狀態。</span><span class="sxs-lookup"><span data-stu-id="13748-155">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="13748-156">此函式會檢查 pSkipConstants 中的每個常數，以查看：</span><span class="sxs-lookup"><span data-stu-id="13748-156">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="13748-157">它會系結至常數暫存器。</span><span class="sxs-lookup"><span data-stu-id="13748-157">It is bound to a constant register.</span></span>
-   <span data-ttu-id="13748-158">它只會在 HLSL 著色器程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="13748-158">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="13748-159">如果常數是在不存在於效果中的字串中命名，則會忽略它。</span><span class="sxs-lookup"><span data-stu-id="13748-159">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

<span data-ttu-id="13748-160">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="13748-160">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="13748-161">否則，LPCTSTR 資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="13748-161">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="13748-162">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="13748-162">The compiler setting also determines the function version.</span></span> <span data-ttu-id="13748-163">如果已定義 Unicode，函式呼叫會解析為 D3DXCreateEffectFromResourceW。</span><span class="sxs-lookup"><span data-stu-id="13748-163">If Unicode is defined, the function call resolves to D3DXCreateEffectFromResourceW.</span></span> <span data-ttu-id="13748-164">否則，函式呼叫會解析為 D3DXCreateEffectFromResourceA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="13748-164">Otherwise, the function call resolves to D3DXCreateEffectFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="13748-165">D3DXCreateEffectFromResource 會從 RT RCDATA 類型的資源載入資料 \_ 。</span><span class="sxs-lookup"><span data-stu-id="13748-165">D3DXCreateEffectFromResource loads data from a resource of type RT\_RCDATA.</span></span> <span data-ttu-id="13748-166">如需 Windows 資源的詳細資訊，請參閱 MSDN。</span><span class="sxs-lookup"><span data-stu-id="13748-166">See MSDN for more information about Windows resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="13748-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="13748-167">Requirements</span></span>



| <span data-ttu-id="13748-168">需求</span><span class="sxs-lookup"><span data-stu-id="13748-168">Requirement</span></span> | <span data-ttu-id="13748-169">值</span><span class="sxs-lookup"><span data-stu-id="13748-169">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="13748-170">標頭</span><span class="sxs-lookup"><span data-stu-id="13748-170">Header</span></span><br/>  | <dl> <span data-ttu-id="13748-171"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="13748-171"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="13748-172">程式庫</span><span class="sxs-lookup"><span data-stu-id="13748-172">Library</span></span><br/> | <dl> <span data-ttu-id="13748-173"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="13748-173"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="13748-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13748-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13748-175">效果函數</span><span class="sxs-lookup"><span data-stu-id="13748-175">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="13748-176">**D3DXCreateEffectEx**</span><span class="sxs-lookup"><span data-stu-id="13748-176">**D3DXCreateEffectEx**</span></span>](d3dxcreateeffectex.md)
</dt> <dt>

[<span data-ttu-id="13748-177">**D3DXCreateEffectFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="13748-177">**D3DXCreateEffectFromFileEx**</span></span>](d3dxcreateeffectfromfileex.md)
</dt> </dl>

 

 
