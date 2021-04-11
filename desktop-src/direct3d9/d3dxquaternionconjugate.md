---
description: 傳回四元數的共軛。
ms.assetid: f690fdd8-7805-4fc1-9064-4f249d5f7c4f
title: 'D3DXQuaternionConjugate 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionConjugate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bbf288724dbdede9d98ec4ee21afd1bb57dd7a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196344"
---
# <a name="d3dxquaternionconjugate-function"></a><span data-ttu-id="b32ee-103">D3DXQuaternionConjugate 函式</span><span class="sxs-lookup"><span data-stu-id="b32ee-103">D3DXQuaternionConjugate function</span></span>

<span data-ttu-id="b32ee-104">傳回四元數的共軛。</span><span class="sxs-lookup"><span data-stu-id="b32ee-104">Returns the conjugate of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="b32ee-105">語法</span><span class="sxs-lookup"><span data-stu-id="b32ee-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionConjugate(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="b32ee-106">參數</span><span class="sxs-lookup"><span data-stu-id="b32ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b32ee-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="b32ee-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b32ee-108">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="b32ee-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b32ee-109">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="b32ee-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b32ee-110">*pQ* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b32ee-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b32ee-111">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="b32ee-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b32ee-112">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b32ee-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b32ee-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b32ee-113">Return value</span></span>

<span data-ttu-id="b32ee-114">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="b32ee-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="b32ee-115">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是四元數的共軛。</span><span class="sxs-lookup"><span data-stu-id="b32ee-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the conjugate of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="b32ee-116">備註</span><span class="sxs-lookup"><span data-stu-id="b32ee-116">Remarks</span></span>

<span data-ttu-id="b32ee-117">假設 (x、y、z、w) 的四元數， **D3DXQuaternionConjugate** 函式會傳回四元數 (-x、-y、-z、w) 。</span><span class="sxs-lookup"><span data-stu-id="b32ee-117">Given a quaternion (x, y, z, w), the **D3DXQuaternionConjugate** function will return the quaternion (-x, -y, -z, w).</span></span>

<span data-ttu-id="b32ee-118">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="b32ee-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b32ee-119">如此一來， **D3DXQuaternionConjugate** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="b32ee-119">In this way, the **D3DXQuaternionConjugate** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b32ee-120">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="b32ee-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="b32ee-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="b32ee-121">Requirements</span></span>



| <span data-ttu-id="b32ee-122">需求</span><span class="sxs-lookup"><span data-stu-id="b32ee-122">Requirement</span></span> | <span data-ttu-id="b32ee-123">值</span><span class="sxs-lookup"><span data-stu-id="b32ee-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b32ee-124">標頭</span><span class="sxs-lookup"><span data-stu-id="b32ee-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b32ee-125"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="b32ee-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b32ee-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="b32ee-126">Library</span></span><br/> | <dl> <span data-ttu-id="b32ee-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b32ee-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b32ee-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b32ee-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b32ee-129">數學函數</span><span class="sxs-lookup"><span data-stu-id="b32ee-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b32ee-130">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="b32ee-130">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 




