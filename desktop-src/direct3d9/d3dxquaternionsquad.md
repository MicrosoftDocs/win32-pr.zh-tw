---
description: 使用球面四邊形插補在四元數之間進行插補。
ms.assetid: afce9afb-64cc-4059-90f5-7ed1aca9b3cb
title: 'D3DXQuaternionSquad 函式 (D3dx9math) '
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e4fa980d551ac43f66035c1dcaa46d1c1c590a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992533"
---
# <a name="d3dxquaternionsquad-function-d3dx9mathh"></a><span data-ttu-id="4ac47-103">D3DXQuaternionSquad 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="4ac47-103">D3DXQuaternionSquad function (D3dx9math.h)</span></span>

<span data-ttu-id="4ac47-104">使用球面四邊形插補在四元數之間進行插補。</span><span class="sxs-lookup"><span data-stu-id="4ac47-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ac47-105">語法</span><span class="sxs-lookup"><span data-stu-id="4ac47-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="4ac47-106">參數</span><span class="sxs-lookup"><span data-stu-id="4ac47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ac47-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4ac47-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac47-108">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ac47-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4ac47-109">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="4ac47-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4ac47-110">*pQ1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ac47-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac47-111">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4ac47-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4ac47-112">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4ac47-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4ac47-113">*pA* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ac47-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac47-114">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4ac47-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4ac47-115">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4ac47-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4ac47-116">*pB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ac47-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac47-117">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4ac47-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4ac47-118">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4ac47-118">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4ac47-119">*電腦* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ac47-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac47-120">Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4ac47-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4ac47-121">來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4ac47-121">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4ac47-122"> \[ 中的 t\]</span><span class="sxs-lookup"><span data-stu-id="4ac47-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ac47-123">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4ac47-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4ac47-124">指出在四元數之間插離的參數。</span><span class="sxs-lookup"><span data-stu-id="4ac47-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ac47-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ac47-125">Return value</span></span>

<span data-ttu-id="4ac47-126">類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4ac47-126">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4ac47-127">[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是指球形四邊形插補的結果。</span><span class="sxs-lookup"><span data-stu-id="4ac47-127">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ac47-128">備註</span><span class="sxs-lookup"><span data-stu-id="4ac47-128">Remarks</span></span>

<span data-ttu-id="4ac47-129">此函式會使用下列一連串的球面線性插補作業：</span><span class="sxs-lookup"><span data-stu-id="4ac47-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="4ac47-130">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="4ac47-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="4ac47-131">如此一來， **D3DXQuaternionSquad** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="4ac47-131">In this way, the **D3DXQuaternionSquad** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="4ac47-132">如需在四元數之間插插的範例，請參閱 SkinnedMesh 範例。</span><span class="sxs-lookup"><span data-stu-id="4ac47-132">For an example of interpolating between quaternions, see the SkinnedMesh Sample.</span></span> <span data-ttu-id="4ac47-133">您可以從 DirectX SDK 取得此範例並瞭解它。</span><span class="sxs-lookup"><span data-stu-id="4ac47-133">You can get this sample and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="4ac47-134">如需有關 DirectX SDK 的資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。</span><span class="sxs-lookup"><span data-stu-id="4ac47-134">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="4ac47-135">針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。</span><span class="sxs-lookup"><span data-stu-id="4ac47-135">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ac47-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ac47-136">Requirements</span></span>



| <span data-ttu-id="4ac47-137">需求</span><span class="sxs-lookup"><span data-stu-id="4ac47-137">Requirement</span></span> | <span data-ttu-id="4ac47-138">值</span><span class="sxs-lookup"><span data-stu-id="4ac47-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ac47-139">標頭</span><span class="sxs-lookup"><span data-stu-id="4ac47-139">Header</span></span><br/>  | <dl> <span data-ttu-id="4ac47-140"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ac47-140"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4ac47-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="4ac47-141">Library</span></span><br/> | <dl> <span data-ttu-id="4ac47-142"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ac47-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4ac47-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ac47-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ac47-144">數學函數</span><span class="sxs-lookup"><span data-stu-id="4ac47-144">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4ac47-145">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="4ac47-145">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="4ac47-146">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="4ac47-146">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="4ac47-147">**D3DXQuaternionSquadSetup**</span><span class="sxs-lookup"><span data-stu-id="4ac47-147">**D3DXQuaternionSquadSetup**</span></span>](d3dxquaternionsquadsetup.md)
</dt> </dl>

 

 
