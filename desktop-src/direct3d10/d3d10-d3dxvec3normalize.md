---
description: D3DXVec3Normalize 函式 (D3DX10Math) -傳回3D 向量的正規化版本。
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
ms.openlocfilehash: 3f1317b1b8887b9ff306fcaed2cb6da2d077010f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108176"
---
# <a name="d3dxvec3normalize-function-d3dx10mathh"></a><span data-ttu-id="de767-103">D3DXVec3Normalize 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="de767-103">D3DXVec3Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="de767-104">傳回正規化版本的3D 向量。</span><span class="sxs-lookup"><span data-stu-id="de767-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="de767-105">語法</span><span class="sxs-lookup"><span data-stu-id="de767-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="de767-106">參數</span><span class="sxs-lookup"><span data-stu-id="de767-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de767-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="de767-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="de767-108">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="de767-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="de767-109">作業結果之 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="de767-109">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="de767-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="de767-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de767-111">Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="de767-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="de767-112">來源 D3DXVECTOR3 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="de767-112">Pointer to the source D3DXVECTOR3 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de767-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="de767-113">Return value</span></span>

<span data-ttu-id="de767-114">類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="de767-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="de767-115">D3DXVECTOR3 結構的指標，該結構為指定向量的正規化版本。</span><span class="sxs-lookup"><span data-stu-id="de767-115">Pointer to a D3DXVECTOR3 structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="de767-116">備註</span><span class="sxs-lookup"><span data-stu-id="de767-116">Remarks</span></span>

<span data-ttu-id="de767-117">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="de767-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="de767-118">如此一來，D3DXVec3Normalize 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="de767-118">In this way, the D3DXVec3Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="de767-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="de767-119">Requirements</span></span>



| <span data-ttu-id="de767-120">需求</span><span class="sxs-lookup"><span data-stu-id="de767-120">Requirement</span></span> | <span data-ttu-id="de767-121">值</span><span class="sxs-lookup"><span data-stu-id="de767-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de767-122">標頭</span><span class="sxs-lookup"><span data-stu-id="de767-122">Header</span></span><br/> | <dl> <span data-ttu-id="de767-123"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="de767-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de767-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de767-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de767-125">數學函數</span><span class="sxs-lookup"><span data-stu-id="de767-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
