---
description: 調整3D 向量。
ms.assetid: b2483d6e-56e4-4557-a603-d59c0767774d
title: 'D3DXVec3Scale 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5357b862b9cf82e458429edea27001163eb9635
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992752"
---
# <a name="d3dxvec3scale-function"></a><span data-ttu-id="d305a-103">D3DXVec3Scale 函式</span><span class="sxs-lookup"><span data-stu-id="d305a-103">D3DXVec3Scale function</span></span>

<span data-ttu-id="d305a-104">調整3D 向量。</span><span class="sxs-lookup"><span data-stu-id="d305a-104">Scales a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="d305a-105">語法</span><span class="sxs-lookup"><span data-stu-id="d305a-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Scale(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="d305a-106">參數</span><span class="sxs-lookup"><span data-stu-id="d305a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d305a-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d305a-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d305a-108">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d305a-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d305a-109">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="d305a-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d305a-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d305a-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d305a-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d305a-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d305a-112">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d305a-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d305a-113"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="d305a-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d305a-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d305a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d305a-115">調整值。</span><span class="sxs-lookup"><span data-stu-id="d305a-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d305a-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d305a-116">Return value</span></span>

<span data-ttu-id="d305a-117">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d305a-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d305a-118">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是縮放向量。</span><span class="sxs-lookup"><span data-stu-id="d305a-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="d305a-119">備註</span><span class="sxs-lookup"><span data-stu-id="d305a-119">Remarks</span></span>

<span data-ttu-id="d305a-120">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="d305a-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="d305a-121">如此一來， **D3DXVec3Scale** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="d305a-121">In this way, the **D3DXVec3Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d305a-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d305a-122">Requirements</span></span>



| <span data-ttu-id="d305a-123">需求</span><span class="sxs-lookup"><span data-stu-id="d305a-123">Requirement</span></span> | <span data-ttu-id="d305a-124">值</span><span class="sxs-lookup"><span data-stu-id="d305a-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d305a-125">標頭</span><span class="sxs-lookup"><span data-stu-id="d305a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d305a-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="d305a-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d305a-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="d305a-127">Library</span></span><br/> | <dl> <span data-ttu-id="d305a-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d305a-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d305a-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d305a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d305a-130">數學函數</span><span class="sxs-lookup"><span data-stu-id="d305a-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d305a-131">**D3DXVec3Add**</span><span class="sxs-lookup"><span data-stu-id="d305a-131">**D3DXVec3Add**</span></span>](d3dxvec3add.md)
</dt> <dt>

[<span data-ttu-id="d305a-132">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="d305a-132">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
</dt> </dl>

 

 
