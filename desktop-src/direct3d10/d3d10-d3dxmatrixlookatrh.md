---
description: 建立右手向的外觀矩陣。
ms.assetid: 98c8932f-f179-42ed-a361-a89065b71876
title: 'D3DXMatrixLookAtRH 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 28c2ad0cc7eb8a3ba98aacadc764bc277a1fdad0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035392"
---
# <a name="d3dxmatrixlookatrh-function-d3dx10mathh"></a><span data-ttu-id="ef30a-103">D3DXMatrixLookAtRH 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="ef30a-103">D3DXMatrixLookAtRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="ef30a-104">建立右手向的外觀矩陣。</span><span class="sxs-lookup"><span data-stu-id="ef30a-104">Builds a right-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef30a-105">語法</span><span class="sxs-lookup"><span data-stu-id="ef30a-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="ef30a-106">參數</span><span class="sxs-lookup"><span data-stu-id="ef30a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef30a-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="ef30a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef30a-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ef30a-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ef30a-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="ef30a-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ef30a-110">*pEye* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef30a-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef30a-111">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ef30a-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ef30a-112">定義眼睛點之 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="ef30a-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that defines the eye point.</span></span> <span data-ttu-id="ef30a-113">此值用於轉譯中。</span><span class="sxs-lookup"><span data-stu-id="ef30a-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="ef30a-114">*pAt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef30a-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef30a-115">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ef30a-115">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ef30a-116">D3DXVECTOR3 結構的指標，該結構定義相機查看目標。</span><span class="sxs-lookup"><span data-stu-id="ef30a-116">Pointer to the D3DXVECTOR3 structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="ef30a-117">*pUp* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef30a-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef30a-118">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ef30a-118">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="ef30a-119">D3DXVECTOR3 結構的指標，該結構定義目前的世界，通常是 \[ 0、1、0 \] 。</span><span class="sxs-lookup"><span data-stu-id="ef30a-119">Pointer to the D3DXVECTOR3 structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef30a-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef30a-120">Return value</span></span>

<span data-ttu-id="ef30a-121">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="ef30a-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ef30a-122">D3DXMATRIX 結構的指標，此結構是右手向的外觀矩陣。</span><span class="sxs-lookup"><span data-stu-id="ef30a-122">Pointer to a D3DXMATRIX structure that is a right-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef30a-123">備註</span><span class="sxs-lookup"><span data-stu-id="ef30a-123">Remarks</span></span>

<span data-ttu-id="ef30a-124">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="ef30a-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="ef30a-125">如此一來，D3DXMatrixLookAtRH 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="ef30a-125">In this way, the D3DXMatrixLookAtRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="ef30a-126">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="ef30a-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 -xaxis.x           yaxis.x           -zaxis.x          0
 -xaxis.y           yaxis.y           -zaxis.y          0
 -xaxis.z           yaxis.z           -zaxis.z          0
dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="ef30a-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef30a-127">Requirements</span></span>



| <span data-ttu-id="ef30a-128">需求</span><span class="sxs-lookup"><span data-stu-id="ef30a-128">Requirement</span></span> | <span data-ttu-id="ef30a-129">值</span><span class="sxs-lookup"><span data-stu-id="ef30a-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef30a-130">標頭</span><span class="sxs-lookup"><span data-stu-id="ef30a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="ef30a-131"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="ef30a-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="ef30a-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="ef30a-132">Library</span></span><br/> | <dl> <span data-ttu-id="ef30a-133"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef30a-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ef30a-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef30a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef30a-135">數學函數</span><span class="sxs-lookup"><span data-stu-id="ef30a-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
