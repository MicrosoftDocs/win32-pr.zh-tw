---
description: D3DXMatrixMultiply 函數 (D3dx9math) -決定兩個矩陣的乘積。
ms.assetid: 160c801a-6589-4a0d-8e90-7e7a99fbd5f7
title: 'D3DXMatrixMultiply 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiply
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3d183fc3c79797bab886d3a40211448ccf57d552
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107546"
---
# <a name="d3dxmatrixmultiply-function-d3dx9mathh"></a><span data-ttu-id="f577b-103">D3DXMatrixMultiply 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="f577b-103">D3DXMatrixMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="f577b-104">決定兩個矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="f577b-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="f577b-105">語法</span><span class="sxs-lookup"><span data-stu-id="f577b-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="f577b-106">參數</span><span class="sxs-lookup"><span data-stu-id="f577b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f577b-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f577b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f577b-108">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f577b-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f577b-109">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="f577b-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f577b-110">*pM1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f577b-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f577b-111">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f577b-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f577b-112">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f577b-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f577b-113">*pM2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f577b-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f577b-114">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="f577b-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f577b-115">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="f577b-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f577b-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f577b-116">Return value</span></span>

<span data-ttu-id="f577b-117">類型： **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f577b-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f577b-118">[**D3DXMATRIX**](d3dxmatrix.md)結構的指標，這是兩個矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="f577b-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="f577b-119">備註</span><span class="sxs-lookup"><span data-stu-id="f577b-119">Remarks</span></span>

<span data-ttu-id="f577b-120">結果代表轉換 M1，後面接著轉換 M2 (Out = M1 \* m2) 。</span><span class="sxs-lookup"><span data-stu-id="f577b-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="f577b-121">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="f577b-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f577b-122">如此一來， **D3DXMatrixMultiply** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="f577b-122">In this way, the **D3DXMatrixMultiply** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f577b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="f577b-123">Requirements</span></span>



| <span data-ttu-id="f577b-124">需求</span><span class="sxs-lookup"><span data-stu-id="f577b-124">Requirement</span></span> | <span data-ttu-id="f577b-125">值</span><span class="sxs-lookup"><span data-stu-id="f577b-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f577b-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f577b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="f577b-127"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="f577b-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f577b-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="f577b-128">Library</span></span><br/> | <dl> <span data-ttu-id="f577b-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f577b-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f577b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f577b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f577b-131">數學函數</span><span class="sxs-lookup"><span data-stu-id="f577b-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f577b-132">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="f577b-132">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




