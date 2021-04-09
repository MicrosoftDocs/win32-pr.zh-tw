---
description: 傳回正規化版本的3D 向量。
ms.assetid: 7bb8302e-8af2-4328-9b46-bc9f5a009f56
title: 'D3DXVec3Normalize 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e563b17e53ead8199de582f6dcdeb9660fa622f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035344"
---
# <a name="d3dxvec3normalize-function-d3dx9mathh"></a><span data-ttu-id="6a754-103">D3DXVec3Normalize 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="6a754-103">D3DXVec3Normalize function (D3dx9math.h)</span></span>

<span data-ttu-id="6a754-104">傳回正規化版本的3D 向量。</span><span class="sxs-lookup"><span data-stu-id="6a754-104">Returns the normalized version of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a754-105">語法</span><span class="sxs-lookup"><span data-stu-id="6a754-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3Normalize(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="6a754-106">參數</span><span class="sxs-lookup"><span data-stu-id="6a754-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a754-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="6a754-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a754-108">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a754-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6a754-109">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="6a754-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6a754-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a754-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a754-111">Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6a754-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6a754-112">來源 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="6a754-112">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a754-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a754-113">Return value</span></span>

<span data-ttu-id="6a754-114">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="6a754-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6a754-115">[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，該結構為指定向量的正規化版本。</span><span class="sxs-lookup"><span data-stu-id="6a754-115">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the normalized version of the specified vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a754-116">備註</span><span class="sxs-lookup"><span data-stu-id="6a754-116">Remarks</span></span>

<span data-ttu-id="6a754-117">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="6a754-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="6a754-118">如此一來， **D3DXVec3Normalize** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="6a754-118">In this way, the **D3DXVec3Normalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a754-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a754-119">Requirements</span></span>



| <span data-ttu-id="6a754-120">需求</span><span class="sxs-lookup"><span data-stu-id="6a754-120">Requirement</span></span> | <span data-ttu-id="6a754-121">值</span><span class="sxs-lookup"><span data-stu-id="6a754-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a754-122">標頭</span><span class="sxs-lookup"><span data-stu-id="6a754-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6a754-123"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a754-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6a754-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="6a754-124">Library</span></span><br/> | <dl> <span data-ttu-id="6a754-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a754-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6a754-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a754-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a754-127">數學函數</span><span class="sxs-lookup"><span data-stu-id="6a754-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




