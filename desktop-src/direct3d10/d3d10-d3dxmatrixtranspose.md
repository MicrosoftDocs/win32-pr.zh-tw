---
description: 傳回矩陣的矩陣變換。
ms.assetid: 934b17cc-39c4-425c-839b-69e080f0efd7
title: 'D3DXMatrixTranspose 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0ecc93a560e15b8f0abe4337b866efc292c9355e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985725"
---
# <a name="d3dxmatrixtranspose-function-d3dx10mathh"></a><span data-ttu-id="28ce4-103">D3DXMatrixTranspose 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="28ce4-103">D3DXMatrixTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="28ce4-104">傳回矩陣的矩陣變換。</span><span class="sxs-lookup"><span data-stu-id="28ce4-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="28ce4-105">語法</span><span class="sxs-lookup"><span data-stu-id="28ce4-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="28ce4-106">參數</span><span class="sxs-lookup"><span data-stu-id="28ce4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28ce4-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="28ce4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28ce4-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="28ce4-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="28ce4-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="28ce4-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="28ce4-110">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28ce4-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28ce4-111">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="28ce4-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="28ce4-112">來源 D3DXMATRIX 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="28ce4-112">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28ce4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="28ce4-113">Return value</span></span>

<span data-ttu-id="28ce4-114">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="28ce4-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="28ce4-115">D3DXMATRIX 結構的指標，此結構是矩陣的矩陣變換。</span><span class="sxs-lookup"><span data-stu-id="28ce4-115">Pointer to the D3DXMATRIX structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="28ce4-116">備註</span><span class="sxs-lookup"><span data-stu-id="28ce4-116">Remarks</span></span>

<span data-ttu-id="28ce4-117">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="28ce4-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="28ce4-118">如此一來，D3DXMatrixTranspose 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="28ce4-118">In this way, the D3DXMatrixTranspose function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="28ce4-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="28ce4-119">Requirements</span></span>



| <span data-ttu-id="28ce4-120">需求</span><span class="sxs-lookup"><span data-stu-id="28ce4-120">Requirement</span></span> | <span data-ttu-id="28ce4-121">值</span><span class="sxs-lookup"><span data-stu-id="28ce4-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28ce4-122">標頭</span><span class="sxs-lookup"><span data-stu-id="28ce4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="28ce4-123"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="28ce4-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="28ce4-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="28ce4-124">Library</span></span><br/> | <dl> <span data-ttu-id="28ce4-125"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="28ce4-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="28ce4-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28ce4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28ce4-127">數學函數</span><span class="sxs-lookup"><span data-stu-id="28ce4-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
