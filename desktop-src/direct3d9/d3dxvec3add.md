---
description: 新增兩個3D 向量。
ms.assetid: 2979e291-786b-4bc9-b584-421f08db949a
title: 'D3DXVec3Add 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Add
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16fb06c5e7b32506a94a5828fe7f5e1305afff7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976733"
---
# <a name="d3dxvec3add-function"></a><span data-ttu-id="e57da-103">D3DXVec3Add 函式</span><span class="sxs-lookup"><span data-stu-id="e57da-103">D3DXVec3Add function</span></span>

<span data-ttu-id="e57da-104">新增兩個3D 向量。</span><span class="sxs-lookup"><span data-stu-id="e57da-104">Adds two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="e57da-105">語法</span><span class="sxs-lookup"><span data-stu-id="e57da-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Add(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="e57da-106">參數</span><span class="sxs-lookup"><span data-stu-id="e57da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e57da-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="e57da-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e57da-108">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e57da-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e57da-109">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="e57da-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e57da-110">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e57da-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e57da-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e57da-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e57da-112">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="e57da-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e57da-113">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e57da-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e57da-114">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e57da-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e57da-115">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="e57da-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e57da-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="e57da-116">Return value</span></span>

<span data-ttu-id="e57da-117">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e57da-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="e57da-118">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，這是兩個3d 向量的總和。</span><span class="sxs-lookup"><span data-stu-id="e57da-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the sum of the two 3D vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="e57da-119">備註</span><span class="sxs-lookup"><span data-stu-id="e57da-119">Remarks</span></span>

<span data-ttu-id="e57da-120">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="e57da-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e57da-121">如此一來， **D3DXVec3Add** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="e57da-121">In this way, the **D3DXVec3Add** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e57da-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e57da-122">Requirements</span></span>



| <span data-ttu-id="e57da-123">需求</span><span class="sxs-lookup"><span data-stu-id="e57da-123">Requirement</span></span> | <span data-ttu-id="e57da-124">值</span><span class="sxs-lookup"><span data-stu-id="e57da-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e57da-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e57da-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e57da-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="e57da-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e57da-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="e57da-127">Library</span></span><br/> | <dl> <span data-ttu-id="e57da-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e57da-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e57da-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e57da-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e57da-130">數學函數</span><span class="sxs-lookup"><span data-stu-id="e57da-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e57da-131">**D3DXVec3Subtract**</span><span class="sxs-lookup"><span data-stu-id="e57da-131">**D3DXVec3Subtract**</span></span>](d3dxvec3subtract.md)
</dt> <dt>

[<span data-ttu-id="e57da-132">**D3DXVec3Scale**</span><span class="sxs-lookup"><span data-stu-id="e57da-132">**D3DXVec3Scale**</span></span>](d3dxvec3scale.md)
</dt> </dl>

 

 




