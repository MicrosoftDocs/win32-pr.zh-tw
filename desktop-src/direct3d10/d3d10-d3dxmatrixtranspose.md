---
description: D3DXMatrixTranspose 函式 (D3DX10Math) -傳回矩陣的矩陣轉型。
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
ms.openlocfilehash: e20fd8a29ba3f9adec7134a011f8f470c60f7011
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108856"
---
# <a name="d3dxmatrixtranspose-function-d3dx10mathh"></a><span data-ttu-id="773f2-103">D3DXMatrixTranspose 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="773f2-103">D3DXMatrixTranspose function (D3DX10Math.h)</span></span>

<span data-ttu-id="773f2-104">傳回矩陣的矩陣變換。</span><span class="sxs-lookup"><span data-stu-id="773f2-104">Returns the matrix transpose of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="773f2-105">語法</span><span class="sxs-lookup"><span data-stu-id="773f2-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranspose(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="773f2-106">參數</span><span class="sxs-lookup"><span data-stu-id="773f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="773f2-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="773f2-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="773f2-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="773f2-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="773f2-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="773f2-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="773f2-110">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="773f2-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="773f2-111">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="773f2-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="773f2-112">來源 D3DXMATRIX 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="773f2-112">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="773f2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="773f2-113">Return value</span></span>

<span data-ttu-id="773f2-114">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="773f2-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="773f2-115">D3DXMATRIX 結構的指標，此結構是矩陣的矩陣變換。</span><span class="sxs-lookup"><span data-stu-id="773f2-115">Pointer to the D3DXMATRIX structure that is the matrix transpose of the matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="773f2-116">備註</span><span class="sxs-lookup"><span data-stu-id="773f2-116">Remarks</span></span>

<span data-ttu-id="773f2-117">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="773f2-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="773f2-118">如此一來，D3DXMatrixTranspose 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="773f2-118">In this way, the D3DXMatrixTranspose function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="773f2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="773f2-119">Requirements</span></span>



| <span data-ttu-id="773f2-120">需求</span><span class="sxs-lookup"><span data-stu-id="773f2-120">Requirement</span></span> | <span data-ttu-id="773f2-121">值</span><span class="sxs-lookup"><span data-stu-id="773f2-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="773f2-122">標頭</span><span class="sxs-lookup"><span data-stu-id="773f2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="773f2-123"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="773f2-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="773f2-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="773f2-124">Library</span></span><br/> | <dl> <span data-ttu-id="773f2-125"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="773f2-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="773f2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="773f2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="773f2-127">數學函數</span><span class="sxs-lookup"><span data-stu-id="773f2-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
