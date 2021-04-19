---
description: 將兩個色彩值加在一起，以建立新的色彩值。
ms.assetid: 7743392d-4676-4408-93e9-f92d4bf02411
title: 'D3DXColorAdd 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f326c9bec4802a9a94accc76b825cd1c6ea28fd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992330"
---
# <a name="d3dxcoloradd-function"></a><span data-ttu-id="3ff27-103">D3DXColorAdd 函式</span><span class="sxs-lookup"><span data-stu-id="3ff27-103">D3DXColorAdd function</span></span>

<span data-ttu-id="3ff27-104">將兩個色彩值加在一起，以建立新的色彩值。</span><span class="sxs-lookup"><span data-stu-id="3ff27-104">Adds two color values together to create a new color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ff27-105">語法</span><span class="sxs-lookup"><span data-stu-id="3ff27-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdd(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="3ff27-106">參數</span><span class="sxs-lookup"><span data-stu-id="3ff27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ff27-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="3ff27-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ff27-108">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="3ff27-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="3ff27-109">[**D3DXCOLOR**](d3dxcolor.md)結構的指標，該結構為運算的結果。</span><span class="sxs-lookup"><span data-stu-id="3ff27-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3ff27-110">*test-pc1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ff27-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ff27-111">Type： **Const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="3ff27-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="3ff27-112">來源 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="3ff27-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3ff27-113">*pC2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ff27-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ff27-114">Type： **Const [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="3ff27-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="3ff27-115">來源 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="3ff27-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ff27-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ff27-116">Return value</span></span>

<span data-ttu-id="3ff27-117">類型： **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="3ff27-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="3ff27-118">此函式會傳回 [**D3DXCOLOR**](d3dxcolor.md) 結構的指標，這是兩個色彩值的總和。</span><span class="sxs-lookup"><span data-stu-id="3ff27-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the sum of two color values.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ff27-119">備註</span><span class="sxs-lookup"><span data-stu-id="3ff27-119">Remarks</span></span>

<span data-ttu-id="3ff27-120">此函式的傳回值與不悅中傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="3ff27-120">The return value for this function is the same value returned in pOut.</span></span> <span data-ttu-id="3ff27-121">如此一來， **D3DXColorAdd** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="3ff27-121">In this way, the **D3DXColorAdd** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ff27-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ff27-122">Requirements</span></span>



| <span data-ttu-id="3ff27-123">需求</span><span class="sxs-lookup"><span data-stu-id="3ff27-123">Requirement</span></span> | <span data-ttu-id="3ff27-124">值</span><span class="sxs-lookup"><span data-stu-id="3ff27-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff27-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3ff27-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3ff27-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ff27-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3ff27-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="3ff27-127">Library</span></span><br/> | <dl> <span data-ttu-id="3ff27-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ff27-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3ff27-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ff27-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ff27-130">數學函數</span><span class="sxs-lookup"><span data-stu-id="3ff27-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="3ff27-131">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="3ff27-131">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="3ff27-132">**D3DXColorSubtract**</span><span class="sxs-lookup"><span data-stu-id="3ff27-132">**D3DXColorSubtract**</span></span>](d3dxcolorsubtract.md)
</dt> </dl>

 

 




