---
description: D3DXQuaternionRotationMatrix function (D3dx9math) -從旋轉矩陣建立四元數。
ms.assetid: 4fafb1aa-5d6f-46e6-84b1-e0bac22952d2
title: 'D3DXQuaternionRotationMatrix 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9b0ff8529f32d398ac208cff3214fccfdb2ade81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094006"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx9mathh"></a><span data-ttu-id="725f1-103">D3DXQuaternionRotationMatrix 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="725f1-103">D3DXQuaternionRotationMatrix function (D3dx9math.h)</span></span>

<span data-ttu-id="725f1-104">從旋轉矩陣建立四元數。</span><span class="sxs-lookup"><span data-stu-id="725f1-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="725f1-105">語法</span><span class="sxs-lookup"><span data-stu-id="725f1-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="725f1-106">參數</span><span class="sxs-lookup"><span data-stu-id="725f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="725f1-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="725f1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="725f1-108">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="725f1-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="725f1-109">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="725f1-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="725f1-110">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="725f1-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="725f1-111">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="725f1-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="725f1-112">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="725f1-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="725f1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="725f1-113">Return value</span></span>

<span data-ttu-id="725f1-114">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="725f1-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="725f1-115">從旋轉矩陣建立之 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="725f1-115">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="725f1-116">備註</span><span class="sxs-lookup"><span data-stu-id="725f1-116">Remarks</span></span>

<span data-ttu-id="725f1-117">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="725f1-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="725f1-118">如此一來， **D3DXQuaternionRotationMatrix** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="725f1-118">In this way, the **D3DXQuaternionRotationMatrix** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="725f1-119">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="725f1-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="725f1-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="725f1-120">Requirements</span></span>



| <span data-ttu-id="725f1-121">需求</span><span class="sxs-lookup"><span data-stu-id="725f1-121">Requirement</span></span> | <span data-ttu-id="725f1-122">值</span><span class="sxs-lookup"><span data-stu-id="725f1-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="725f1-123">標頭</span><span class="sxs-lookup"><span data-stu-id="725f1-123">Header</span></span><br/>  | <dl> <span data-ttu-id="725f1-124"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="725f1-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="725f1-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="725f1-125">Library</span></span><br/> | <dl> <span data-ttu-id="725f1-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="725f1-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="725f1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="725f1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="725f1-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="725f1-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="725f1-129">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="725f1-129">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="725f1-130">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="725f1-130">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 




