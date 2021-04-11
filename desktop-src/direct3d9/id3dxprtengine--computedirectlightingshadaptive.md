---
description: 使用調適型取樣，計算以球面調和 (SH) 近似值表示之3D 物件的直接光源比重。
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: 'ID3DXPRTEngine：： ComputeDirectLightingSHAdaptive 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8abbcfd955fa909166b53f6e050b9aff5837508d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696860"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a><span data-ttu-id="f8de3-103">ID3DXPRTEngine：： ComputeDirectLightingSHAdaptive 方法</span><span class="sxs-lookup"><span data-stu-id="f8de3-103">ID3DXPRTEngine::ComputeDirectLightingSHAdaptive method</span></span>

<span data-ttu-id="f8de3-104">使用調適型取樣，計算以球面調和 (SH) 近似值表示之3D 物件的直接光源比重。</span><span class="sxs-lookup"><span data-stu-id="f8de3-104">Computes the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation, using adaptive sampling.</span></span> <span data-ttu-id="f8de3-105">這個方法會在網格上產生新的頂點和臉部，以更精確地近似預先計算 radiance 傳輸 (PRT) 信號。</span><span class="sxs-lookup"><span data-stu-id="f8de3-105">This method generates new vertices and faces on the mesh to more accurately approximate the precomputed radiance transfer (PRT) signal.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8de3-106">語法</span><span class="sxs-lookup"><span data-stu-id="f8de3-106">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSHAdaptive(
  [in]      UINT            Order,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="f8de3-107">參數</span><span class="sxs-lookup"><span data-stu-id="f8de3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8de3-108">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8de3-108">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8de3-109">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8de3-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8de3-110">SH 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="f8de3-110">Order of the SH evaluation.</span></span> <span data-ttu-id="f8de3-111">必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="f8de3-111">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="f8de3-112">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="f8de3-112">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="f8de3-113">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="f8de3-113">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="f8de3-114">*AdaptiveThresh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8de3-114">*AdaptiveThresh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8de3-115">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8de3-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8de3-116">用於細分網格頂點和臉部的 PRT 向量閾值。</span><span class="sxs-lookup"><span data-stu-id="f8de3-116">Threshold on the PRT vector to use for subdividing mesh vertices and faces.</span></span> <span data-ttu-id="f8de3-117">如果小於 1e-6f，則會指定值為 1e-6f 的預設值。</span><span class="sxs-lookup"><span data-stu-id="f8de3-117">If less than 1e-6f, a default value of 1e-6f is specified.</span></span>

</dd> <dt>

<span data-ttu-id="f8de3-118">*MinEdgeLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8de3-118">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8de3-119">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8de3-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8de3-120">自動調整取樣中將產生的最小臉部邊長度。</span><span class="sxs-lookup"><span data-stu-id="f8de3-120">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="f8de3-121">如果方法判斷該值太小，則會指定模型相依的值。</span><span class="sxs-lookup"><span data-stu-id="f8de3-121">If the method determines that the value is too small, a model-dependent value is specified.</span></span> <span data-ttu-id="f8de3-122">如果為零，則會指定預設值4。</span><span class="sxs-lookup"><span data-stu-id="f8de3-122">If zero, a default value of 4 is specified.</span></span>

</dd> <dt>

<span data-ttu-id="f8de3-123">*MaxSubdiv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8de3-123">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8de3-124">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8de3-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8de3-125">臉部的最大細分層級，將用於適應性取樣中。</span><span class="sxs-lookup"><span data-stu-id="f8de3-125">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span>

</dd> <dt>

<span data-ttu-id="f8de3-126">*pDataOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f8de3-126">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8de3-127">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="f8de3-127">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="f8de3-128">輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="f8de3-128">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="f8de3-129">這個緩衝區必須有配置給模擬的適當顏色通道數目。</span><span class="sxs-lookup"><span data-stu-id="f8de3-129">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8de3-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8de3-130">Return value</span></span>

<span data-ttu-id="f8de3-131">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8de3-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8de3-132">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="f8de3-132">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f8de3-133">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="f8de3-133">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8de3-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8de3-134">Requirements</span></span>



| <span data-ttu-id="f8de3-135">需求</span><span class="sxs-lookup"><span data-stu-id="f8de3-135">Requirement</span></span> | <span data-ttu-id="f8de3-136">值</span><span class="sxs-lookup"><span data-stu-id="f8de3-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8de3-137">標頭</span><span class="sxs-lookup"><span data-stu-id="f8de3-137">Header</span></span><br/>  | <dl> <span data-ttu-id="f8de3-138"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="f8de3-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f8de3-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="f8de3-139">Library</span></span><br/> | <dl> <span data-ttu-id="f8de3-140"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8de3-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8de3-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8de3-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8de3-142">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="f8de3-142">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="f8de3-143">**ID3DXPRTEngine::RobustMeshRefine**</span><span class="sxs-lookup"><span data-stu-id="f8de3-143">**ID3DXPRTEngine::RobustMeshRefine**</span></span>](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
