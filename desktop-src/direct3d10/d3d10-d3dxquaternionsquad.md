---
description: 使用球面四邊形插補在四元數之間進行插補。
ms.assetid: ba953731-4372-4b32-942b-23abfe479704
title: 'D3DXQuaternionSquad 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: af2bb582909cf09a4044b293f3f298a5da2335a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514657"
---
# <a name="d3dxquaternionsquad-function-d3dx10mathh"></a><span data-ttu-id="60f8d-103">D3DXQuaternionSquad 函式 (D3DX10Math) </span><span class="sxs-lookup"><span data-stu-id="60f8d-103">D3DXQuaternionSquad function (D3DX10Math.h)</span></span>

<span data-ttu-id="60f8d-104">使用球面四邊形插補在四元數之間進行插補。</span><span class="sxs-lookup"><span data-stu-id="60f8d-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="60f8d-105">語法</span><span class="sxs-lookup"><span data-stu-id="60f8d-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="60f8d-106">參數</span><span class="sxs-lookup"><span data-stu-id="60f8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60f8d-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="60f8d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="60f8d-108">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="60f8d-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="60f8d-109">作業結果之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="60f8d-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="60f8d-110">*pQ1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60f8d-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f8d-111">Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="60f8d-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="60f8d-112">來源 D3DXQUATERNION 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="60f8d-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="60f8d-113">*pA* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60f8d-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f8d-114">Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="60f8d-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="60f8d-115">來源 D3DXQUATERNION 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="60f8d-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="60f8d-116">*pB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60f8d-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f8d-117">Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="60f8d-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="60f8d-118">來源 D3DXQUATERNION 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="60f8d-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="60f8d-119">*電腦* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60f8d-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f8d-120">Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="60f8d-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="60f8d-121">來源 D3DXQUATERNION 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="60f8d-121">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="60f8d-122"> \[ 中的 t\]</span><span class="sxs-lookup"><span data-stu-id="60f8d-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f8d-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60f8d-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60f8d-124">指出在四元數之間插離的參數。</span><span class="sxs-lookup"><span data-stu-id="60f8d-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60f8d-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="60f8d-125">Return value</span></span>

<span data-ttu-id="60f8d-126">類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="60f8d-126">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="60f8d-127">D3DXQUATERNION 結構的指標，此結構是指球形四邊形插補的結果。</span><span class="sxs-lookup"><span data-stu-id="60f8d-127">Pointer to a D3DXQUATERNION structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="60f8d-128">備註</span><span class="sxs-lookup"><span data-stu-id="60f8d-128">Remarks</span></span>

<span data-ttu-id="60f8d-129">此函式會使用下列一連串的球面線性插補作業：</span><span class="sxs-lookup"><span data-stu-id="60f8d-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="60f8d-130">此函式的傳回值與不悅參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="60f8d-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="60f8d-131">如此一來，D3DXQuaternionSquad 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="60f8d-131">In this way, the D3DXQuaternionSquad function can be used as a parameter for another function.</span></span>

<span data-ttu-id="60f8d-132">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="60f8d-132">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="60f8d-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="60f8d-133">Requirements</span></span>



| <span data-ttu-id="60f8d-134">需求</span><span class="sxs-lookup"><span data-stu-id="60f8d-134">Requirement</span></span> | <span data-ttu-id="60f8d-135">值</span><span class="sxs-lookup"><span data-stu-id="60f8d-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60f8d-136">標頭</span><span class="sxs-lookup"><span data-stu-id="60f8d-136">Header</span></span><br/>  | <dl> <span data-ttu-id="60f8d-137"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="60f8d-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="60f8d-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="60f8d-138">Library</span></span><br/> | <dl> <span data-ttu-id="60f8d-139"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="60f8d-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="60f8d-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60f8d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60f8d-141">數學函數</span><span class="sxs-lookup"><span data-stu-id="60f8d-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
