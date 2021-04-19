---
description: 計算本地 deformable 預先計算 radiance 傳輸 (LDPRT 相對於每個樣本一般向量的) 係數，以將輸入 ID3DXPRTBuffer 資料的最小平方誤差降至最低。
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: 'ID3DXPRTEngine：： ComputeLDPRTCoeffs 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeLDPRTCoeffs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 351ecb8022e06b1a5a24abad8fa8541798d13ba0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988221"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a><span data-ttu-id="74c52-103">ID3DXPRTEngine：： ComputeLDPRTCoeffs 方法</span><span class="sxs-lookup"><span data-stu-id="74c52-103">ID3DXPRTEngine::ComputeLDPRTCoeffs method</span></span>

<span data-ttu-id="74c52-104">計算本地 deformable 預先計算 radiance 傳輸 (LDPRT 相對於每個樣本一般向量的) 係數，以將輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 資料的最小平方誤差降至最低。</span><span class="sxs-lookup"><span data-stu-id="74c52-104">Computes locally-deformable precomputed radiance transfer (LDPRT) coefficients relative to per-sample normal vectors to minimize the least-squares error with respect to input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) data.</span></span> <span data-ttu-id="74c52-105">這些係數可搭配 skinned 或轉換的一般向量使用，以在動態物件上建立全域效果的模型。</span><span class="sxs-lookup"><span data-stu-id="74c52-105">These coefficients can be used with skinned or transformed normal vectors to model global effects on dynamic objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="74c52-106">語法</span><span class="sxs-lookup"><span data-stu-id="74c52-106">Syntax</span></span>


```C++
HRESULT ComputeLDPRTCoeffs(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      UINT            Order,
  [in, out] D3DXVECTOR3     *pNormOut,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="74c52-107">參數</span><span class="sxs-lookup"><span data-stu-id="74c52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74c52-108">*pDataIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74c52-108">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74c52-109">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="74c52-109">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="74c52-110">輸入的指標 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 球面調和 (SH) 預先計算 radiance 傳輸 (PRT) 資料物件。</span><span class="sxs-lookup"><span data-stu-id="74c52-110">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) spherical harmonic (SH) precomputed radiance transfer (PRT) data object.</span></span>

</dd> <dt>

<span data-ttu-id="74c52-111">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74c52-111">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74c52-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74c52-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74c52-113">SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="74c52-113">Order of the SH evaluation.</span></span> <span data-ttu-id="74c52-114">必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="74c52-114">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="74c52-115">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="74c52-115">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="74c52-116">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="74c52-116">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="74c52-117">*pNormOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="74c52-117">*pNormOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="74c52-118">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="74c52-118">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="74c52-119">選用的向量陣列，要以最適合已優化 LDPRT 係數的著色器最佳標準向量來填滿。</span><span class="sxs-lookup"><span data-stu-id="74c52-119">Optional vector array to be filled with shader-optimal normal vectors for which LDPRT coefficients are optimized.</span></span> <span data-ttu-id="74c52-120">這個陣列的大小必須與 pDataIn 中的樣本數相同。</span><span class="sxs-lookup"><span data-stu-id="74c52-120">This array must be the same size as the number of samples in pDataIn.</span></span> <span data-ttu-id="74c52-121">如果是 **Null**，則會使用介面法線向量。</span><span class="sxs-lookup"><span data-stu-id="74c52-121">If **NULL**, surface normal vectors are used.</span></span>

</dd> <dt>

<span data-ttu-id="74c52-122">*pDataOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="74c52-122">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="74c52-123">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="74c52-123">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="74c52-124">輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件包含每個色彩通道每個樣本的順序區域調和係數。</span><span class="sxs-lookup"><span data-stu-id="74c52-124">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that contains Order zonal harmonic coefficients per color channel per sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74c52-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="74c52-125">Return value</span></span>

<span data-ttu-id="74c52-126">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74c52-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74c52-127">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="74c52-127">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="74c52-128">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="74c52-128">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="74c52-129">備註</span><span class="sxs-lookup"><span data-stu-id="74c52-129">Remarks</span></span>

<span data-ttu-id="74c52-130">您可以選擇性地使用這個方法來取得陰影一般向量的解決方案。</span><span class="sxs-lookup"><span data-stu-id="74c52-130">Solutions for shading normal vectors can optionally be obtained with this method.</span></span> <span data-ttu-id="74c52-131">這些一般向量以及 LDPRT 係數可以更精確地呈現 PRT 信號。</span><span class="sxs-lookup"><span data-stu-id="74c52-131">These normal vectors, along with the LDPRT coefficients, can more accurately represent the PRT signal.</span></span> <span data-ttu-id="74c52-132">在此情況下，係數代表一般方向的區域性諧波導向。</span><span class="sxs-lookup"><span data-stu-id="74c52-132">In this case, the coefficients represent zonal harmonics oriented in the normal direction.</span></span>

<span data-ttu-id="74c52-133">這個方法無法搭配 [**ID3DXPRTEngine：： ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) 或 [**ID3DXPRTEngine：： ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md)的結果使用。</span><span class="sxs-lookup"><span data-stu-id="74c52-133">This method cannot be used with results from [**ID3DXPRTEngine::ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) or [**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74c52-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="74c52-134">Requirements</span></span>



| <span data-ttu-id="74c52-135">需求</span><span class="sxs-lookup"><span data-stu-id="74c52-135">Requirement</span></span> | <span data-ttu-id="74c52-136">值</span><span class="sxs-lookup"><span data-stu-id="74c52-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74c52-137">標頭</span><span class="sxs-lookup"><span data-stu-id="74c52-137">Header</span></span><br/>  | <dl> <span data-ttu-id="74c52-138"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="74c52-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="74c52-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="74c52-139">Library</span></span><br/> | <dl> <span data-ttu-id="74c52-140"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="74c52-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74c52-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74c52-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74c52-142">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="74c52-142">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
