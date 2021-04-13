---
description: 編譯效果。
ms.assetid: be6f862a-5091-4a06-a27a-308e81360129
title: 'ID3DXEffectCompiler：： CompileEffect 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6552d0216cd05c40c122657270c02e0886438da1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322716"
---
# <a name="id3dxeffectcompilercompileeffect-method"></a><span data-ttu-id="2a49b-103">ID3DXEffectCompiler：： CompileEffect 方法</span><span class="sxs-lookup"><span data-stu-id="2a49b-103">ID3DXEffectCompiler::CompileEffect method</span></span>

<span data-ttu-id="2a49b-104">編譯效果。</span><span class="sxs-lookup"><span data-stu-id="2a49b-104">Compile an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a49b-105">語法</span><span class="sxs-lookup"><span data-stu-id="2a49b-105">Syntax</span></span>


```C++
HRESULT CompileEffect(
  [in]          DWORD        Flags,
  [out, retval] LPD3DXBUFFER *ppEffect,
  [out, retval] LPD3DXBUFFER *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="2a49b-106">參數</span><span class="sxs-lookup"><span data-stu-id="2a49b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a49b-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="2a49b-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a49b-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a49b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2a49b-109">不同旗標所識別的編譯選項。</span><span class="sxs-lookup"><span data-stu-id="2a49b-109">Compile options identified by various flags.</span></span> <span data-ttu-id="2a49b-110">Direct3D 10 HLSL 編譯器現在是預設值。</span><span class="sxs-lookup"><span data-stu-id="2a49b-110">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="2a49b-111">如需詳細資料，請參閱 [D3DXSHADER 旗標](d3dxshader-flags.md) 。</span><span class="sxs-lookup"><span data-stu-id="2a49b-111">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="2a49b-112">*ppEffect* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="2a49b-112">*ppEffect* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2a49b-113">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="2a49b-113">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="2a49b-114">包含已編譯效果的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2a49b-114">Buffer containing the compiled effect.</span></span> <span data-ttu-id="2a49b-115">如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="2a49b-115">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a49b-116">*ppErrorMsgs* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="2a49b-116">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2a49b-117">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="2a49b-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="2a49b-118">包含至少發生第一個編譯錯誤訊息的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2a49b-118">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="2a49b-119">這包括對編譯器錯誤和高階語言編譯錯誤的影響。</span><span class="sxs-lookup"><span data-stu-id="2a49b-119">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="2a49b-120">如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="2a49b-120">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a49b-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a49b-121">Return value</span></span>

<span data-ttu-id="2a49b-122">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2a49b-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2a49b-123">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="2a49b-123">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="2a49b-124">如果引數無效，此方法將會傳回 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="2a49b-124">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="2a49b-125">如果方法失敗，傳回值將會是 E \_ 失敗。</span><span class="sxs-lookup"><span data-stu-id="2a49b-125">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a49b-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a49b-126">Requirements</span></span>



| <span data-ttu-id="2a49b-127">需求</span><span class="sxs-lookup"><span data-stu-id="2a49b-127">Requirement</span></span> | <span data-ttu-id="2a49b-128">值</span><span class="sxs-lookup"><span data-stu-id="2a49b-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a49b-129">標頭</span><span class="sxs-lookup"><span data-stu-id="2a49b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2a49b-130"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="2a49b-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2a49b-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="2a49b-131">Library</span></span><br/> | <dl> <span data-ttu-id="2a49b-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a49b-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2a49b-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a49b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a49b-134">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="2a49b-134">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> </dl>

 

 
