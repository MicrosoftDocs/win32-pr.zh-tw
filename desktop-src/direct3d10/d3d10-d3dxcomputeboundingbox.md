---
description: 計算座標軸導向的周框方塊。
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
ms.openlocfilehash: 9a93eb4a10f6c2b2fd7eda82afcc21158138a1e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999036"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a><span data-ttu-id="9d928-103">D3DXComputeBoundingBox 函式 (D3DX10math) </span><span class="sxs-lookup"><span data-stu-id="9d928-103">D3DXComputeBoundingBox function (D3DX10math.h)</span></span>

<span data-ttu-id="9d928-104">計算座標軸導向的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="9d928-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d928-105">語法</span><span class="sxs-lookup"><span data-stu-id="9d928-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="9d928-106">參數</span><span class="sxs-lookup"><span data-stu-id="9d928-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d928-107">*pFirstPosition* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9d928-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d928-108">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="9d928-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9d928-109">第一個位置的指標。</span><span class="sxs-lookup"><span data-stu-id="9d928-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="9d928-110">*NumVertices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9d928-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d928-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d928-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9d928-112">頂點數目。</span><span class="sxs-lookup"><span data-stu-id="9d928-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="9d928-113">*dwStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9d928-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d928-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d928-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9d928-115">頂點之間的計數或位元組數目。</span><span class="sxs-lookup"><span data-stu-id="9d928-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="9d928-116">*pMin* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9d928-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d928-117">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d928-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9d928-118">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，描述周框方塊的傳回左下角。</span><span class="sxs-lookup"><span data-stu-id="9d928-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span>

</dd> <dt>

<span data-ttu-id="9d928-119">*pMax* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9d928-119">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d928-120">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d928-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="9d928-121">[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，描述周框方塊的右上角。</span><span class="sxs-lookup"><span data-stu-id="9d928-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d928-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d928-122">Return value</span></span>

<span data-ttu-id="9d928-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9d928-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9d928-124">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="9d928-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9d928-125">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="9d928-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d928-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d928-126">Requirements</span></span>



| <span data-ttu-id="9d928-127">需求</span><span class="sxs-lookup"><span data-stu-id="9d928-127">Requirement</span></span> | <span data-ttu-id="9d928-128">值</span><span class="sxs-lookup"><span data-stu-id="9d928-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d928-129">標頭</span><span class="sxs-lookup"><span data-stu-id="9d928-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9d928-130"><dt>D3DX10math。h</dt></span><span class="sxs-lookup"><span data-stu-id="9d928-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="9d928-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="9d928-131">Library</span></span><br/> | <dl> <span data-ttu-id="9d928-132"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d928-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9d928-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d928-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d928-134">網格函數</span><span class="sxs-lookup"><span data-stu-id="9d928-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
