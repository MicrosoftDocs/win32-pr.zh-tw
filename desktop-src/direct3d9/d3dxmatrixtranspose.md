---
description: 傳回矩陣的矩陣變換。
ms.assetid: 0ba9682f-3dd6-48b2-82b1-6e34e8ce5452
title: 'D3DXMatrixTranspose 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranspose
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 700fc023cd15227c2cf26cd5bdcab51dc0ae3297
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988574"
---
# <a name="d3dxmatrixtranspose-function-d3dx9mathh"></a><span data-ttu-id="65da3-103">D3DXMatrixTranspose 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="65da3-103">D3DXMatrixTranspose function (D3dx9math.h)</span></span>

<span data-ttu-id="65da3-104">傳回矩陣的矩陣變換。</span><span class="sxs-lookup"><span data-stu-id="65da3-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="65da3-105">語法</span><span class="sxs-lookup"><span data-stu-id="65da3-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="65da3-106">參數</span><span class="sxs-lookup"><span data-stu-id="65da3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65da3-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="65da3-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="65da3-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="65da3-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="65da3-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="65da3-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="65da3-110">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="65da3-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65da3-111">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="65da3-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="65da3-112">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="65da3-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65da3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="65da3-113">Return value</span></span>

<span data-ttu-id="65da3-114">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="65da3-114">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="65da3-115">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是矩陣的矩陣變換。</span><span class="sxs-lookup"><span data-stu-id="65da3-115">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="65da3-116">備註</span><span class="sxs-lookup"><span data-stu-id="65da3-116">Remarks</span></span>

<span data-ttu-id="65da3-117">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="65da3-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="65da3-118">如此一來， **D3DXMatrixTranspose** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="65da3-118">In this way, the **D3DXMatrixTranspose** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="65da3-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="65da3-119">Requirements</span></span>



| <span data-ttu-id="65da3-120">需求</span><span class="sxs-lookup"><span data-stu-id="65da3-120">Requirement</span></span> | <span data-ttu-id="65da3-121">值</span><span class="sxs-lookup"><span data-stu-id="65da3-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65da3-122">標頭</span><span class="sxs-lookup"><span data-stu-id="65da3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="65da3-123"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="65da3-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="65da3-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="65da3-124">Library</span></span><br/> | <dl> <span data-ttu-id="65da3-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="65da3-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="65da3-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65da3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65da3-127">數學函數</span><span class="sxs-lookup"><span data-stu-id="65da3-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




