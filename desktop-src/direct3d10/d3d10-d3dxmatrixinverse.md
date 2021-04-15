---
description: 計算矩陣的反向。
ms.assetid: 928a201b-814d-41cc-bfab-d2f8a12addeb
title: 'D3DXMatrixInverse 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixInverse
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc075609ea118e12b46846f649d689f6fbc2caf7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514688"
---
# <a name="d3dxmatrixinverse-function-d3dx10mathh"></a><span data-ttu-id="da5bc-103">D3DXMatrixInverse 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="da5bc-103">D3DXMatrixInverse function (D3DX10Math.h)</span></span>

<span data-ttu-id="da5bc-104">計算矩陣的反向。</span><span class="sxs-lookup"><span data-stu-id="da5bc-104">Calculates the inverse of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="da5bc-105">語法</span><span class="sxs-lookup"><span data-stu-id="da5bc-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixInverse(
  _Inout_       D3DXMATRIX *pOut,
  _Inout_       FLOAT      *pDeterminant,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="da5bc-106">參數</span><span class="sxs-lookup"><span data-stu-id="da5bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da5bc-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="da5bc-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="da5bc-108">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="da5bc-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="da5bc-109">[**D3DXMATRIX**](d3d10-d3dxmatrix.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="da5bc-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="da5bc-110">*pDeterminant* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="da5bc-110">*pDeterminant* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="da5bc-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="da5bc-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="da5bc-112">包含矩陣行列式的 FLOAT 值指標。</span><span class="sxs-lookup"><span data-stu-id="da5bc-112">Pointer to a FLOAT value containing the determinant of the matrix.</span></span> <span data-ttu-id="da5bc-113">如果不需要行列式，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="da5bc-113">If the determinant is not needed, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="da5bc-114">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da5bc-114">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da5bc-115">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="da5bc-115">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="da5bc-116">來源 D3DXMATRIX 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="da5bc-116">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da5bc-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="da5bc-117">Return value</span></span>

<span data-ttu-id="da5bc-118">類型： **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="da5bc-118">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="da5bc-119">D3DXMATRIX 結構的指標，此結構是矩陣的反向。</span><span class="sxs-lookup"><span data-stu-id="da5bc-119">Pointer to a D3DXMATRIX structure that is the inverse of the matrix.</span></span> <span data-ttu-id="da5bc-120">如果矩陣反轉失敗，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="da5bc-120">If matrix inversion fails, **NULL** is returned.</span></span>

<span data-ttu-id="da5bc-121">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="da5bc-121">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="da5bc-122">如此一來，D3DXMatrixInverse 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="da5bc-122">In this way, the D3DXMatrixInverse function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="da5bc-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="da5bc-123">Requirements</span></span>



| <span data-ttu-id="da5bc-124">需求</span><span class="sxs-lookup"><span data-stu-id="da5bc-124">Requirement</span></span> | <span data-ttu-id="da5bc-125">值</span><span class="sxs-lookup"><span data-stu-id="da5bc-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da5bc-126">標頭</span><span class="sxs-lookup"><span data-stu-id="da5bc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="da5bc-127"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="da5bc-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="da5bc-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="da5bc-128">Library</span></span><br/> | <dl> <span data-ttu-id="da5bc-129"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="da5bc-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="da5bc-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da5bc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da5bc-131">數學函數</span><span class="sxs-lookup"><span data-stu-id="da5bc-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
