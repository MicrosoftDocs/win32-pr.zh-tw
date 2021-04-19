---
description: 建立左手向的透視圖投影矩陣
ms.assetid: 5fd8da67-ff12-42fa-b915-b50fa2680b32
title: 'D3DXMatrixPerspectiveLH 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 400967b5e4a25244c50dbd6093fa2079700ba4eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986766"
---
# <a name="d3dxmatrixperspectivelh-function-d3dx10mathh"></a><span data-ttu-id="16b55-103">D3DXMatrixPerspectiveLH 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="16b55-103">D3DXMatrixPerspectiveLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="16b55-104">建立左手向的透視圖投影矩陣</span><span class="sxs-lookup"><span data-stu-id="16b55-104">Builds a left-handed perspective projection matrix</span></span>

## <a name="syntax"></a><span data-ttu-id="16b55-105">語法</span><span class="sxs-lookup"><span data-stu-id="16b55-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="16b55-106">參數</span><span class="sxs-lookup"><span data-stu-id="16b55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16b55-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="16b55-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="16b55-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="16b55-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="16b55-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="16b55-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="16b55-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16b55-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b55-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16b55-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16b55-112">接近 view 平面的視圖音量寬度。</span><span class="sxs-lookup"><span data-stu-id="16b55-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="16b55-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16b55-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b55-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16b55-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16b55-115">接近 view 平面的視圖音量高度。</span><span class="sxs-lookup"><span data-stu-id="16b55-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="16b55-116">*zn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16b55-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b55-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16b55-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16b55-118">接近視圖平面的 Z 值。</span><span class="sxs-lookup"><span data-stu-id="16b55-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="16b55-119">*zf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16b55-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b55-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="16b55-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="16b55-121">最遠的視圖平面的 Z 值。</span><span class="sxs-lookup"><span data-stu-id="16b55-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16b55-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="16b55-122">Return value</span></span>

<span data-ttu-id="16b55-123">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="16b55-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="16b55-124">D3DXMATRIX 結構的指標，此結構是左手向的透視圖投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="16b55-124">Pointer to a D3DXMATRIX structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="16b55-125">備註</span><span class="sxs-lookup"><span data-stu-id="16b55-125">Remarks</span></span>

<span data-ttu-id="16b55-126">D3DXMatrixPerspectiveLH 函數的所有參數都是相機空間中的距離。</span><span class="sxs-lookup"><span data-stu-id="16b55-126">All the parameters of the D3DXMatrixPerspectiveLH function are distances in camera space.</span></span> <span data-ttu-id="16b55-127">參數描述視圖磁片區的維度。</span><span class="sxs-lookup"><span data-stu-id="16b55-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="16b55-128">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="16b55-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="16b55-129">如此一來，D3DXMatrixPerspectiveLH 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="16b55-129">In this way, the D3DXMatrixPerspectiveLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="16b55-130">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="16b55-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zf-zn)     1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="16b55-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="16b55-131">Requirements</span></span>



| <span data-ttu-id="16b55-132">需求</span><span class="sxs-lookup"><span data-stu-id="16b55-132">Requirement</span></span> | <span data-ttu-id="16b55-133">值</span><span class="sxs-lookup"><span data-stu-id="16b55-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16b55-134">標頭</span><span class="sxs-lookup"><span data-stu-id="16b55-134">Header</span></span><br/>  | <dl> <span data-ttu-id="16b55-135"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="16b55-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="16b55-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="16b55-136">Library</span></span><br/> | <dl> <span data-ttu-id="16b55-137"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="16b55-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="16b55-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16b55-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16b55-139">數學函數</span><span class="sxs-lookup"><span data-stu-id="16b55-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
