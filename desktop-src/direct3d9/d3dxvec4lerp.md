---
description: 在兩個4D 向量之間執行線性插補。
ms.assetid: a068a626-17cd-4df9-8f41-9b417bfda1d1
title: 'D3DXVec4Lerp 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8df6f7b4be5a39335532dc86096f989727230942
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999013"
---
# <a name="d3dxvec4lerp-function"></a><span data-ttu-id="dba05-103">D3DXVec4Lerp 函式</span><span class="sxs-lookup"><span data-stu-id="dba05-103">D3DXVec4Lerp function</span></span>

<span data-ttu-id="dba05-104">在兩個4D 向量之間執行線性插補。</span><span class="sxs-lookup"><span data-stu-id="dba05-104">Performs a linear interpolation between two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="dba05-105">語法</span><span class="sxs-lookup"><span data-stu-id="dba05-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Lerp(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="dba05-106">參數</span><span class="sxs-lookup"><span data-stu-id="dba05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dba05-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="dba05-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dba05-108">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="dba05-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="dba05-109">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="dba05-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="dba05-110">*pV1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dba05-110">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dba05-111">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="dba05-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="dba05-112">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="dba05-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dba05-113">*pV2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dba05-113">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dba05-114">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="dba05-114">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="dba05-115">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="dba05-115">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dba05-116"> \[ 中的 s\]</span><span class="sxs-lookup"><span data-stu-id="dba05-116">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dba05-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dba05-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dba05-118">以線性方式在向量之間插補的參數。</span><span class="sxs-lookup"><span data-stu-id="dba05-118">Parameter that linearly interpolates between the vectors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dba05-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="dba05-119">Return value</span></span>

<span data-ttu-id="dba05-120">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="dba05-120">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="dba05-121">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是線性插補的結果。</span><span class="sxs-lookup"><span data-stu-id="dba05-121">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the linear interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="dba05-122">備註</span><span class="sxs-lookup"><span data-stu-id="dba05-122">Remarks</span></span>

<span data-ttu-id="dba05-123">此函式會根據下列公式執行線性插補： V1 + s (V2-V1) 。</span><span class="sxs-lookup"><span data-stu-id="dba05-123">This function performs the linear interpolation based on the following formula: V1 + s(V2-V1).</span></span>

<span data-ttu-id="dba05-124">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="dba05-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="dba05-125">如此一來， **D3DXVec4Lerp** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="dba05-125">In this way, the **D3DXVec4Lerp** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dba05-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="dba05-126">Requirements</span></span>



| <span data-ttu-id="dba05-127">需求</span><span class="sxs-lookup"><span data-stu-id="dba05-127">Requirement</span></span> | <span data-ttu-id="dba05-128">值</span><span class="sxs-lookup"><span data-stu-id="dba05-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dba05-129">標頭</span><span class="sxs-lookup"><span data-stu-id="dba05-129">Header</span></span><br/>  | <dl> <span data-ttu-id="dba05-130"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="dba05-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="dba05-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="dba05-131">Library</span></span><br/> | <dl> <span data-ttu-id="dba05-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dba05-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dba05-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dba05-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dba05-134">數學函數</span><span class="sxs-lookup"><span data-stu-id="dba05-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
