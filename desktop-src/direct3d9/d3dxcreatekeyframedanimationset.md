---
description: 建立 ID3DXKeyframedAnimationSet 索引鍵的框架動畫集合介面。
ms.assetid: 7b4fffdc-696c-400c-a0cc-fc755fd25b75
title: 'D3DXCreateKeyframedAnimationSet 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateKeyframedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f3eb45e999d25c776014c3df5824e0468d03ffd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986121"
---
# <a name="d3dxcreatekeyframedanimationset-function"></a><span data-ttu-id="00ca0-103">D3DXCreateKeyframedAnimationSet 函式</span><span class="sxs-lookup"><span data-stu-id="00ca0-103">D3DXCreateKeyframedAnimationSet function</span></span>

<span data-ttu-id="00ca0-104">建立 [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) 索引鍵的框架動畫集合介面。</span><span class="sxs-lookup"><span data-stu-id="00ca0-104">Creates a [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) key framed animation set interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="00ca0-105">語法</span><span class="sxs-lookup"><span data-stu-id="00ca0-105">Syntax</span></span>


```C++
HRESULT D3DXCreateKeyframedAnimationSet(
  _In_        LPCSTR                      pName,
  _In_        DOUBLE                      TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE           Playback,
  _In_        UINT                        NumAnimations,
  _In_        UINT                        NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK          *pCallKeys,
  _Out_       LPD3DXKEYFRAMEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a><span data-ttu-id="00ca0-106">參數</span><span class="sxs-lookup"><span data-stu-id="00ca0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00ca0-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00ca0-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00ca0-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00ca0-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00ca0-109">動畫集合名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="00ca0-109">Pointer to the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="00ca0-110">*TicksPerSecond* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00ca0-110">*TicksPerSecond* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00ca0-111">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00ca0-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00ca0-112">每秒經過的主要畫面格刻度數目。</span><span class="sxs-lookup"><span data-stu-id="00ca0-112">Number of key frame ticks that elapse per second.</span></span>

</dd> <dt>

<span data-ttu-id="00ca0-113">*播放* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00ca0-113">*Playback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00ca0-114">類型： **[ **D3DXPLAYBACK \_ 類型**](./d3dxplayback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="00ca0-114">Type: **[**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md)**</span></span>

<span data-ttu-id="00ca0-115">動畫集合播放迴圈的型別。</span><span class="sxs-lookup"><span data-stu-id="00ca0-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="00ca0-116">請參閱 [**D3DXPLAYBACK \_ 類型**](./d3dxplayback-type.md)。</span><span class="sxs-lookup"><span data-stu-id="00ca0-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="00ca0-117">*NumAnimations* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00ca0-117">*NumAnimations* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00ca0-118">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00ca0-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00ca0-119">調整規模、旋轉和轉譯 (SRT) 動畫組的數目。</span><span class="sxs-lookup"><span data-stu-id="00ca0-119">Number of scale, rotate, and translate (SRT) animation sets.</span></span>

</dd> <dt>

<span data-ttu-id="00ca0-120">*NumCallbackKeys* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00ca0-120">*NumCallbackKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00ca0-121">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="00ca0-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="00ca0-122">回呼金鑰數目。</span><span class="sxs-lookup"><span data-stu-id="00ca0-122">Number of callback keys.</span></span>

</dd> <dt>

<span data-ttu-id="00ca0-123">*pCallKeys* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00ca0-123">*pCallKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00ca0-124">類型： **Const [**LPD3DXKEY \_ 回呼**](d3dxkey-callback.md) \***</span><span class="sxs-lookup"><span data-stu-id="00ca0-124">Type: **const [**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)\***</span></span>

<span data-ttu-id="00ca0-125">儲存使用者回呼資料的 [**D3DXKEY \_ 回呼**](d3dxkey-callback.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="00ca0-125">Pointer to a [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structure that stores user callback data.</span></span>

</dd> <dt>

<span data-ttu-id="00ca0-126">*ppAnimationSet* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="00ca0-126">*ppAnimationSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00ca0-127">類型： **[ **LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="00ca0-127">Type: **[**LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***</span></span>

<span data-ttu-id="00ca0-128">[**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md)主要框架動畫集合介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="00ca0-128">Address of a pointer to the [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) key framed animation set interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00ca0-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="00ca0-129">Return value</span></span>

<span data-ttu-id="00ca0-130">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="00ca0-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="00ca0-131">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="00ca0-131">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="00ca0-132">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="00ca0-132">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="00ca0-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="00ca0-133">Requirements</span></span>



| <span data-ttu-id="00ca0-134">需求</span><span class="sxs-lookup"><span data-stu-id="00ca0-134">Requirement</span></span> | <span data-ttu-id="00ca0-135">值</span><span class="sxs-lookup"><span data-stu-id="00ca0-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00ca0-136">標頭</span><span class="sxs-lookup"><span data-stu-id="00ca0-136">Header</span></span><br/>  | <dl> <span data-ttu-id="00ca0-137"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="00ca0-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="00ca0-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="00ca0-138">Library</span></span><br/> | <dl> <span data-ttu-id="00ca0-139"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="00ca0-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="00ca0-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00ca0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00ca0-141">動畫函數</span><span class="sxs-lookup"><span data-stu-id="00ca0-141">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
