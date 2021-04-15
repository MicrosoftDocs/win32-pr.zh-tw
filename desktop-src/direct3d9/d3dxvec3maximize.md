---
description: 傳回由兩個3D 向量的最大元件所組成的3D 向量。
ms.assetid: 8d3a5310-bee9-4dbd-bef3-8a0e1586f365
title: 'D3DXVec3Maximize 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Maximize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d86f3e54a6399693e37cc0c8970439558d82c9c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514573"
---
# <a name="d3dxvec3maximize-function"></a><span data-ttu-id="a4f35-103">D3DXVec3Maximize 函式</span><span class="sxs-lookup"><span data-stu-id="a4f35-103">D3DXVec3Maximize function</span></span>

<span data-ttu-id="a4f35-104">傳回由兩個3D 向量的最大元件所組成的3D 向量。</span><span class="sxs-lookup"><span data-stu-id="a4f35-104">Returns a 3D vector that is made up of the largest components of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f35-105">語法</span><span class="sxs-lookup"><span data-stu-id="a4f35-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Maximize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="a4f35-106">參數</span><span class="sxs-lookup"><span data-stu-id="a4f35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4f35-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="a4f35-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f35-108">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4f35-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a4f35-109">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="a4f35-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a4f35-110">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4f35-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f35-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a4f35-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a4f35-112">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a4f35-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a4f35-113">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4f35-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f35-114">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="a4f35-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a4f35-115">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a4f35-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4f35-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4f35-116">Return value</span></span>

<span data-ttu-id="a4f35-117">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4f35-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="a4f35-118">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是由兩個向量的最大元件所組成。</span><span class="sxs-lookup"><span data-stu-id="a4f35-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is made up of the largest components of the two vectors.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4f35-119">備註</span><span class="sxs-lookup"><span data-stu-id="a4f35-119">Remarks</span></span>

<span data-ttu-id="a4f35-120">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="a4f35-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="a4f35-121">如此一來， **D3DXVec3Maximize** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="a4f35-121">In this way, the **D3DXVec3Maximize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f35-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4f35-122">Requirements</span></span>



| <span data-ttu-id="a4f35-123">需求</span><span class="sxs-lookup"><span data-stu-id="a4f35-123">Requirement</span></span> | <span data-ttu-id="a4f35-124">值</span><span class="sxs-lookup"><span data-stu-id="a4f35-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f35-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a4f35-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a4f35-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="a4f35-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a4f35-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="a4f35-127">Library</span></span><br/> | <dl> <span data-ttu-id="a4f35-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4f35-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a4f35-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4f35-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f35-130">數學函數</span><span class="sxs-lookup"><span data-stu-id="a4f35-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a4f35-131">**D3DXVec3Minimize**</span><span class="sxs-lookup"><span data-stu-id="a4f35-131">**D3DXVec3Minimize**</span></span>](d3dxvec3minimize.md)
</dt> </dl>

 

 




