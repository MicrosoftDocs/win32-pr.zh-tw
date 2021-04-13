---
description: 設定3D 物件之間交集的最小和最大距離。
ms.assetid: da825c70-0c55-4303-b78a-a761ba037182
title: 'ID3DXPRTEngine：： SetMinMaxIntersection 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMinMaxIntersection
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68845f713289c524afc844037ca305909e5b89b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323036"
---
# <a name="id3dxprtenginesetminmaxintersection-method"></a><span data-ttu-id="9dd3b-103">ID3DXPRTEngine：： SetMinMaxIntersection 方法</span><span class="sxs-lookup"><span data-stu-id="9dd3b-103">ID3DXPRTEngine::SetMinMaxIntersection method</span></span>

<span data-ttu-id="9dd3b-104">設定3D 物件之間交集的最小和最大距離。</span><span class="sxs-lookup"><span data-stu-id="9dd3b-104">Sets the minimum and maximum distances of intersection between 3D objects.</span></span> <span data-ttu-id="9dd3b-105">這些距離值可以用來控制物件可以陰影或反映光線的最小或最大距離。</span><span class="sxs-lookup"><span data-stu-id="9dd3b-105">These distance values can be used to control the minimum or maximum distance that objects can shadow or reflect light.</span></span> <span data-ttu-id="9dd3b-106">例如，方法可以用來限制3D 模型的鄰近功能遮蔽。</span><span class="sxs-lookup"><span data-stu-id="9dd3b-106">For example, the method can be used to limit the shadowing of nearby features of a 3D model.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dd3b-107">語法</span><span class="sxs-lookup"><span data-stu-id="9dd3b-107">Syntax</span></span>


```C++
HRESULT SetMinMaxIntersection(
  [in] FLOAT fMin ,
  [in] FLOAT fMax
);
```



## <a name="parameters"></a><span data-ttu-id="9dd3b-108">參數</span><span class="sxs-lookup"><span data-stu-id="9dd3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dd3b-109">*fMin* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9dd3b-109">*fMin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dd3b-110">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9dd3b-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9dd3b-111">最小交集距離。</span><span class="sxs-lookup"><span data-stu-id="9dd3b-111">Minimum intersection distance.</span></span> <span data-ttu-id="9dd3b-112">必須是正數且小於 fMax。</span><span class="sxs-lookup"><span data-stu-id="9dd3b-112">Must be positive and less than fMax.</span></span>

</dd> <dt>

<span data-ttu-id="9dd3b-113">*fMax* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9dd3b-113">*fMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dd3b-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9dd3b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9dd3b-115">最大交集距離。</span><span class="sxs-lookup"><span data-stu-id="9dd3b-115">Maximum intersection distance.</span></span> <span data-ttu-id="9dd3b-116">如果是 0.0 f，將會使用先前的值;否則，必須大於 fMin。</span><span class="sxs-lookup"><span data-stu-id="9dd3b-116">If 0.0f, the previous value will be used; otherwise, must be greater than fMin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dd3b-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="9dd3b-117">Return value</span></span>

<span data-ttu-id="9dd3b-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9dd3b-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9dd3b-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="9dd3b-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9dd3b-120">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="9dd3b-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dd3b-121">備註</span><span class="sxs-lookup"><span data-stu-id="9dd3b-121">Remarks</span></span>

<span data-ttu-id="9dd3b-122">此方法不能用於預先計算 radiance 傳輸 (在 GPU 中執行的 PRT) 模擬。</span><span class="sxs-lookup"><span data-stu-id="9dd3b-122">This method cannot be used in precomputed radiance transfer (PRT) simulations that run in the GPU.</span></span> <span data-ttu-id="9dd3b-123">請參閱 [**ID3DXPRTEngine：： ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md)。</span><span class="sxs-lookup"><span data-stu-id="9dd3b-123">See [**ID3DXPRTEngine::ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9dd3b-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="9dd3b-124">Requirements</span></span>



| <span data-ttu-id="9dd3b-125">需求</span><span class="sxs-lookup"><span data-stu-id="9dd3b-125">Requirement</span></span> | <span data-ttu-id="9dd3b-126">值</span><span class="sxs-lookup"><span data-stu-id="9dd3b-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd3b-127">標頭</span><span class="sxs-lookup"><span data-stu-id="9dd3b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="9dd3b-128"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="9dd3b-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9dd3b-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="9dd3b-129">Library</span></span><br/> | <dl> <span data-ttu-id="9dd3b-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9dd3b-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9dd3b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9dd3b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd3b-132">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="9dd3b-132">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
