---
description: 從 ASCII 或二進位效果描述建立效果。 此函式是 D3DXCreateEffect 的延伸版本，可讓應用程式控制效果系統會忽略哪些參數。
ms.assetid: b08f727e-6061-4e78-8243-08c4ccab342d
title: 'D3DXCreateEffectEx 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 979b09f852e692b4c25414607f79cd8792342755
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986101"
---
# <a name="d3dxcreateeffectex-function"></a><span data-ttu-id="9f042-104">D3DXCreateEffectEx 函式</span><span class="sxs-lookup"><span data-stu-id="9f042-104">D3DXCreateEffectEx function</span></span>

<span data-ttu-id="9f042-105">從 ASCII 或二進位效果描述建立效果。</span><span class="sxs-lookup"><span data-stu-id="9f042-105">Creates an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="9f042-106">此函式是 [**D3DXCreateEffect**](d3dxcreateeffect.md) 的延伸版本，可讓應用程式控制效果系統會忽略哪些參數。</span><span class="sxs-lookup"><span data-stu-id="9f042-106">This function is an extended version of [**D3DXCreateEffect**](d3dxcreateeffect.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f042-107">語法</span><span class="sxs-lookup"><span data-stu-id="9f042-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="9f042-108">參數</span><span class="sxs-lookup"><span data-stu-id="9f042-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f042-109">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9f042-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f042-110">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="9f042-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="9f042-111">將建立效果之裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="9f042-111">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="9f042-112">請參閱 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)。</span><span class="sxs-lookup"><span data-stu-id="9f042-112">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="9f042-113">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9f042-113">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f042-114">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f042-114">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f042-115">包含效果描述之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="9f042-115">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="9f042-116">*SrcDataLen* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9f042-116">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f042-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f042-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f042-118">效果資料的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="9f042-118">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9f042-119">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9f042-119">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f042-120">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="9f042-120">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="9f042-121">[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列，描述預處理器定義。</span><span class="sxs-lookup"><span data-stu-id="9f042-121">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="9f042-122">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="9f042-122">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9f042-123">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9f042-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f042-124">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="9f042-124">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="9f042-125">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="9f042-125">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="9f042-126">如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="9f042-126">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="9f042-127">*pSkipConstants* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9f042-127">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f042-128">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f042-128">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f042-129">效果系統將忽略效果參數的字串。</span><span class="sxs-lookup"><span data-stu-id="9f042-129">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="9f042-130">字串必須以 **Null** 結束，且必須包含每個應用程式管理的常數名稱（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="9f042-130">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="9f042-131">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="9f042-131">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f042-132">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f042-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f042-133">如果 *pSrcData* 包含文字效果，旗標可以是 [D3DXSHADER 旗標](d3dxshader-flags.md) 和 [D3DXFX](d3dxfx.md) 旗標的組合;否則， *pSrcData* 會包含二進位效果，而唯一接受的旗標為 D3DXFX 旗標。</span><span class="sxs-lookup"><span data-stu-id="9f042-133">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="9f042-134">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="9f042-134">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="9f042-135">請參閱 [效果-編譯器工具](../direct3dtools/fxc.md) 以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9f042-135">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="9f042-136">*pPool* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9f042-136">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f042-137">類型： **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="9f042-137">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="9f042-138">要用於共用參數之 [**ID3DXEffectPool**](id3dxeffectpool.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="9f042-138">Pointer to an [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="9f042-139">如果這個值為 **Null**，則不會共用任何參數。</span><span class="sxs-lookup"><span data-stu-id="9f042-139">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="9f042-140">*ppEffect* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9f042-140">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f042-141">類型： **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f042-141">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="9f042-142">傳回 [**ID3DXEffect**](id3dxeffect.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9f042-142">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="9f042-143">*ppCompilationErrors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9f042-143">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f042-144">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f042-144">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9f042-145">傳回包含編譯錯誤清單的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9f042-145">Returns a buffer containing a list of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f042-146">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f042-146">Return value</span></span>

<span data-ttu-id="9f042-147">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9f042-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9f042-148">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="9f042-148">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9f042-149">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="9f042-149">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f042-150">備註</span><span class="sxs-lookup"><span data-stu-id="9f042-150">Remarks</span></span>

<span data-ttu-id="9f042-151">此函式是 [**D3DXCreateEffect**](d3dxcreateeffect.md) 的延伸版本，可讓應用程式指定應用程式要管理哪些效果常數。</span><span class="sxs-lookup"><span data-stu-id="9f042-151">This function is an extended version of [**D3DXCreateEffect**](d3dxcreateeffect.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="9f042-152">效果系統會忽略應用程式所管理的常數。</span><span class="sxs-lookup"><span data-stu-id="9f042-152">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="9f042-153">也就是說，應用程式會負責初始化常數，並在適當時儲存和還原其狀態。</span><span class="sxs-lookup"><span data-stu-id="9f042-153">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="9f042-154">此函式會檢查 pSkipConstants 中的每個常數，以查看：</span><span class="sxs-lookup"><span data-stu-id="9f042-154">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="9f042-155">它會系結至常數暫存器。</span><span class="sxs-lookup"><span data-stu-id="9f042-155">It is bound to a constant register.</span></span>
-   <span data-ttu-id="9f042-156">它只會在 HLSL 著色器程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="9f042-156">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="9f042-157">如果常數是在不存在於效果中的字串中命名，則會忽略它。</span><span class="sxs-lookup"><span data-stu-id="9f042-157">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f042-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f042-158">Requirements</span></span>



| <span data-ttu-id="9f042-159">需求</span><span class="sxs-lookup"><span data-stu-id="9f042-159">Requirement</span></span> | <span data-ttu-id="9f042-160">值</span><span class="sxs-lookup"><span data-stu-id="9f042-160">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f042-161">標頭</span><span class="sxs-lookup"><span data-stu-id="9f042-161">Header</span></span><br/>  | <dl> <span data-ttu-id="9f042-162"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="9f042-162"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="9f042-163">程式庫</span><span class="sxs-lookup"><span data-stu-id="9f042-163">Library</span></span><br/> | <dl> <span data-ttu-id="9f042-164"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f042-164"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9f042-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9f042-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f042-166">效果函數</span><span class="sxs-lookup"><span data-stu-id="9f042-166">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="9f042-167">**D3DXCreateEffectFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="9f042-167">**D3DXCreateEffectFromFileEx**</span></span>](d3dxcreateeffectfromfileex.md)
</dt> <dt>

[<span data-ttu-id="9f042-168">**D3DXCreateEffectFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="9f042-168">**D3DXCreateEffectFromResourceEx**</span></span>](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
