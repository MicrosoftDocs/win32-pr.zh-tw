---
description: 依指定的矩陣轉換3D 向量，將結果投射回 w = 1。
ms.assetid: 4075b067-1e64-46c9-be73-5fa765c9cb9d
title: 'D3DXVec3TransformCoord 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4bcf1a78f9da4cf5fb2a5f67360a1659182c7ffb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323360"
---
# <a name="d3dxvec3transformcoord-function-d3dx9mathh"></a><span data-ttu-id="061fd-103">D3DXVec3TransformCoord 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="061fd-103">D3DXVec3TransformCoord function (D3dx9math.h)</span></span>

<span data-ttu-id="061fd-104">依指定的矩陣轉換3D 向量，將結果投射回 w = 1。</span><span class="sxs-lookup"><span data-stu-id="061fd-104">Transforms a 3D vector by a given matrix, projecting the result back into w = 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="061fd-105">語法</span><span class="sxs-lookup"><span data-stu-id="061fd-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformCoord(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="061fd-106">參數</span><span class="sxs-lookup"><span data-stu-id="061fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="061fd-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="061fd-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="061fd-108">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="061fd-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="061fd-109">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="061fd-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="061fd-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="061fd-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="061fd-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="061fd-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="061fd-112">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="061fd-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="061fd-113">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="061fd-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="061fd-114">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="061fd-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="061fd-115">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="061fd-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="061fd-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="061fd-116">Return value</span></span>

<span data-ttu-id="061fd-117">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="061fd-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="061fd-118">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是已轉換的向量。</span><span class="sxs-lookup"><span data-stu-id="061fd-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the transformed vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="061fd-119">備註</span><span class="sxs-lookup"><span data-stu-id="061fd-119">Remarks</span></span>

<span data-ttu-id="061fd-120">此函式會將向量、 *pV* (x、y、z、1) ，由矩陣 *pM* 轉換，然後將結果投射回 w = 1。</span><span class="sxs-lookup"><span data-stu-id="061fd-120">This function transforms the vector, *pV* (x, y, z, 1), by the matrix, *pM*, projecting the result back into w=1.</span></span>

<span data-ttu-id="061fd-121">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="061fd-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="061fd-122">如此一來， **D3DXVec3TransformCoord** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="061fd-122">In this way, the **D3DXVec3TransformCoord** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="061fd-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="061fd-123">Requirements</span></span>



| <span data-ttu-id="061fd-124">需求</span><span class="sxs-lookup"><span data-stu-id="061fd-124">Requirement</span></span> | <span data-ttu-id="061fd-125">值</span><span class="sxs-lookup"><span data-stu-id="061fd-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="061fd-126">標頭</span><span class="sxs-lookup"><span data-stu-id="061fd-126">Header</span></span><br/>  | <dl> <span data-ttu-id="061fd-127"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="061fd-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="061fd-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="061fd-128">Library</span></span><br/> | <dl> <span data-ttu-id="061fd-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="061fd-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="061fd-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="061fd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="061fd-131">數學函數</span><span class="sxs-lookup"><span data-stu-id="061fd-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="061fd-132">**D3DXVec3Transform**</span><span class="sxs-lookup"><span data-stu-id="061fd-132">**D3DXVec3Transform**</span></span>](d3dxvec3transform.md)
</dt> <dt>

[<span data-ttu-id="061fd-133">**D3DXVec3TransformNormal**</span><span class="sxs-lookup"><span data-stu-id="061fd-133">**D3DXVec3TransformNormal**</span></span>](d3dxvec3transformnormal.md)
</dt> </dl>

 

 




