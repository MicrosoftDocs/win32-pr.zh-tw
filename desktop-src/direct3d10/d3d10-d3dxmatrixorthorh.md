---
description: D3DXMatrixOrthoRH 函式 (D3DX10Math) -建立右手的正向投射矩陣。
ms.assetid: e6673ff4-06a2-4a16-b72e-5ca69ddf2438
title: 'D3DXMatrixOrthoRH 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f1ab6069890bdffdedbd3e36caed1a93984fc2c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109146"
---
# <a name="d3dxmatrixorthorh-function-d3dx10mathh"></a><span data-ttu-id="48a59-103">D3DXMatrixOrthoRH 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="48a59-103">D3DXMatrixOrthoRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="48a59-104">建立右手的正向投射矩陣。</span><span class="sxs-lookup"><span data-stu-id="48a59-104">Builds a right-handed orthographic projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a59-105">語法</span><span class="sxs-lookup"><span data-stu-id="48a59-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="48a59-106">參數</span><span class="sxs-lookup"><span data-stu-id="48a59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a59-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="48a59-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="48a59-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="48a59-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="48a59-109">產生之 [**D3DXMATRIX**](d3d10-d3dxmatrix.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="48a59-109">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="48a59-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48a59-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48a59-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48a59-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48a59-112">視圖音量的寬度。</span><span class="sxs-lookup"><span data-stu-id="48a59-112">Width of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="48a59-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48a59-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48a59-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48a59-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48a59-115">視圖音量的高度。</span><span class="sxs-lookup"><span data-stu-id="48a59-115">Height of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="48a59-116">*zn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48a59-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48a59-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48a59-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48a59-118">視圖音量的最小 z 值。</span><span class="sxs-lookup"><span data-stu-id="48a59-118">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="48a59-119">*zf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48a59-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48a59-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48a59-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48a59-121">視圖音量的最大 z 值。</span><span class="sxs-lookup"><span data-stu-id="48a59-121">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48a59-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="48a59-122">Return value</span></span>

<span data-ttu-id="48a59-123">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="48a59-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="48a59-124">產生之 [**D3DXMATRIX**](d3d10-d3dxmatrix.md)的指標。</span><span class="sxs-lookup"><span data-stu-id="48a59-124">Pointer to the resulting [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="48a59-125">備註</span><span class="sxs-lookup"><span data-stu-id="48a59-125">Remarks</span></span>

<span data-ttu-id="48a59-126">D3DXMatrixOrthoRH 函數的所有參數都是相機空間中的距離。</span><span class="sxs-lookup"><span data-stu-id="48a59-126">All the parameters of the D3DXMatrixOrthoRH function are distances in camera space.</span></span> <span data-ttu-id="48a59-127">參數描述視圖磁片區的維度。</span><span class="sxs-lookup"><span data-stu-id="48a59-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="48a59-128">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="48a59-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="48a59-129">如此一來，D3DXMatrixOrthoRH 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="48a59-129">In this way, the D3DXMatrixOrthoRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="48a59-130">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="48a59-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a><span data-ttu-id="48a59-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="48a59-131">Requirements</span></span>



| <span data-ttu-id="48a59-132">需求</span><span class="sxs-lookup"><span data-stu-id="48a59-132">Requirement</span></span> | <span data-ttu-id="48a59-133">值</span><span class="sxs-lookup"><span data-stu-id="48a59-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48a59-134">標頭</span><span class="sxs-lookup"><span data-stu-id="48a59-134">Header</span></span><br/>  | <dl> <span data-ttu-id="48a59-135"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="48a59-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="48a59-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="48a59-136">Library</span></span><br/> | <dl> <span data-ttu-id="48a59-137"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="48a59-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="48a59-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48a59-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a59-139">數學函數</span><span class="sxs-lookup"><span data-stu-id="48a59-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
