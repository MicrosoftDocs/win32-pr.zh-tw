---
description: 針對任意點 (和一般向量) 計算預先計算 radiance 傳輸 (PRT) 範例。
ms.assetid: 862a9067-5c5e-4428-86f4-ebef653411b9
title: 'ID3DXPRTEngine：： ComputeSurfSamplesBounce 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55cea3e87850273b6ea8d190422bd77afeb831f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323399"
---
# <a name="id3dxprtenginecomputesurfsamplesbounce-method"></a><span data-ttu-id="38ea7-103">ID3DXPRTEngine：： ComputeSurfSamplesBounce 方法</span><span class="sxs-lookup"><span data-stu-id="38ea7-103">ID3DXPRTEngine::ComputeSurfSamplesBounce method</span></span>

<span data-ttu-id="38ea7-104">針對任意點 (和一般向量) 計算預先計算 radiance 傳輸 (PRT) 範例。</span><span class="sxs-lookup"><span data-stu-id="38ea7-104">Computes precomputed radiance transfer (PRT) samples for an arbitrary point (and normal vector).</span></span>

## <a name="syntax"></a><span data-ttu-id="38ea7-105">語法</span><span class="sxs-lookup"><span data-stu-id="38ea7-105">Syntax</span></span>


```C++
HRESULT ComputeSurfSamplesBounce(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut,
  [in, out]       LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="38ea7-106">參數</span><span class="sxs-lookup"><span data-stu-id="38ea7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38ea7-107">*pSurfDataIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38ea7-107">*pSurfDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38ea7-108">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="38ea7-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="38ea7-109">輸入 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件表示3d 物件的來源 radiance。</span><span class="sxs-lookup"><span data-stu-id="38ea7-109">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the source radiance of the 3D object.</span></span> <span data-ttu-id="38ea7-110">此輸入緩衝區必須有配置給模擬的適當顏色通道數目。</span><span class="sxs-lookup"><span data-stu-id="38ea7-110">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="38ea7-111">*NumSamples* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38ea7-111">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38ea7-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38ea7-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38ea7-113">範例位置的數目。</span><span class="sxs-lookup"><span data-stu-id="38ea7-113">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="38ea7-114">*pSampleLocs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38ea7-114">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38ea7-115">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="38ea7-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="38ea7-116">每個範例的位置。</span><span class="sxs-lookup"><span data-stu-id="38ea7-116">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="38ea7-117">*pSampleNorms* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38ea7-117">*pSampleNorms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38ea7-118">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="38ea7-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="38ea7-119">每個範例位置的一般向量。</span><span class="sxs-lookup"><span data-stu-id="38ea7-119">Normal vector for each sample location.</span></span>

</dd> <dt>

<span data-ttu-id="38ea7-120">*pDataOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="38ea7-120">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ea7-121">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="38ea7-121">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="38ea7-122">輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件會使用球形調和 (SH) 近似值來將直接光源比重模型為點。</span><span class="sxs-lookup"><span data-stu-id="38ea7-122">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution to the point, using the spherical harmonic (SH) approximation.</span></span>

</dd> <dt>

<span data-ttu-id="38ea7-123">*pDataTotal* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="38ea7-123">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="38ea7-124">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="38ea7-124">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="38ea7-125">選擇性 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件為所有先前 pDataOut 輸出的執行總和。</span><span class="sxs-lookup"><span data-stu-id="38ea7-125">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="38ea7-126">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="38ea7-126">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38ea7-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="38ea7-127">Return value</span></span>

<span data-ttu-id="38ea7-128">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38ea7-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38ea7-129">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="38ea7-129">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="38ea7-130">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="38ea7-130">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="38ea7-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="38ea7-131">Requirements</span></span>



| <span data-ttu-id="38ea7-132">需求</span><span class="sxs-lookup"><span data-stu-id="38ea7-132">Requirement</span></span> | <span data-ttu-id="38ea7-133">值</span><span class="sxs-lookup"><span data-stu-id="38ea7-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="38ea7-134">標頭</span><span class="sxs-lookup"><span data-stu-id="38ea7-134">Header</span></span><br/>  | <dl> <span data-ttu-id="38ea7-135"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="38ea7-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="38ea7-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="38ea7-136">Library</span></span><br/> | <dl> <span data-ttu-id="38ea7-137"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="38ea7-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="38ea7-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38ea7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ea7-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="38ea7-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="38ea7-140">**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**</span><span class="sxs-lookup"><span data-stu-id="38ea7-140">**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**</span></span>](id3dxprtengine--computesurfsamplesdirectsh.md)
</dt> </dl>

 

 
