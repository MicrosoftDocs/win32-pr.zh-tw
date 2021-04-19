---
description: 決定兩個3D 向量的交叉乘積。
ms.assetid: c9623f35-c8fc-4fbe-87b6-0e5bb8ebd5e8
title: 'D3DXVec3Cross 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Cross
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ba0d8a80690f43d5f8e9f6df55aa3b2e0db23dc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988182"
---
# <a name="d3dxvec3cross-function"></a><span data-ttu-id="6c722-103">D3DXVec3Cross 函式</span><span class="sxs-lookup"><span data-stu-id="6c722-103">D3DXVec3Cross function</span></span>

<span data-ttu-id="6c722-104">決定兩個3D 向量的交叉乘積。</span><span class="sxs-lookup"><span data-stu-id="6c722-104">Determines the cross-product of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c722-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c722-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Cross(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="6c722-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c722-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c722-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="6c722-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c722-108">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c722-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6c722-109">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="6c722-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6c722-110">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c722-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c722-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6c722-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6c722-112">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6c722-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6c722-113">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c722-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c722-114">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6c722-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6c722-115">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6c722-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c722-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c722-116">Return value</span></span>

<span data-ttu-id="6c722-117">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c722-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6c722-118">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，這是兩個3d 向量的交叉乘積。</span><span class="sxs-lookup"><span data-stu-id="6c722-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the cross product of two 3D vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c722-119">備註</span><span class="sxs-lookup"><span data-stu-id="6c722-119">Remarks</span></span>

<span data-ttu-id="6c722-120">此函數會使用下列程式碼來決定交叉乘積。</span><span class="sxs-lookup"><span data-stu-id="6c722-120">This function determines the cross-product with the following code.</span></span>


```
D3DXVECTOR3 v;
    
v.x = pV1->y * pV2->z - pV1->z * pV2->y;
v.y = pV1->z * pV2->x - pV1->x * pV2->z;
v.z = pV1->x * pV2->y - pV1->y * pV2->x;
    
*pOut = v;
```



<span data-ttu-id="6c722-121">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="6c722-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6c722-122">如此一來， **D3DXVec3Cross** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="6c722-122">In this way, the **D3DXVec3Cross** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c722-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c722-123">Requirements</span></span>



| <span data-ttu-id="6c722-124">需求</span><span class="sxs-lookup"><span data-stu-id="6c722-124">Requirement</span></span> | <span data-ttu-id="6c722-125">值</span><span class="sxs-lookup"><span data-stu-id="6c722-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c722-126">標頭</span><span class="sxs-lookup"><span data-stu-id="6c722-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6c722-127"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c722-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6c722-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="6c722-128">Library</span></span><br/> | <dl> <span data-ttu-id="6c722-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c722-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6c722-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c722-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c722-131">數學函數</span><span class="sxs-lookup"><span data-stu-id="6c722-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6c722-132">**D3DXVec3Dot**</span><span class="sxs-lookup"><span data-stu-id="6c722-132">**D3DXVec3Dot**</span></span>](d3dxvec3dot.md)
</dt> </dl>

 

 




