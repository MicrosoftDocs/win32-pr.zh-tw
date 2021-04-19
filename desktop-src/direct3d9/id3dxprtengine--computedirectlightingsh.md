---
description: 計算3D 物件的直接光源比重，其中來源 radiance 是以球面調和 (SH) 近似值表示。
ms.assetid: 52d614cc-578a-4f2b-ba91-70d0c4371042
title: 'ID3DXPRTEngine：： ComputeDirectLightingSH 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 01b6c3cff082c40c4df5d9bee1d997599a41965b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986552"
---
# <a name="id3dxprtenginecomputedirectlightingsh-method"></a><span data-ttu-id="3cc86-103">ID3DXPRTEngine：： ComputeDirectLightingSH 方法</span><span class="sxs-lookup"><span data-stu-id="3cc86-103">ID3DXPRTEngine::ComputeDirectLightingSH method</span></span>

<span data-ttu-id="3cc86-104">計算3D 物件的直接光源比重，其中來源 radiance 是以球面調和 (SH) 近似值表示。</span><span class="sxs-lookup"><span data-stu-id="3cc86-104">Computes the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cc86-105">語法</span><span class="sxs-lookup"><span data-stu-id="3cc86-105">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSH(
  [in]      UINT            Order,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="3cc86-106">參數</span><span class="sxs-lookup"><span data-stu-id="3cc86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cc86-107">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3cc86-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cc86-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3cc86-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3cc86-109">SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="3cc86-109">Order of the SH evaluation.</span></span> <span data-ttu-id="3cc86-110">必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="3cc86-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="3cc86-111">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="3cc86-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="3cc86-112">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="3cc86-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="3cc86-113">*pDataOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="3cc86-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cc86-114">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="3cc86-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="3cc86-115">輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件會以 SH 近似值來將直接光源比重模型。</span><span class="sxs-lookup"><span data-stu-id="3cc86-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution with the SH approximation.</span></span> <span data-ttu-id="3cc86-116">這個緩衝區必須有配置給模擬的適當顏色通道數目。</span><span class="sxs-lookup"><span data-stu-id="3cc86-116">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cc86-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="3cc86-117">Return value</span></span>

<span data-ttu-id="3cc86-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3cc86-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3cc86-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="3cc86-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3cc86-120">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="3cc86-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cc86-121">備註</span><span class="sxs-lookup"><span data-stu-id="3cc86-121">Remarks</span></span>

<span data-ttu-id="3cc86-122">輸出不會包含 >albedo，而且模擬器中只會整合連入的光線。</span><span class="sxs-lookup"><span data-stu-id="3cc86-122">The output does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="3cc86-123">藉由不乘以 >albedo，您可以使用比來源 radiance 更精細的規模來建立 >albedo 變異的模型，進而從壓縮產生更精確的結果。</span><span class="sxs-lookup"><span data-stu-id="3cc86-123">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="3cc86-124">呼叫 [**ID3DXPRTEngine：： MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) ，以將每個預先計算 radiance 傳輸 (PRT) vector 乘以 >albedo。</span><span class="sxs-lookup"><span data-stu-id="3cc86-124">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cc86-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="3cc86-125">Requirements</span></span>



| <span data-ttu-id="3cc86-126">需求</span><span class="sxs-lookup"><span data-stu-id="3cc86-126">Requirement</span></span> | <span data-ttu-id="3cc86-127">值</span><span class="sxs-lookup"><span data-stu-id="3cc86-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cc86-128">標頭</span><span class="sxs-lookup"><span data-stu-id="3cc86-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3cc86-129"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="3cc86-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3cc86-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="3cc86-130">Library</span></span><br/> | <dl> <span data-ttu-id="3cc86-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3cc86-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3cc86-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3cc86-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cc86-133">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="3cc86-133">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
