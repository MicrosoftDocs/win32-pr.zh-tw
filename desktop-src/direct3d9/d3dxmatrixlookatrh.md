---
description: D3DXMatrixLookAtRH 函式 (D3dx9math) -建立右手向的查詢矩陣。
ms.assetid: 10198bb9-a77e-4482-be6e-cc5f76eff30b
title: 'D3DXMatrixLookAtRH 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44b3a738de31edf373deb65ea9991e1e1502f47c
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335602"
---
# <a name="d3dxmatrixlookatrh-function-d3dx9mathh"></a><span data-ttu-id="dae79-103">D3DXMatrixLookAtRH 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="dae79-103">D3DXMatrixLookAtRH function (D3dx9math.h)</span></span>

<span data-ttu-id="dae79-104">建立右手向的外觀矩陣。</span><span class="sxs-lookup"><span data-stu-id="dae79-104">Builds a right-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="dae79-105">語法</span><span class="sxs-lookup"><span data-stu-id="dae79-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="dae79-106">參數</span><span class="sxs-lookup"><span data-stu-id="dae79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dae79-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="dae79-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dae79-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="dae79-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="dae79-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="dae79-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="dae79-110">*pEye* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dae79-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dae79-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="dae79-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="dae79-112">定義眼睛的 [**D3DXVECTOR3**](d3dxvector3.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="dae79-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="dae79-113">此值用於轉譯中。</span><span class="sxs-lookup"><span data-stu-id="dae79-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="dae79-114">*pAt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dae79-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dae79-115">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="dae79-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="dae79-116">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，該結構定義相機查看目標。</span><span class="sxs-lookup"><span data-stu-id="dae79-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="dae79-117">*pUp* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dae79-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dae79-118">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="dae79-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="dae79-119">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，該結構定義目前的世界，通常是 \[ 0、1、0 \] 。</span><span class="sxs-lookup"><span data-stu-id="dae79-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dae79-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="dae79-120">Return value</span></span>

<span data-ttu-id="dae79-121">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="dae79-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="dae79-122">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是右手向的外觀矩陣。</span><span class="sxs-lookup"><span data-stu-id="dae79-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="dae79-123">備註</span><span class="sxs-lookup"><span data-stu-id="dae79-123">Remarks</span></span>

<span data-ttu-id="dae79-124">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="dae79-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="dae79-125">如此一來， **D3DXMatrixLookAtRH** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="dae79-125">In this way, the **D3DXMatrixLookAtRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="dae79-126">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="dae79-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x            yaxis.x            zaxis.x           0
 xaxis.y            yaxis.y            zaxis.y           0
 xaxis.z            yaxis.z            zaxis.z           0
 -dot(xaxis, eye)   -dot(yaxis, eye)   -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="dae79-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="dae79-127">Requirements</span></span>



| <span data-ttu-id="dae79-128">需求</span><span class="sxs-lookup"><span data-stu-id="dae79-128">Requirement</span></span> | <span data-ttu-id="dae79-129">值</span><span class="sxs-lookup"><span data-stu-id="dae79-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dae79-130">標頭</span><span class="sxs-lookup"><span data-stu-id="dae79-130">Header</span></span><br/>  | <dl> <span data-ttu-id="dae79-131"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="dae79-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="dae79-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="dae79-132">Library</span></span><br/> | <dl> <span data-ttu-id="dae79-133"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dae79-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dae79-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dae79-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae79-135">數學函數</span><span class="sxs-lookup"><span data-stu-id="dae79-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="dae79-136">**D3DXMatrixLookAtLH**</span><span class="sxs-lookup"><span data-stu-id="dae79-136">**D3DXMatrixLookAtLH**</span></span>](d3dxmatrixlookatlh.md)
</dt> </dl>

 

 




