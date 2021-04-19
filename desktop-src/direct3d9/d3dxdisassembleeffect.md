---
description: 分解效果。
ms.assetid: d95d6e97-2e79-4cd2-965e-483aa1a1ddbc
title: 'D3DXDisassembleEffect 函式 (D3DX9Effect) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDisassembleEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 945c30319d16264a2b7489d1dc0849a4678cbede
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000595"
---
# <a name="d3dxdisassembleeffect-function"></a><span data-ttu-id="6c7f6-103">D3DXDisassembleEffect 函式</span><span class="sxs-lookup"><span data-stu-id="6c7f6-103">D3DXDisassembleEffect function</span></span>

<span data-ttu-id="6c7f6-104">分解效果。</span><span class="sxs-lookup"><span data-stu-id="6c7f6-104">Disassemble an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c7f6-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c7f6-105">Syntax</span></span>


```C++
HRESULT D3DXDisassembleEffect(
  _In_  LPD3DXEFFECT pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ LPD3DXBUFFER *ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="6c7f6-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c7f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c7f6-107">*pEffect* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c7f6-107">*pEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c7f6-108">類型： **[ **LPD3DXEFFECT**](id3dxeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="6c7f6-108">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)**</span></span>

<span data-ttu-id="6c7f6-109">包含效果的 [**ID3DXEffect**](id3dxeffect.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="6c7f6-109">Pointer to an [**ID3DXEffect**](id3dxeffect.md) interface that contains the effect.</span></span>

</dd> <dt>

<span data-ttu-id="6c7f6-110">*EnableColorCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c7f6-110">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c7f6-111">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c7f6-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c7f6-112">啟用色彩編碼，讓反組解碼更容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="6c7f6-112">Enable color coding to make the disassembly easier to read.</span></span>

</dd> <dt>

<span data-ttu-id="6c7f6-113">*ppDisassembly* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c7f6-113">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c7f6-114">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c7f6-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6c7f6-115">傳回包含已拆解著色器的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="6c7f6-115">Returns a buffer containing the disassembled shader.</span></span> <span data-ttu-id="6c7f6-116">請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="6c7f6-116">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c7f6-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c7f6-117">Return value</span></span>

<span data-ttu-id="6c7f6-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6c7f6-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6c7f6-119">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="6c7f6-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6c7f6-120">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="6c7f6-120">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c7f6-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c7f6-121">Requirements</span></span>



| <span data-ttu-id="6c7f6-122">需求</span><span class="sxs-lookup"><span data-stu-id="6c7f6-122">Requirement</span></span> | <span data-ttu-id="6c7f6-123">值</span><span class="sxs-lookup"><span data-stu-id="6c7f6-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c7f6-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6c7f6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6c7f6-125"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c7f6-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6c7f6-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="6c7f6-126">Library</span></span><br/> | <dl> <span data-ttu-id="6c7f6-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c7f6-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6c7f6-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c7f6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c7f6-129">效果函數</span><span class="sxs-lookup"><span data-stu-id="6c7f6-129">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 
