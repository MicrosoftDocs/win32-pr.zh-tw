---
description: D3DXQuaternionRotationMatrix function (D3DX10Math) -從旋轉矩陣建立四元數。
ms.assetid: 316bf3e0-32ff-4e5e-b771-99f7eea2e27c
title: 'D3DXQuaternionRotationMatrix 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationMatrix
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cb923c135d436b36fe032d344366fdee687d27a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103146"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx10mathh"></a><span data-ttu-id="70990-103">D3DXQuaternionRotationMatrix 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="70990-103">D3DXQuaternionRotationMatrix function (D3DX10Math.h)</span></span>

<span data-ttu-id="70990-104">從旋轉矩陣建立四元數。</span><span class="sxs-lookup"><span data-stu-id="70990-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="70990-105">語法</span><span class="sxs-lookup"><span data-stu-id="70990-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="70990-106">參數</span><span class="sxs-lookup"><span data-stu-id="70990-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70990-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="70990-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="70990-108">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="70990-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="70990-109">作業結果之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="70990-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="70990-110">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="70990-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70990-111">Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="70990-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="70990-112">來源 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="70990-112">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70990-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="70990-113">Return value</span></span>

<span data-ttu-id="70990-114">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="70990-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="70990-115">從旋轉矩陣建立之 D3DXQUATERNION 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="70990-115">Pointer to the D3DXQUATERNION structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="70990-116">備註</span><span class="sxs-lookup"><span data-stu-id="70990-116">Remarks</span></span>

<span data-ttu-id="70990-117">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="70990-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="70990-118">如此一來，D3DXQuaternionRotationMatrix 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="70990-118">In this way, the D3DXQuaternionRotationMatrix function can be used as a parameter for another function.</span></span>

<span data-ttu-id="70990-119">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="70990-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="70990-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="70990-120">Requirements</span></span>



| <span data-ttu-id="70990-121">需求</span><span class="sxs-lookup"><span data-stu-id="70990-121">Requirement</span></span> | <span data-ttu-id="70990-122">值</span><span class="sxs-lookup"><span data-stu-id="70990-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70990-123">標頭</span><span class="sxs-lookup"><span data-stu-id="70990-123">Header</span></span><br/>  | <dl> <span data-ttu-id="70990-124"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="70990-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="70990-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="70990-125">Library</span></span><br/> | <dl> <span data-ttu-id="70990-126"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="70990-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="70990-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70990-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70990-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="70990-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
