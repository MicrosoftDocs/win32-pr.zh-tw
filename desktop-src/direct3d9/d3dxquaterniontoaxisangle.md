---
description: D3DXQuaternionToAxisAngle 函數 (D3dx9math) -計算四元數的軸和旋轉角度。
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: 'D3DXQuaternionToAxisAngle 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8613a9d14c5e33b0f9f4e719a02ac9a6d70d1119
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117976"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a><span data-ttu-id="63d67-103">D3DXQuaternionToAxisAngle 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="63d67-103">D3DXQuaternionToAxisAngle function (D3dx9math.h)</span></span>

<span data-ttu-id="63d67-104">計算四元數的軸和旋轉角度。</span><span class="sxs-lookup"><span data-stu-id="63d67-104">Computes a quaternion's axis and angle of rotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="63d67-105">語法</span><span class="sxs-lookup"><span data-stu-id="63d67-105">Syntax</span></span>


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a><span data-ttu-id="63d67-106">參數</span><span class="sxs-lookup"><span data-stu-id="63d67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63d67-107">*pQ* \[在\]</span><span class="sxs-lookup"><span data-stu-id="63d67-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63d67-108">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="63d67-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="63d67-109">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="63d67-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="63d67-110">*pAxis* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="63d67-110">*pAxis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="63d67-111">類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="63d67-111">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="63d67-112">此函式會傳回 [**D3DXVECTOR3**](d3dxvector3.md) 結構的指標，此結構會識別四元數的旋轉軸。</span><span class="sxs-lookup"><span data-stu-id="63d67-112">This function returns a pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the quaternion's axis of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="63d67-113">*pAngle* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="63d67-113">*pAngle* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="63d67-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="63d67-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="63d67-115">此函式會傳回浮點值的指標，此值會識別四元數的旋轉角度（以弧度為單位）。</span><span class="sxs-lookup"><span data-stu-id="63d67-115">This function returns a pointer to a FLOAT value that identifies the quaternion's angle of rotation in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63d67-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="63d67-116">Return value</span></span>

<span data-ttu-id="63d67-117">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="63d67-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="63d67-118">備註</span><span class="sxs-lookup"><span data-stu-id="63d67-118">Remarks</span></span>

<span data-ttu-id="63d67-119">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="63d67-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="63d67-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="63d67-120">Requirements</span></span>



| <span data-ttu-id="63d67-121">需求</span><span class="sxs-lookup"><span data-stu-id="63d67-121">Requirement</span></span> | <span data-ttu-id="63d67-122">值</span><span class="sxs-lookup"><span data-stu-id="63d67-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63d67-123">標頭</span><span class="sxs-lookup"><span data-stu-id="63d67-123">Header</span></span><br/>  | <dl> <span data-ttu-id="63d67-124"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="63d67-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="63d67-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="63d67-125">Library</span></span><br/> | <dl> <span data-ttu-id="63d67-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="63d67-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="63d67-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63d67-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63d67-128">數學函數</span><span class="sxs-lookup"><span data-stu-id="63d67-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
