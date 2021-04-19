---
description: 計算上一個光源的投射投射到球面調和 (SH) 基礎向量（代表指定位置的事件 radiance）。
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: 'ID3DXPRTEngine：： ComputeVolumeSamples 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamples
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd77fff723f0cf7e3dc2a52be6a40ff6f0d71fe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982044"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a><span data-ttu-id="a91d0-103">ID3DXPRTEngine：： ComputeVolumeSamples 方法</span><span class="sxs-lookup"><span data-stu-id="a91d0-103">ID3DXPRTEngine::ComputeVolumeSamples method</span></span>

<span data-ttu-id="a91d0-104">計算上一個光源的投射投射到球面調和 (SH) 基礎向量（代表指定位置的事件 radiance）。</span><span class="sxs-lookup"><span data-stu-id="a91d0-104">Computes a projection of the direct lighting from the previous light bounce into spherical harmonic (SH) basis vectors that represent incident radiance at specified locations.</span></span>

## <a name="syntax"></a><span data-ttu-id="a91d0-105">語法</span><span class="sxs-lookup"><span data-stu-id="a91d0-105">Syntax</span></span>


```C++
HRESULT ComputeVolumeSamples(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            Order,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="a91d0-106">參數</span><span class="sxs-lookup"><span data-stu-id="a91d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a91d0-107">*pSurfDataIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a91d0-107">*pSurfDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a91d0-108">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="a91d0-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="a91d0-109">輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件代表前一個光線彈跳的3d 物件。</span><span class="sxs-lookup"><span data-stu-id="a91d0-109">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span>

</dd> <dt>

<span data-ttu-id="a91d0-110">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a91d0-110">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a91d0-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a91d0-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a91d0-112">SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="a91d0-112">Order of the SH evaluation.</span></span> <span data-ttu-id="a91d0-113">必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="a91d0-113">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="a91d0-114">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="a91d0-114">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="a91d0-115">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="a91d0-115">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="a91d0-116">*NumVolSamples.xml* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a91d0-116">*NumVolSamples.xml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a91d0-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a91d0-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a91d0-118">範例位置的數目。</span><span class="sxs-lookup"><span data-stu-id="a91d0-118">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="a91d0-119">*pSampleLocs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a91d0-119">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a91d0-120">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a91d0-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a91d0-121">每個範例的位置。</span><span class="sxs-lookup"><span data-stu-id="a91d0-121">Position for each sample.</span></span> <span data-ttu-id="a91d0-122">如果 pSampleLocs 為 **Null**，則 ComputeVolumeSamples 會在每個網格頂點計算傳輸矩陣。</span><span class="sxs-lookup"><span data-stu-id="a91d0-122">If pSampleLocs is **NULL**, ComputeVolumeSamples will compute transfer matrices at every mesh vertex.</span></span> <span data-ttu-id="a91d0-123">但是，如果 pSampleLocs 不是 **Null**，您就必須在球體 (set UseSphere = **TRUE** and UseCosine = **FALSE** 的 [**ID3DXPRTEngine：： SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)) ;否則，ComputeVolumeSamples 會傳回 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="a91d0-123">However, if pSampleLocs is not **NULL**, you must sample over a sphere (set UseSphere = **TRUE** and UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); otherwise, ComputeVolumeSamples will return D3DERR\_INVALIDCALL.</span></span>

</dd> <dt>

<span data-ttu-id="a91d0-124">*pDataOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="a91d0-124">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a91d0-125">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="a91d0-125">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="a91d0-126">輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件會投射上一個光源的直接光源，以 SH 為單位的向量。</span><span class="sxs-lookup"><span data-stu-id="a91d0-126">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that projects the direct lighting from the previous light bounce into SH basis vectors.</span></span> <span data-ttu-id="a91d0-127">這個緩衝區必須有配置給模擬的適當顏色通道數目。</span><span class="sxs-lookup"><span data-stu-id="a91d0-127">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a91d0-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="a91d0-128">Return value</span></span>

<span data-ttu-id="a91d0-129">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a91d0-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a91d0-130">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="a91d0-130">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a91d0-131">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="a91d0-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a91d0-132">備註</span><span class="sxs-lookup"><span data-stu-id="a91d0-132">Remarks</span></span>

<span data-ttu-id="a91d0-133">這個方法會計算來源 radiance 函式中的光線如何反映出表示場景 (pSurfDataIn) ，然後抵達 pSampleLocs 所指定空間中每個點的介面。</span><span class="sxs-lookup"><span data-stu-id="a91d0-133">This method computes how the light from the source radiance function is reflected off the surface that represents the scene (pSurfDataIn) and arrives at each point in space specified by pSampleLocs.</span></span> <span data-ttu-id="a91d0-134">SH 係數代表來源 radiance 到傳輸事件 radiance 的每個 pSampleLocs 點的對應。</span><span class="sxs-lookup"><span data-stu-id="a91d0-134">The SH coefficients represent the mapping, at each pSampleLocs point, of source radiance to transferred incident radiance.</span></span>

## <a name="requirements"></a><span data-ttu-id="a91d0-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="a91d0-135">Requirements</span></span>



| <span data-ttu-id="a91d0-136">需求</span><span class="sxs-lookup"><span data-stu-id="a91d0-136">Requirement</span></span> | <span data-ttu-id="a91d0-137">值</span><span class="sxs-lookup"><span data-stu-id="a91d0-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a91d0-138">標頭</span><span class="sxs-lookup"><span data-stu-id="a91d0-138">Header</span></span><br/>  | <dl> <span data-ttu-id="a91d0-139"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="a91d0-139"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a91d0-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="a91d0-140">Library</span></span><br/> | <dl> <span data-ttu-id="a91d0-141"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a91d0-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a91d0-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a91d0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a91d0-143">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="a91d0-143">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="a91d0-144">**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**</span><span class="sxs-lookup"><span data-stu-id="a91d0-144">**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**</span></span>](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
