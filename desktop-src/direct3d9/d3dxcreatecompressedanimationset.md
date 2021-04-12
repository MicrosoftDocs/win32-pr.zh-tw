---
description: 建立 ID3DXCompressedAnimationSet 索引鍵框架動畫集介面，以壓縮格式儲存主要畫面格資料。
ms.assetid: c3f97d35-5654-4d85-a337-d77819ce3874
title: 'D3DXCreateCompressedAnimationSet 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCompressedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8aab23466cecf43a50a4136eb0b3d93a271dcb0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946126"
---
# <a name="d3dxcreatecompressedanimationset-function"></a><span data-ttu-id="e3b88-103">D3DXCreateCompressedAnimationSet 函式</span><span class="sxs-lookup"><span data-stu-id="e3b88-103">D3DXCreateCompressedAnimationSet function</span></span>

<span data-ttu-id="e3b88-104">建立 [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) 索引鍵框架動畫集介面，以壓縮格式儲存主要畫面格資料。</span><span class="sxs-lookup"><span data-stu-id="e3b88-104">Creates a [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) key framed animation set interface that stores key frame data in a compressed format.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b88-105">語法</span><span class="sxs-lookup"><span data-stu-id="e3b88-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCompressedAnimationSet(
  _In_        LPCSTR                       pName,
  _In_        DOUBLE                       TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE            Playback,
  _In_        LPD3DXBUFFER                 pCompressedData,
  _In_        UINT                         NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK           *pCallKeys,
  _Out_       LPD3DXCOMPRESSEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a><span data-ttu-id="e3b88-106">參數</span><span class="sxs-lookup"><span data-stu-id="e3b88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3b88-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3b88-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b88-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3b88-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3b88-109">動畫集合名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="e3b88-109">Pointer to the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="e3b88-110">*TicksPerSecond* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3b88-110">*TicksPerSecond* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b88-111">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3b88-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3b88-112">每秒經過的主要畫面格刻度數目。</span><span class="sxs-lookup"><span data-stu-id="e3b88-112">Number of key frame ticks that elapse per second.</span></span>

</dd> <dt>

<span data-ttu-id="e3b88-113">*播放* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3b88-113">*Playback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b88-114">類型： **[ **D3DXPLAYBACK \_ 類型**](./d3dxplayback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="e3b88-114">Type: **[**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md)**</span></span>

<span data-ttu-id="e3b88-115">動畫集合播放迴圈的型別。</span><span class="sxs-lookup"><span data-stu-id="e3b88-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="e3b88-116">請參閱 [**D3DXPLAYBACK \_ 類型**](./d3dxplayback-type.md)。</span><span class="sxs-lookup"><span data-stu-id="e3b88-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3b88-117">*pCompressedData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3b88-117">*pCompressedData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b88-118">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e3b88-118">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="e3b88-119">[**ID3DXBuffer**](id3dxbuffer.md)緩衝區的指標，此緩衝區會將動畫設定為壓縮的資料。</span><span class="sxs-lookup"><span data-stu-id="e3b88-119">Pointer to the [**ID3DXBuffer**](id3dxbuffer.md) buffer that stores the animation set as compressed data.</span></span>

</dd> <dt>

<span data-ttu-id="e3b88-120">*NumCallbackKeys* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3b88-120">*NumCallbackKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b88-121">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3b88-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3b88-122">回呼金鑰數目。</span><span class="sxs-lookup"><span data-stu-id="e3b88-122">Number of callback keys.</span></span>

</dd> <dt>

<span data-ttu-id="e3b88-123">*pCallKeys* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3b88-123">*pCallKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b88-124">類型： **Const [**LPD3DXKEY \_ 回呼**](d3dxkey-callback.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3b88-124">Type: **const [**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)\***</span></span>

<span data-ttu-id="e3b88-125">儲存使用者回呼資料的 [**D3DXKEY \_ 回呼**](d3dxkey-callback.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="e3b88-125">Pointer to a [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structure that stores user callback data.</span></span>

</dd> <dt>

<span data-ttu-id="e3b88-126">*ppAnimationSet* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e3b88-126">*ppAnimationSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3b88-127">類型： **[ **LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3b88-127">Type: **[**LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***</span></span>

<span data-ttu-id="e3b88-128">[**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md)介面的指標位址，此介面會以壓縮格式儲存主要框架動畫設定的資料。</span><span class="sxs-lookup"><span data-stu-id="e3b88-128">Address of a pointer to the [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) interface that stores key framed animation set data in a compressed format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3b88-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3b88-129">Return value</span></span>

<span data-ttu-id="e3b88-130">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e3b88-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e3b88-131">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e3b88-131">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e3b88-132">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="e3b88-132">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b88-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3b88-133">Requirements</span></span>



| <span data-ttu-id="e3b88-134">需求</span><span class="sxs-lookup"><span data-stu-id="e3b88-134">Requirement</span></span> | <span data-ttu-id="e3b88-135">值</span><span class="sxs-lookup"><span data-stu-id="e3b88-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b88-136">標頭</span><span class="sxs-lookup"><span data-stu-id="e3b88-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e3b88-137"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="e3b88-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e3b88-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="e3b88-138">Library</span></span><br/> | <dl> <span data-ttu-id="e3b88-139"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3b88-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e3b88-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3b88-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b88-141">動畫函數</span><span class="sxs-lookup"><span data-stu-id="e3b88-141">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
