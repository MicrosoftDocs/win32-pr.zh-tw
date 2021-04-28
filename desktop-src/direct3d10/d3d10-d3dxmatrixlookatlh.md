---
description: D3DXMatrixLookAtLH 函式 (D3DX10Math) -建立左手向的查詢矩陣。
ms.assetid: 06888a97-66ef-447f-be8b-ea458ce16b4b
title: 'D3DXMatrixLookAtLH 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3590d2cbdeead9e1b9b2547b2344163b81f05d11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109166"
---
# <a name="d3dxmatrixlookatlh-function-d3dx10mathh"></a><span data-ttu-id="45d89-103">D3DXMatrixLookAtLH 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="45d89-103">D3DXMatrixLookAtLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="45d89-104">建立左手向的查詢矩陣。</span><span class="sxs-lookup"><span data-stu-id="45d89-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="45d89-105">語法</span><span class="sxs-lookup"><span data-stu-id="45d89-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="45d89-106">參數</span><span class="sxs-lookup"><span data-stu-id="45d89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45d89-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="45d89-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="45d89-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="45d89-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="45d89-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="45d89-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="45d89-110">*pEye* \[在\]</span><span class="sxs-lookup"><span data-stu-id="45d89-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45d89-111">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="45d89-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="45d89-112">定義眼睛點之 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="45d89-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that defines the eye point.</span></span> <span data-ttu-id="45d89-113">此值用於轉譯中。</span><span class="sxs-lookup"><span data-stu-id="45d89-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="45d89-114">*pAt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="45d89-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45d89-115">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="45d89-115">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="45d89-116">D3DXVECTOR3 結構的指標，該結構定義相機查看目標。</span><span class="sxs-lookup"><span data-stu-id="45d89-116">Pointer to the D3DXVECTOR3 structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="45d89-117">*pUp* \[在\]</span><span class="sxs-lookup"><span data-stu-id="45d89-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45d89-118">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="45d89-118">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="45d89-119">D3DXVECTOR3 結構的指標，該結構定義目前的世界，通常是 \[ 0、1、0 \] 。</span><span class="sxs-lookup"><span data-stu-id="45d89-119">Pointer to the D3DXVECTOR3 structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45d89-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="45d89-120">Return value</span></span>

<span data-ttu-id="45d89-121">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="45d89-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="45d89-122">D3DXMATRIX 結構的指標，此結構是左手向的外觀矩陣。</span><span class="sxs-lookup"><span data-stu-id="45d89-122">Pointer to a D3DXMATRIX structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="45d89-123">備註</span><span class="sxs-lookup"><span data-stu-id="45d89-123">Remarks</span></span>

<span data-ttu-id="45d89-124">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="45d89-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="45d89-125">如此一來，D3DXMatrixLookAtLH 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="45d89-125">In this way, the D3DXMatrixLookAtLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="45d89-126">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="45d89-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="45d89-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="45d89-127">Requirements</span></span>



| <span data-ttu-id="45d89-128">需求</span><span class="sxs-lookup"><span data-stu-id="45d89-128">Requirement</span></span> | <span data-ttu-id="45d89-129">值</span><span class="sxs-lookup"><span data-stu-id="45d89-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45d89-130">標頭</span><span class="sxs-lookup"><span data-stu-id="45d89-130">Header</span></span><br/>  | <dl> <span data-ttu-id="45d89-131"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="45d89-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="45d89-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="45d89-132">Library</span></span><br/> | <dl> <span data-ttu-id="45d89-133"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="45d89-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="45d89-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45d89-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d89-135">數學函數</span><span class="sxs-lookup"><span data-stu-id="45d89-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
