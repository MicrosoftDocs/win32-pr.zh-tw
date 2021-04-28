---
description: D3DXComputeBoundingBox 函式 (D3DX10math) -計算座標軸導向的周框方塊。
ms.assetid: 1b8f328c-2fe1-462e-b464-c8dd9dc03e67
title: 'D3DXComputeBoundingBox 函式 (D3DX10math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingBox
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2a12e7e302fb36ffb8856e6402f110e01bb2afb2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103526"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a><span data-ttu-id="69e91-103">D3DXComputeBoundingBox 函式 (D3DX10math) </span><span class="sxs-lookup"><span data-stu-id="69e91-103">D3DXComputeBoundingBox function (D3DX10math.h)</span></span>

<span data-ttu-id="69e91-104">計算座標軸導向的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="69e91-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="69e91-105">語法</span><span class="sxs-lookup"><span data-stu-id="69e91-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="69e91-106">參數</span><span class="sxs-lookup"><span data-stu-id="69e91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69e91-107">*pFirstPosition* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69e91-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69e91-108">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="69e91-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="69e91-109">第一個位置的指標。</span><span class="sxs-lookup"><span data-stu-id="69e91-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="69e91-110">*NumVertices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69e91-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69e91-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69e91-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69e91-112">頂點數目。</span><span class="sxs-lookup"><span data-stu-id="69e91-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="69e91-113">*dwStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69e91-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69e91-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69e91-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69e91-115">頂點之間的計數或位元組數目。</span><span class="sxs-lookup"><span data-stu-id="69e91-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="69e91-116">*pMin* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="69e91-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69e91-117">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="69e91-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="69e91-118">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，描述周框方塊的傳回左下角。</span><span class="sxs-lookup"><span data-stu-id="69e91-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span>

</dd> <dt>

<span data-ttu-id="69e91-119">*pMax* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="69e91-119">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69e91-120">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="69e91-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="69e91-121">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，描述周框方塊的右上角。</span><span class="sxs-lookup"><span data-stu-id="69e91-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69e91-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="69e91-122">Return value</span></span>

<span data-ttu-id="69e91-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69e91-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69e91-124">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="69e91-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="69e91-125">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="69e91-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="69e91-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="69e91-126">Requirements</span></span>



| <span data-ttu-id="69e91-127">需求</span><span class="sxs-lookup"><span data-stu-id="69e91-127">Requirement</span></span> | <span data-ttu-id="69e91-128">值</span><span class="sxs-lookup"><span data-stu-id="69e91-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69e91-129">標頭</span><span class="sxs-lookup"><span data-stu-id="69e91-129">Header</span></span><br/>  | <dl> <span data-ttu-id="69e91-130"><dt>D3DX10math。h</dt></span><span class="sxs-lookup"><span data-stu-id="69e91-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="69e91-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="69e91-131">Library</span></span><br/> | <dl> <span data-ttu-id="69e91-132"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="69e91-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="69e91-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69e91-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69e91-134">網格函數</span><span class="sxs-lookup"><span data-stu-id="69e91-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
