---
description: 計算目前的光源投射到球面調和 (SH) 基礎向量（代表指定位置的事件 radiance）。
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: 'ID3DXPRTEngine：： ComputeVolumeSamplesDirectSH 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 757e227907eab73848f43b2b8e2f40f9b4b1071b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991492"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a><span data-ttu-id="e32cd-103">ID3DXPRTEngine：： ComputeVolumeSamplesDirectSH 方法</span><span class="sxs-lookup"><span data-stu-id="e32cd-103">ID3DXPRTEngine::ComputeVolumeSamplesDirectSH method</span></span>

<span data-ttu-id="e32cd-104">計算目前的光源投射到球面調和 (SH) 基礎向量（代表指定位置的事件 radiance）。</span><span class="sxs-lookup"><span data-stu-id="e32cd-104">Computes a projection of distant lighting into spherical harmonic (SH) basis vectors that represent incident radiance at specified locations.</span></span>

## <a name="syntax"></a><span data-ttu-id="e32cd-105">語法</span><span class="sxs-lookup"><span data-stu-id="e32cd-105">Syntax</span></span>


```C++
HRESULT ComputeVolumeSamplesDirectSH(
  [in]            UINT            OrderIn,
  [in]            UINT            OrderOut,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="e32cd-106">參數</span><span class="sxs-lookup"><span data-stu-id="e32cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e32cd-107">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e32cd-107">*OrderIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e32cd-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e32cd-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e32cd-109">距離光線的 SH 標記法的順序。</span><span class="sxs-lookup"><span data-stu-id="e32cd-109">Order of the SH representation of distant lighting.</span></span> <span data-ttu-id="e32cd-110">必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="e32cd-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="e32cd-111">評估的程度是訂單-1。</span><span class="sxs-lookup"><span data-stu-id="e32cd-111">The degree of the evaluation is OrderIn - 1.</span></span>

</dd> <dt>

<span data-ttu-id="e32cd-112">*OrderOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e32cd-112">*OrderOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e32cd-113">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e32cd-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e32cd-114">區域光源的 SH 標記法的順序。</span><span class="sxs-lookup"><span data-stu-id="e32cd-114">Order of the SH representation of local lighting.</span></span> <span data-ttu-id="e32cd-115">必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="e32cd-115">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="e32cd-116">評估的程度是 OrderOut-1。</span><span class="sxs-lookup"><span data-stu-id="e32cd-116">The degree of the evaluation is OrderOut - 1.</span></span>

</dd> <dt>

<span data-ttu-id="e32cd-117">*NumVolSamples.xml* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e32cd-117">*NumVolSamples.xml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e32cd-118">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e32cd-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e32cd-119">範例位置的數目。</span><span class="sxs-lookup"><span data-stu-id="e32cd-119">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="e32cd-120">*pSampleLocs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e32cd-120">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e32cd-121">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e32cd-121">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e32cd-122">每個範例的位置。</span><span class="sxs-lookup"><span data-stu-id="e32cd-122">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="e32cd-123">*pDataOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="e32cd-123">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e32cd-124">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="e32cd-124">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="e32cd-125">輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，此物件會將最遠的光源投射到 SH 基礎向量中。</span><span class="sxs-lookup"><span data-stu-id="e32cd-125">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that projects the distant lighting into SH basis vectors.</span></span> <span data-ttu-id="e32cd-126">這個緩衝區必須有配置給模擬的適當顏色通道數目。</span><span class="sxs-lookup"><span data-stu-id="e32cd-126">This buffer must have the proper number of color channels allocated for the simulation.</span></span> <span data-ttu-id="e32cd-127">這個方法會 \* 在每個範例位置的每個通道產生訂單² OrderOut "²純量。</span><span class="sxs-lookup"><span data-stu-id="e32cd-127">This method generates OrderIn² \* OrderOut"² scalars per channel at each sample location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e32cd-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="e32cd-128">Return value</span></span>

<span data-ttu-id="e32cd-129">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e32cd-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e32cd-130">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="e32cd-130">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e32cd-131">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="e32cd-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e32cd-132">備註</span><span class="sxs-lookup"><span data-stu-id="e32cd-132">Remarks</span></span>

<span data-ttu-id="e32cd-133">這個方法會計算距離來源的光線如何抵達 pSampleLocs 所指定空間中的每個點。</span><span class="sxs-lookup"><span data-stu-id="e32cd-133">This method computes how light from a distant source arrives at each point in space specified by pSampleLocs.</span></span> <span data-ttu-id="e32cd-134">SH 係數代表來源 radiance 到傳輸事件 radiance 的每個 pSampleLocs 點的對應。</span><span class="sxs-lookup"><span data-stu-id="e32cd-134">The SH coefficients represent the mapping, at each pSampleLocs point, of source radiance to transferred incident radiance.</span></span>

<span data-ttu-id="e32cd-135">若要成功使用此方法，您必須在 [**ID3DXPRTEngine：： SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); 中以 UseSphere = **TRUE** 和 UseCosine = **FALSE** 的球體設定取樣否則，這個方法會傳回 D3DERR INVALIDCALL 的錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e32cd-135">To use this method successfully, you must set sampling over a sphere with UseSphere = **TRUE** and UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); otherwise, this method will return an error with D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e32cd-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="e32cd-136">Requirements</span></span>



| <span data-ttu-id="e32cd-137">需求</span><span class="sxs-lookup"><span data-stu-id="e32cd-137">Requirement</span></span> | <span data-ttu-id="e32cd-138">值</span><span class="sxs-lookup"><span data-stu-id="e32cd-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e32cd-139">標頭</span><span class="sxs-lookup"><span data-stu-id="e32cd-139">Header</span></span><br/>  | <dl> <span data-ttu-id="e32cd-140"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="e32cd-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e32cd-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="e32cd-141">Library</span></span><br/> | <dl> <span data-ttu-id="e32cd-142"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e32cd-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e32cd-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e32cd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e32cd-144">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="e32cd-144">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="e32cd-145">**ID3DXPRTEngine::ComputeVolumeSamples**</span><span class="sxs-lookup"><span data-stu-id="e32cd-145">**ID3DXPRTEngine::ComputeVolumeSamples**</span></span>](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
