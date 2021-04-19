---
description: 建立預先計算 radiance 傳輸 (可由模擬器壓縮或填滿的 PRT) 緩衝區。 此函式應該用來建立每個圖元的緩衝區。
ms.assetid: 41e65674-e5e1-4df9-aab8-1530ebf85f25
title: 'D3DXCreatePRTBufferTex 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBufferTex
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e3e88073f85d281e164c002ba5180493f6217e3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999009"
---
# <a name="d3dxcreateprtbuffertex-function"></a><span data-ttu-id="d73e1-104">D3DXCreatePRTBufferTex 函式</span><span class="sxs-lookup"><span data-stu-id="d73e1-104">D3DXCreatePRTBufferTex function</span></span>

<span data-ttu-id="d73e1-105">建立預先計算 radiance 傳輸 (可由模擬器壓縮或填滿的 PRT) 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d73e1-105">Creates a precomputed radiance transfer (PRT) buffer that can be compressed or filled by a simulator.</span></span> <span data-ttu-id="d73e1-106">此函式應該用來建立每個圖元的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d73e1-106">This function should be used to create per-pixel buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d73e1-107">語法</span><span class="sxs-lookup"><span data-stu-id="d73e1-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTBufferTex(
  _In_    UINT            Width,
  _In_    UINT            Height,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="d73e1-108">參數</span><span class="sxs-lookup"><span data-stu-id="d73e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d73e1-109">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d73e1-109">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d73e1-110">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d73e1-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d73e1-111">材質的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d73e1-111">Width of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="d73e1-112">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d73e1-112">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d73e1-113">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d73e1-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d73e1-114">紋理的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d73e1-114">Height of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="d73e1-115">*NumCoeffs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d73e1-115">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d73e1-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d73e1-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d73e1-117">每個樣本位置的係數數目。</span><span class="sxs-lookup"><span data-stu-id="d73e1-117">Number of coefficients per sample location.</span></span> <span data-ttu-id="d73e1-118">使用球面調和 (SH) PRT 時，係數的數目應該是 Order ²，其中 Order 是 SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="d73e1-118">When using spherical harmonic (SH) PRT, the number of coefficients should be Order², where Order is the order of the SH evaluation.</span></span> <span data-ttu-id="d73e1-119">順序必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="d73e1-119">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="d73e1-120">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="d73e1-120">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="d73e1-121">*NumChannels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d73e1-121">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d73e1-122">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d73e1-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d73e1-123">要在網格中設定的色彩通道數目。</span><span class="sxs-lookup"><span data-stu-id="d73e1-123">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="d73e1-124">設定為1以指定灰色材質 (R = G = B) 或3，以啟用色彩不規則效果。</span><span class="sxs-lookup"><span data-stu-id="d73e1-124">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="d73e1-125">*ppBuffer* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d73e1-125">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d73e1-126">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d73e1-126">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="d73e1-127">所建立之 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標位址。</span><span class="sxs-lookup"><span data-stu-id="d73e1-127">Address of a pointer to the created [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d73e1-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="d73e1-128">Return value</span></span>

<span data-ttu-id="d73e1-129">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d73e1-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d73e1-130">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="d73e1-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d73e1-131">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="d73e1-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d73e1-132">備註</span><span class="sxs-lookup"><span data-stu-id="d73e1-132">Remarks</span></span>

<span data-ttu-id="d73e1-133">建立緩衝區時，所有值都會初始化為零。</span><span class="sxs-lookup"><span data-stu-id="d73e1-133">When the buffer is created, all values are initialized to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d73e1-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="d73e1-134">Requirements</span></span>



| <span data-ttu-id="d73e1-135">需求</span><span class="sxs-lookup"><span data-stu-id="d73e1-135">Requirement</span></span> | <span data-ttu-id="d73e1-136">值</span><span class="sxs-lookup"><span data-stu-id="d73e1-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d73e1-137">標頭</span><span class="sxs-lookup"><span data-stu-id="d73e1-137">Header</span></span><br/>  | <dl> <span data-ttu-id="d73e1-138"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="d73e1-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d73e1-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="d73e1-139">Library</span></span><br/> | <dl> <span data-ttu-id="d73e1-140"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d73e1-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d73e1-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d73e1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d73e1-142">預先計算 Radiance 傳送函式</span><span class="sxs-lookup"><span data-stu-id="d73e1-142">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="d73e1-143">**D3DXCreatePRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="d73e1-143">**D3DXCreatePRTBuffer**</span></span>](d3dxcreateprtbuffer.md)
</dt> </dl>

 

 
