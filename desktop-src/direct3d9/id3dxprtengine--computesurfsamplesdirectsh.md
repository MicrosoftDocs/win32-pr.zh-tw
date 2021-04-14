---
description: 計算，在不在網格上的任意時間點，對應來源 radiance (由球面調和表示的傳輸向量 (SH) 近似值) 結束 radiance。
ms.assetid: 44790465-440d-4426-b780-ed872fbf8efb
title: 'ID3DXPRTEngine：： ComputeSurfSamplesDirectSH 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03adb1729a8a2e771ea681ccbdd180999d3adcbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323395"
---
# <a name="id3dxprtenginecomputesurfsamplesdirectsh-method"></a><span data-ttu-id="3dbaf-103">ID3DXPRTEngine：： ComputeSurfSamplesDirectSH 方法</span><span class="sxs-lookup"><span data-stu-id="3dbaf-103">ID3DXPRTEngine::ComputeSurfSamplesDirectSH method</span></span>

<span data-ttu-id="3dbaf-104">計算，在不在網格上的任意時間點，對應來源 radiance (由球面調和表示的傳輸向量 (SH) 近似值) 結束 radiance。</span><span class="sxs-lookup"><span data-stu-id="3dbaf-104">Computes, at an arbitrary point not on a mesh, a transfer vector that maps source radiance (represented by a spherical harmonic (SH) approximation) to exit radiance.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dbaf-105">語法</span><span class="sxs-lookup"><span data-stu-id="3dbaf-105">Syntax</span></span>


```C++
HRESULT ComputeSurfSamplesDirectSH(
  [in]            UINT            SHOrder,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="3dbaf-106">參數</span><span class="sxs-lookup"><span data-stu-id="3dbaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dbaf-107">*SHOrder* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3dbaf-107">*SHOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dbaf-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3dbaf-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3dbaf-109">要使用的 SH 近似值順序。</span><span class="sxs-lookup"><span data-stu-id="3dbaf-109">Order of the SH approximation to use.</span></span>

</dd> <dt>

<span data-ttu-id="3dbaf-110">*NumSamples* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3dbaf-110">*NumSamples* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dbaf-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3dbaf-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3dbaf-112">範例位置的數目。</span><span class="sxs-lookup"><span data-stu-id="3dbaf-112">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="3dbaf-113">*pSampleLocs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3dbaf-113">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dbaf-114">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3dbaf-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3dbaf-115">每個範例的位置。</span><span class="sxs-lookup"><span data-stu-id="3dbaf-115">Position for each sample.</span></span>

</dd> <dt>

<span data-ttu-id="3dbaf-116">*pSampleNorms* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3dbaf-116">*pSampleNorms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dbaf-117">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3dbaf-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3dbaf-118">每個範例位置的一般向量。</span><span class="sxs-lookup"><span data-stu-id="3dbaf-118">Normal vector for each sample location.</span></span>

</dd> <dt>

<span data-ttu-id="3dbaf-119">*pDataOut* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="3dbaf-119">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3dbaf-120">類型： **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="3dbaf-120">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="3dbaf-121">輸出 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 物件的指標，該物件會使用 SH 近似值來將直接光源比重模型到點。</span><span class="sxs-lookup"><span data-stu-id="3dbaf-121">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution to the point, using the SH approximation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dbaf-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="3dbaf-122">Return value</span></span>

<span data-ttu-id="3dbaf-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3dbaf-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3dbaf-124">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="3dbaf-124">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3dbaf-125">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="3dbaf-125">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dbaf-126">備註</span><span class="sxs-lookup"><span data-stu-id="3dbaf-126">Remarks</span></span>

<span data-ttu-id="3dbaf-127">呼叫這個方法時，請勿使用材質緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3dbaf-127">Do not use a texture buffer when calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dbaf-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="3dbaf-128">Requirements</span></span>



| <span data-ttu-id="3dbaf-129">需求</span><span class="sxs-lookup"><span data-stu-id="3dbaf-129">Requirement</span></span> | <span data-ttu-id="3dbaf-130">值</span><span class="sxs-lookup"><span data-stu-id="3dbaf-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dbaf-131">標頭</span><span class="sxs-lookup"><span data-stu-id="3dbaf-131">Header</span></span><br/>  | <dl> <span data-ttu-id="3dbaf-132"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="3dbaf-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3dbaf-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="3dbaf-133">Library</span></span><br/> | <dl> <span data-ttu-id="3dbaf-134"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3dbaf-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3dbaf-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3dbaf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dbaf-136">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="3dbaf-136">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="3dbaf-137">**ID3DXPRTEngine::ComputeDirectLightingSH**</span><span class="sxs-lookup"><span data-stu-id="3dbaf-137">**ID3DXPRTEngine::ComputeDirectLightingSH**</span></span>](id3dxprtengine--computedirectlightingsh.md)
</dt> <dt>

[<span data-ttu-id="3dbaf-138">**ID3DXPRTEngine::ComputeSurfSamplesBounce**</span><span class="sxs-lookup"><span data-stu-id="3dbaf-138">**ID3DXPRTEngine::ComputeSurfSamplesBounce**</span></span>](id3dxprtengine--computesurfsamplesbounce.md)
</dt> </dl>

 

 
