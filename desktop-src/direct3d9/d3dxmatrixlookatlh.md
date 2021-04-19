---
description: 建立左手向的查詢矩陣。
ms.assetid: bf34d3d8-725d-4fc1-b4c8-6c98f9dac329
title: 'D3DXMatrixLookAtLH 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97fa7acdf467761bd3b3cfbc023662e9b3368b98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106984278"
---
# <a name="d3dxmatrixlookatlh-function-d3dx9mathh"></a><span data-ttu-id="2b010-103">D3DXMatrixLookAtLH 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="2b010-103">D3DXMatrixLookAtLH function (D3dx9math.h)</span></span>

<span data-ttu-id="2b010-104">建立左手向的查詢矩陣。</span><span class="sxs-lookup"><span data-stu-id="2b010-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b010-105">語法</span><span class="sxs-lookup"><span data-stu-id="2b010-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="2b010-106">參數</span><span class="sxs-lookup"><span data-stu-id="2b010-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b010-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2b010-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b010-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b010-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2b010-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="2b010-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2b010-110">*pEye* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b010-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b010-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b010-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2b010-112">定義眼睛的 [**D3DXVECTOR3**](d3dxvector3.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="2b010-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="2b010-113">此值用於轉譯中。</span><span class="sxs-lookup"><span data-stu-id="2b010-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="2b010-114">*pAt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b010-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b010-115">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b010-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2b010-116">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，該結構定義相機查看目標。</span><span class="sxs-lookup"><span data-stu-id="2b010-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="2b010-117">*pUp* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b010-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b010-118">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="2b010-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2b010-119">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，該結構定義目前的世界，通常是 \[ 0、1、0 \] 。</span><span class="sxs-lookup"><span data-stu-id="2b010-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b010-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b010-120">Return value</span></span>

<span data-ttu-id="2b010-121">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2b010-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2b010-122">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是左手向的外觀矩陣。</span><span class="sxs-lookup"><span data-stu-id="2b010-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b010-123">備註</span><span class="sxs-lookup"><span data-stu-id="2b010-123">Remarks</span></span>

<span data-ttu-id="2b010-124">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="2b010-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2b010-125">如此一來， **D3DXMatrixLookAtLH** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="2b010-125">In this way, the **D3DXMatrixLookAtLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2b010-126">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="2b010-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="2b010-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b010-127">Requirements</span></span>



| <span data-ttu-id="2b010-128">需求</span><span class="sxs-lookup"><span data-stu-id="2b010-128">Requirement</span></span> | <span data-ttu-id="2b010-129">值</span><span class="sxs-lookup"><span data-stu-id="2b010-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b010-130">標頭</span><span class="sxs-lookup"><span data-stu-id="2b010-130">Header</span></span><br/>  | <dl> <span data-ttu-id="2b010-131"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b010-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2b010-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="2b010-132">Library</span></span><br/> | <dl> <span data-ttu-id="2b010-133"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b010-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2b010-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b010-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b010-135">數學函數</span><span class="sxs-lookup"><span data-stu-id="2b010-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2b010-136">**D3DXMatrixLookAtRH**</span><span class="sxs-lookup"><span data-stu-id="2b010-136">**D3DXMatrixLookAtRH**</span></span>](d3dxmatrixlookatrh.md)
</dt> </dl>

 

 




