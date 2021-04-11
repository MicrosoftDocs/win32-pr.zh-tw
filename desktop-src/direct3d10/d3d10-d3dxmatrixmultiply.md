---
description: 決定兩個矩陣的乘積。
ms.assetid: d15cd680-0e19-4353-9eee-73933663960e
title: 'D3DXMatrixMultiply 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5f07130c25ce9ef1c588309460e4e12e67bb2485
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946228"
---
# <a name="d3dxmatrixmultiply-function-d3dx10mathh"></a><span data-ttu-id="31c90-103">D3DXMatrixMultiply 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="31c90-103">D3DXMatrixMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="31c90-104">決定兩個矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="31c90-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="31c90-105">語法</span><span class="sxs-lookup"><span data-stu-id="31c90-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="31c90-106">參數</span><span class="sxs-lookup"><span data-stu-id="31c90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31c90-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="31c90-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="31c90-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="31c90-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="31c90-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="31c90-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="31c90-110">*pM1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="31c90-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31c90-111">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="31c90-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="31c90-112">來源 D3DXMATRIX 結構的指標 (左手邊) 。</span><span class="sxs-lookup"><span data-stu-id="31c90-112">Pointer to a source D3DXMATRIX structure (left hand side).</span></span>

</dd> <dt>

<span data-ttu-id="31c90-113">*pM2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="31c90-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31c90-114">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="31c90-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="31c90-115">指向來源 D3DXMATRIX 結構 (右手邊) 的指標。</span><span class="sxs-lookup"><span data-stu-id="31c90-115">Pointer to a source D3DXMATRIX structure (right hand side).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31c90-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="31c90-116">Return value</span></span>

<span data-ttu-id="31c90-117">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="31c90-117">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="31c90-118">D3DXMATRIX 結構的指標，這是兩個矩陣的乘積。</span><span class="sxs-lookup"><span data-stu-id="31c90-118">Pointer to a D3DXMATRIX structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="31c90-119">備註</span><span class="sxs-lookup"><span data-stu-id="31c90-119">Remarks</span></span>

<span data-ttu-id="31c90-120">結果代表轉換 M1，後面接著轉換 M2 (Out = M1 \* m2) 。</span><span class="sxs-lookup"><span data-stu-id="31c90-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="31c90-121">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="31c90-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="31c90-122">如此一來，D3DXMatrixMultiply 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="31c90-122">In this way, the D3DXMatrixMultiply function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="31c90-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="31c90-123">Requirements</span></span>



| <span data-ttu-id="31c90-124">需求</span><span class="sxs-lookup"><span data-stu-id="31c90-124">Requirement</span></span> | <span data-ttu-id="31c90-125">值</span><span class="sxs-lookup"><span data-stu-id="31c90-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31c90-126">標頭</span><span class="sxs-lookup"><span data-stu-id="31c90-126">Header</span></span><br/>  | <dl> <span data-ttu-id="31c90-127"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="31c90-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="31c90-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="31c90-128">Library</span></span><br/> | <dl> <span data-ttu-id="31c90-129"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="31c90-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31c90-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31c90-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31c90-131">數學函數</span><span class="sxs-lookup"><span data-stu-id="31c90-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
