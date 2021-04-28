---
description: D3DXComputeBoundingBox 函式 (D3DX9Mesh) -計算座標軸導向的周框方塊。
ms.assetid: 74e1b84e-1264-49eb-9172-7842af7e25e0
title: 'D3DXComputeBoundingBox 函式 (D3DX9Mesh) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39fdf4123781b84d87ec1c9d790eb5ffae058892
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115826"
---
# <a name="d3dxcomputeboundingbox-function-d3dx9meshh"></a><span data-ttu-id="5caa6-103">D3DXComputeBoundingBox 函式 (D3DX9Mesh) </span><span class="sxs-lookup"><span data-stu-id="5caa6-103">D3DXComputeBoundingBox function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="5caa6-104">計算座標軸導向的周框方塊。</span><span class="sxs-lookup"><span data-stu-id="5caa6-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="5caa6-105">語法</span><span class="sxs-lookup"><span data-stu-id="5caa6-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="5caa6-106">參數</span><span class="sxs-lookup"><span data-stu-id="5caa6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5caa6-107">*pFirstPosition* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5caa6-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5caa6-108">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="5caa6-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5caa6-109">第一個位置的指標。</span><span class="sxs-lookup"><span data-stu-id="5caa6-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="5caa6-110">*NumVertices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5caa6-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5caa6-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5caa6-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5caa6-112">頂點數目。</span><span class="sxs-lookup"><span data-stu-id="5caa6-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="5caa6-113">*dwStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5caa6-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5caa6-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5caa6-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5caa6-115">頂點之間的計數或位元組數目。</span><span class="sxs-lookup"><span data-stu-id="5caa6-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="5caa6-116">*pMin* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5caa6-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5caa6-117">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5caa6-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5caa6-118">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，描述周框方塊的傳回左下角。</span><span class="sxs-lookup"><span data-stu-id="5caa6-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span> <span data-ttu-id="5caa6-119">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="5caa6-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5caa6-120">*pMax* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5caa6-120">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5caa6-121">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="5caa6-121">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="5caa6-122">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，描述周框方塊的右上角。</span><span class="sxs-lookup"><span data-stu-id="5caa6-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span> <span data-ttu-id="5caa6-123">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="5caa6-123">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5caa6-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="5caa6-124">Return value</span></span>

<span data-ttu-id="5caa6-125">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5caa6-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5caa6-126">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="5caa6-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5caa6-127">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="5caa6-127">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5caa6-128">備註</span><span class="sxs-lookup"><span data-stu-id="5caa6-128">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5caa6-129">需求</span><span class="sxs-lookup"><span data-stu-id="5caa6-129">Requirements</span></span>



| <span data-ttu-id="5caa6-130">需求</span><span class="sxs-lookup"><span data-stu-id="5caa6-130">Requirement</span></span> | <span data-ttu-id="5caa6-131">值</span><span class="sxs-lookup"><span data-stu-id="5caa6-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5caa6-132">標頭</span><span class="sxs-lookup"><span data-stu-id="5caa6-132">Header</span></span><br/>  | <dl> <span data-ttu-id="5caa6-133"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="5caa6-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5caa6-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="5caa6-134">Library</span></span><br/> | <dl> <span data-ttu-id="5caa6-135"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5caa6-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5caa6-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5caa6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5caa6-137">網格函數</span><span class="sxs-lookup"><span data-stu-id="5caa6-137">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
