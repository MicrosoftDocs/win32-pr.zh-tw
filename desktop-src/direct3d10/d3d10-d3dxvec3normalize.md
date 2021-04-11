---
description: 傳回正規化版本的3D 向量。
ms.assetid: 420321a2-0c3b-419c-9620-acf184e7b4f0
title: 'D3DXVec3Normalize 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 413b807c53e0b46b115af2aa283e4902a45f5979
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854048"
---
# <a name="d3dxvec3normalize-function-d3dx10mathh"></a><span data-ttu-id="f1f87-103">D3DXVec3Normalize 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="f1f87-103">D3DXVec3Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="f1f87-104">傳回正規化版本的3D 向量。</span><span class="sxs-lookup"><span data-stu-id="f1f87-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1f87-105">語法</span><span class="sxs-lookup"><span data-stu-id="f1f87-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="f1f87-106">參數</span><span class="sxs-lookup"><span data-stu-id="f1f87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1f87-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f1f87-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f87-108">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f1f87-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f1f87-109">作業結果之 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="f1f87-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f1f87-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1f87-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1f87-111">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f1f87-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f1f87-112">來源 D3DXVECTOR3 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f1f87-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1f87-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1f87-113">Return value</span></span>

<span data-ttu-id="f1f87-114">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="f1f87-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="f1f87-115">D3DXVECTOR3 結構的指標，該結構為指定向量的正規化版本。</span><span class="sxs-lookup"><span data-stu-id="f1f87-115">Pointer to a D3DXVECTOR3 structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1f87-116">備註</span><span class="sxs-lookup"><span data-stu-id="f1f87-116">Remarks</span></span>

<span data-ttu-id="f1f87-117">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="f1f87-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f1f87-118">如此一來，D3DXVec3Normalize 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="f1f87-118">In this way, the D3DXVec3Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1f87-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1f87-119">Requirements</span></span>



| <span data-ttu-id="f1f87-120">需求</span><span class="sxs-lookup"><span data-stu-id="f1f87-120">Requirement</span></span> | <span data-ttu-id="f1f87-121">值</span><span class="sxs-lookup"><span data-stu-id="f1f87-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1f87-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f1f87-122">Header</span></span><br/> | <dl> <span data-ttu-id="f1f87-123"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1f87-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1f87-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1f87-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1f87-125">數學函數</span><span class="sxs-lookup"><span data-stu-id="f1f87-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
