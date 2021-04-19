---
description: 建立將幾何壓平合併成平面的矩陣。
ms.assetid: 8f283ff9-c879-476c-8057-f4fe77a7a9e7
title: 'D3DXMatrixShadow 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixShadow
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6bf1639adb7364536cce5c0dead9ef58ae10bea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982009"
---
# <a name="d3dxmatrixshadow-function-d3dx9mathh"></a><span data-ttu-id="f8ff0-103">D3DXMatrixShadow 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="f8ff0-103">D3DXMatrixShadow function (D3dx9math.h)</span></span>

<span data-ttu-id="f8ff0-104">建立將幾何壓平合併成平面的矩陣。</span><span class="sxs-lookup"><span data-stu-id="f8ff0-104">Builds a matrix that flattens geometry into a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ff0-105">語法</span><span class="sxs-lookup"><span data-stu-id="f8ff0-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixShadow(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR4 *pLight,
  _In_    const D3DXPLANE   *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="f8ff0-106">參數</span><span class="sxs-lookup"><span data-stu-id="f8ff0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8ff0-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f8ff0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ff0-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8ff0-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f8ff0-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="f8ff0-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f8ff0-110">*pLight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8ff0-110">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ff0-111">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8ff0-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="f8ff0-112">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，描述光源的位置。</span><span class="sxs-lookup"><span data-stu-id="f8ff0-112">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure describing the light's position.</span></span>

</dd> <dt>

<span data-ttu-id="f8ff0-113">*pPlane* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8ff0-113">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8ff0-114">Type： **Const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8ff0-114">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="f8ff0-115">來源 [**D3DXPLANE**](d3dxplane.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f8ff0-115">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8ff0-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8ff0-116">Return value</span></span>

<span data-ttu-id="f8ff0-117">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8ff0-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f8ff0-118">將幾何壓平合併成平面的 [**D3DXMATRIX**](d3dxmatrix.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="f8ff0-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that flattens geometry into a plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8ff0-119">備註</span><span class="sxs-lookup"><span data-stu-id="f8ff0-119">Remarks</span></span>

<span data-ttu-id="f8ff0-120">**D3DXMatrixShadow** 函式會將幾何簡維化為平面，就像從燈光轉換陰影一樣。</span><span class="sxs-lookup"><span data-stu-id="f8ff0-120">The **D3DXMatrixShadow** function flattens geometry into a plane, as if casting a shadow from a light.</span></span>

<span data-ttu-id="f8ff0-121">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="f8ff0-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f8ff0-122">如此一來， **D3DXMatrixShadow** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="f8ff0-122">In this way, the **D3DXMatrixShadow** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f8ff0-123">此函數會使用下列公式來計算傳回的矩陣。</span><span class="sxs-lookup"><span data-stu-id="f8ff0-123">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
L = Light;
d = -dot(P, L)
    
P.a * L.x + d  P.a * L.y      P.a * L.z      P.a * L.w  
P.b * L.x      P.b * L.y + d  P.b * L.z      P.b * L.w  
P.c * L.x      P.c * L.y      P.c * L.z + d  P.c * L.w  
P.d * L.x      P.d * L.y      P.d * L.z      P.d * L.w + d
```



<span data-ttu-id="f8ff0-124">如果光線的 w 元件為0，從原點到燈光的光線代表方向光線。</span><span class="sxs-lookup"><span data-stu-id="f8ff0-124">If the light's w-component is 0, the ray from the origin to the light represents a directional light.</span></span> <span data-ttu-id="f8ff0-125">如果是1，則光線是點燈。</span><span class="sxs-lookup"><span data-stu-id="f8ff0-125">If it is 1, the light is a point light.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ff0-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8ff0-126">Requirements</span></span>



| <span data-ttu-id="f8ff0-127">需求</span><span class="sxs-lookup"><span data-stu-id="f8ff0-127">Requirement</span></span> | <span data-ttu-id="f8ff0-128">值</span><span class="sxs-lookup"><span data-stu-id="f8ff0-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ff0-129">標頭</span><span class="sxs-lookup"><span data-stu-id="f8ff0-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f8ff0-130"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="f8ff0-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f8ff0-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="f8ff0-131">Library</span></span><br/> | <dl> <span data-ttu-id="f8ff0-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8ff0-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8ff0-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8ff0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ff0-134">數學函數</span><span class="sxs-lookup"><span data-stu-id="f8ff0-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




