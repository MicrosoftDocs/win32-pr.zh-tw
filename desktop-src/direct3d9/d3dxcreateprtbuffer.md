---
description: 建立預先計算 radiance 傳輸 (可由模擬器壓縮或填滿的 PRT) 緩衝區。 此函數應該用來建立每個頂點或磁片區緩衝區。
ms.assetid: f79a3691-ab5f-4404-aafd-f9635ff88e71
title: 'D3DXCreatePRTBuffer 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8107edfec436d9eda35324f6934b3f70df6a05d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992719"
---
# <a name="d3dxcreateprtbuffer-function"></a><span data-ttu-id="d4ca6-104">D3DXCreatePRTBuffer 函式</span><span class="sxs-lookup"><span data-stu-id="d4ca6-104">D3DXCreatePRTBuffer function</span></span>

<span data-ttu-id="d4ca6-105">建立預先計算 radiance 傳輸 (可由模擬器壓縮或填滿的 PRT) 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d4ca6-105">Creates a precomputed radiance transfer (PRT) buffer that can be compressed or filled by a simulator.</span></span> <span data-ttu-id="d4ca6-106">此函數應該用來建立每個頂點或磁片區緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d4ca6-106">This function should be used to create per-vertex or volume buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ca6-107">語法</span><span class="sxs-lookup"><span data-stu-id="d4ca6-107">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTBuffer(
  _In_    UINT            NumSamples,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="d4ca6-108">參數</span><span class="sxs-lookup"><span data-stu-id="d4ca6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4ca6-109">*NumSamples* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4ca6-109">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ca6-110">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4ca6-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4ca6-111">取樣 (或材質) 的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="d4ca6-111">Number of vertices (or texels) sampled.</span></span>

</dd> <dt>

<span data-ttu-id="d4ca6-112">*NumCoeffs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4ca6-112">*NumCoeffs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ca6-113">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4ca6-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4ca6-114">每個樣本位置的係數數目。</span><span class="sxs-lookup"><span data-stu-id="d4ca6-114">Number of coefficients per sample location.</span></span> <span data-ttu-id="d4ca6-115">使用球面調和 (SH) PRT 時，係數的數目應該是 Order ²，其中 Order 是 SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="d4ca6-115">When using spherical harmonic (SH) PRT, the number of coefficients should be Order², where Order is the order of the SH evaluation.</span></span> <span data-ttu-id="d4ca6-116">順序必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="d4ca6-116">Order must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="d4ca6-117">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="d4ca6-117">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="d4ca6-118">*NumChannels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d4ca6-118">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ca6-119">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4ca6-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4ca6-120">要在網格中設定的色彩通道數目。</span><span class="sxs-lookup"><span data-stu-id="d4ca6-120">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="d4ca6-121">設定為1以指定灰色材質 (R = G = B) 或3，以啟用色彩不規則效果。</span><span class="sxs-lookup"><span data-stu-id="d4ca6-121">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="d4ca6-122">*ppBuffer* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d4ca6-122">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4ca6-123">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d4ca6-123">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***</span></span>

<span data-ttu-id="d4ca6-124">所建立之 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標位址。</span><span class="sxs-lookup"><span data-stu-id="d4ca6-124">Address of a pointer to the created [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4ca6-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4ca6-125">Return value</span></span>

<span data-ttu-id="d4ca6-126">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4ca6-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4ca6-127">如果函式成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d4ca6-127">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d4ca6-128">如果函式失敗，則傳回值可以是下列其中一個： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="d4ca6-128">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4ca6-129">備註</span><span class="sxs-lookup"><span data-stu-id="d4ca6-129">Remarks</span></span>

<span data-ttu-id="d4ca6-130">建立緩衝區時，所有值都會初始化為零。</span><span class="sxs-lookup"><span data-stu-id="d4ca6-130">When the buffer is created, all values are initialized to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ca6-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4ca6-131">Requirements</span></span>



| <span data-ttu-id="d4ca6-132">需求</span><span class="sxs-lookup"><span data-stu-id="d4ca6-132">Requirement</span></span> | <span data-ttu-id="d4ca6-133">值</span><span class="sxs-lookup"><span data-stu-id="d4ca6-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ca6-134">標頭</span><span class="sxs-lookup"><span data-stu-id="d4ca6-134">Header</span></span><br/>  | <dl> <span data-ttu-id="d4ca6-135"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4ca6-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d4ca6-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="d4ca6-136">Library</span></span><br/> | <dl> <span data-ttu-id="d4ca6-137"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4ca6-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4ca6-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4ca6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ca6-139">預先計算 Radiance 傳送函式</span><span class="sxs-lookup"><span data-stu-id="d4ca6-139">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="d4ca6-140">**D3DXCreatePRTBufferTex**</span><span class="sxs-lookup"><span data-stu-id="d4ca6-140">**D3DXCreatePRTBufferTex**</span></span>](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
