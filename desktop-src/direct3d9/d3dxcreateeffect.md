---
description: 從 ASCII 或二進位效果描述建立效果。
ms.assetid: 1cbd91f2-3cda-4770-a3c5-b1e6702628d1
title: 'D3DXCreateEffect 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3d5ac013617368ba4d702815d79aa411ea2988b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991967"
---
# <a name="d3dxcreateeffect-function"></a><span data-ttu-id="6a791-103">D3DXCreateEffect 函式</span><span class="sxs-lookup"><span data-stu-id="6a791-103">D3DXCreateEffect function</span></span>

<span data-ttu-id="6a791-104">從 ASCII 或二進位效果描述建立效果。</span><span class="sxs-lookup"><span data-stu-id="6a791-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a791-105">語法</span><span class="sxs-lookup"><span data-stu-id="6a791-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="6a791-106">參數</span><span class="sxs-lookup"><span data-stu-id="6a791-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a791-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a791-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a791-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6a791-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6a791-109">將建立效果之裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="6a791-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="6a791-110">請參閱 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)。</span><span class="sxs-lookup"><span data-stu-id="6a791-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="6a791-111">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a791-111">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a791-112">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a791-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a791-113">包含效果描述之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="6a791-113">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="6a791-114">*SrcDataLen* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a791-114">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a791-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a791-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a791-116">效果資料的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="6a791-116">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="6a791-117">*pDefines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a791-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a791-118">Type： **Const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="6a791-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="6a791-119">[**D3DXMACRO**](d3dxmacro.md)結構的選擇性 **Null** 終止陣列，描述預處理器定義。</span><span class="sxs-lookup"><span data-stu-id="6a791-119">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="6a791-120">這個值可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6a791-120">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6a791-121">*pInclude* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a791-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a791-122">類型： **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="6a791-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="6a791-123">選用介面指標 [**ID3DXInclude**](id3dxinclude.md)，用來處理 include 指示詞 \# 。</span><span class="sxs-lookup"><span data-stu-id="6a791-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="6a791-124">如果這個值為 **Null**，則 \# 在從檔案進行編譯時，將會接受 include，或在從資源或記憶體編譯時，將會造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="6a791-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="6a791-125">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="6a791-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a791-126">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a791-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a791-127">如果 *pSrcData* 包含文字效果，旗標可以是 [D3DXSHADER 旗標](d3dxshader-flags.md) 和 [D3DXFX](d3dxfx.md) 旗標的組合;否則， *pSrcData* 會包含二進位效果，而唯一接受的旗標為 D3DXFX 旗標。</span><span class="sxs-lookup"><span data-stu-id="6a791-127">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="6a791-128">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="6a791-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="6a791-129">請參閱 [效果-編譯器工具](../direct3dtools/fxc.md) 以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6a791-129">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="6a791-130">*pPool* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a791-130">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a791-131">類型： **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="6a791-131">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="6a791-132">要用於共用參數之 [**ID3DXEffectPool**](id3dxeffectpool.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="6a791-132">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="6a791-133">如果這個值為 **Null**，則不會共用任何參數。</span><span class="sxs-lookup"><span data-stu-id="6a791-133">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="6a791-134">*ppEffect* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6a791-134">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a791-135">類型： **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a791-135">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="6a791-136">傳回 [**ID3DXEffect**](id3dxeffect.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6a791-136">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="6a791-137">*ppCompilationErrors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6a791-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a791-138">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a791-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6a791-139">傳回包含編譯錯誤清單的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6a791-139">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a791-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a791-140">Return value</span></span>

<span data-ttu-id="6a791-141">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6a791-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6a791-142">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="6a791-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6a791-143">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="6a791-143">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a791-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a791-144">Requirements</span></span>



| <span data-ttu-id="6a791-145">需求</span><span class="sxs-lookup"><span data-stu-id="6a791-145">Requirement</span></span> | <span data-ttu-id="6a791-146">值</span><span class="sxs-lookup"><span data-stu-id="6a791-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a791-147">標頭</span><span class="sxs-lookup"><span data-stu-id="6a791-147">Header</span></span><br/>  | <dl> <span data-ttu-id="6a791-148"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a791-148"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6a791-149">程式庫</span><span class="sxs-lookup"><span data-stu-id="6a791-149">Library</span></span><br/> | <dl> <span data-ttu-id="6a791-150"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a791-150"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6a791-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a791-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a791-152">效果函數</span><span class="sxs-lookup"><span data-stu-id="6a791-152">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="6a791-153">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="6a791-153">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="6a791-154">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="6a791-154">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
