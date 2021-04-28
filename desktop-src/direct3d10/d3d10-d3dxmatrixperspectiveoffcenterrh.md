---
description: D3DXMatrixPerspectiveOffCenterRH 函式 (D3DX10Math) -建立自訂、右手的透視圖投影矩陣。
ms.assetid: 51509bfc-2f49-4ba7-8918-3c44d857d4b2
title: 'D3DXMatrixPerspectiveOffCenterRH 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3f80c32953dbc591d5d8bc7a95fc707e93fe384c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109036"
---
# <a name="d3dxmatrixperspectiveoffcenterrh-function-d3dx10mathh"></a><span data-ttu-id="d99a7-103">D3DXMatrixPerspectiveOffCenterRH 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="d99a7-103">D3DXMatrixPerspectiveOffCenterRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="d99a7-104">建立自訂、右手右手的透視圖投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="d99a7-104">Builds a customized, right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d99a7-105">語法</span><span class="sxs-lookup"><span data-stu-id="d99a7-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="d99a7-106">參數</span><span class="sxs-lookup"><span data-stu-id="d99a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d99a7-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d99a7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d99a7-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d99a7-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d99a7-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="d99a7-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d99a7-110">*l* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d99a7-110">*l* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99a7-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d99a7-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d99a7-112">視圖音量的最小 x 值。</span><span class="sxs-lookup"><span data-stu-id="d99a7-112">Minimum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d99a7-113">*r* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d99a7-113">*r* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99a7-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d99a7-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d99a7-115">視圖音量的最大 x 值。</span><span class="sxs-lookup"><span data-stu-id="d99a7-115">Maximum x-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d99a7-116">*b* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d99a7-116">*b* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99a7-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d99a7-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d99a7-118">視圖音量的最小 y 值。</span><span class="sxs-lookup"><span data-stu-id="d99a7-118">Minimum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d99a7-119"> \[ 中的 t\]</span><span class="sxs-lookup"><span data-stu-id="d99a7-119">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99a7-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d99a7-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d99a7-121">視圖音量的最大 y 值。</span><span class="sxs-lookup"><span data-stu-id="d99a7-121">Maximum y-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d99a7-122">*zn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d99a7-122">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99a7-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d99a7-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d99a7-124">視圖音量的最小 z 值。</span><span class="sxs-lookup"><span data-stu-id="d99a7-124">Minimum z-value of the view volume.</span></span>

</dd> <dt>

<span data-ttu-id="d99a7-125">*zf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d99a7-125">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d99a7-126">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d99a7-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d99a7-127">視圖音量的最大 z 值。</span><span class="sxs-lookup"><span data-stu-id="d99a7-127">Maximum z-value of the view volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d99a7-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="d99a7-128">Return value</span></span>

<span data-ttu-id="d99a7-129">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d99a7-129">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d99a7-130">D3DXMATRIX 結構的指標，此結構是自訂、右手右手的透視圖投影矩陣。</span><span class="sxs-lookup"><span data-stu-id="d99a7-130">Pointer to a D3DXMATRIX structure that is a customized, right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="d99a7-131">備註</span><span class="sxs-lookup"><span data-stu-id="d99a7-131">Remarks</span></span>

<span data-ttu-id="d99a7-132">D3DXMatrixPerspectiveOffCenterRH 函數的所有參數都是相機空間中的距離。</span><span class="sxs-lookup"><span data-stu-id="d99a7-132">All the parameters of the D3DXMatrixPerspectiveOffCenterRH function are distances in camera space.</span></span> <span data-ttu-id="d99a7-133">參數描述視圖磁片區的維度。</span><span class="sxs-lookup"><span data-stu-id="d99a7-133">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="d99a7-134">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="d99a7-134">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d99a7-135">如此一來，D3DXMatrixPerspectiveOffCenterRH 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="d99a7-135">In this way, the D3DXMatrixPerspectiveOffCenterRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d99a7-136">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="d99a7-136">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/(r-l)   0            0                0
0            2*zn/(t-b)   0                0
(l+r)/(r-l)  (t+b)/(t-b)  zf/(zn-zf)      -1
0            0            zn*zf/(zn-zf)    0
```



## <a name="requirements"></a><span data-ttu-id="d99a7-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="d99a7-137">Requirements</span></span>



| <span data-ttu-id="d99a7-138">需求</span><span class="sxs-lookup"><span data-stu-id="d99a7-138">Requirement</span></span> | <span data-ttu-id="d99a7-139">值</span><span class="sxs-lookup"><span data-stu-id="d99a7-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d99a7-140">標頭</span><span class="sxs-lookup"><span data-stu-id="d99a7-140">Header</span></span><br/>  | <dl> <span data-ttu-id="d99a7-141"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="d99a7-141"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d99a7-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="d99a7-142">Library</span></span><br/> | <dl> <span data-ttu-id="d99a7-143"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d99a7-143"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d99a7-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d99a7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d99a7-145">數學函數</span><span class="sxs-lookup"><span data-stu-id="d99a7-145">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
