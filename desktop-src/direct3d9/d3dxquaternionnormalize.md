---
description: 計算單位長度四元數。
ms.assetid: 31f56c2b-96b0-4110-a5b9-ce09983779b6
title: 'D3DXQuaternionNormalize 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionNormalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d052d4dfc88feb2a00237392071f63d724070b3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514585"
---
# <a name="d3dxquaternionnormalize-function-d3dx9mathh"></a><span data-ttu-id="ff98e-103">D3DXQuaternionNormalize 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="ff98e-103">D3DXQuaternionNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="ff98e-104">計算單位長度四元數。</span><span class="sxs-lookup"><span data-stu-id="ff98e-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff98e-105">語法</span><span class="sxs-lookup"><span data-stu-id="ff98e-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="ff98e-106">參數</span><span class="sxs-lookup"><span data-stu-id="ff98e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff98e-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="ff98e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff98e-108">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ff98e-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ff98e-109">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="ff98e-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ff98e-110">*pQ* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff98e-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff98e-111">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="ff98e-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ff98e-112">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ff98e-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff98e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff98e-113">Return value</span></span>

<span data-ttu-id="ff98e-114">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="ff98e-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="ff98e-115">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是四元數的標準。</span><span class="sxs-lookup"><span data-stu-id="ff98e-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff98e-116">備註</span><span class="sxs-lookup"><span data-stu-id="ff98e-116">Remarks</span></span>

<span data-ttu-id="ff98e-117">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="ff98e-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="ff98e-118">如此一來， **D3DXQuaternionNormalize** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="ff98e-118">In this way, the **D3DXQuaternionNormalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff98e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff98e-119">Requirements</span></span>



| <span data-ttu-id="ff98e-120">需求</span><span class="sxs-lookup"><span data-stu-id="ff98e-120">Requirement</span></span> | <span data-ttu-id="ff98e-121">值</span><span class="sxs-lookup"><span data-stu-id="ff98e-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff98e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ff98e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ff98e-123"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff98e-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ff98e-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="ff98e-124">Library</span></span><br/> | <dl> <span data-ttu-id="ff98e-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff98e-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ff98e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff98e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff98e-127">數學函數</span><span class="sxs-lookup"><span data-stu-id="ff98e-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="ff98e-128">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="ff98e-128">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 




