---
description: 依指定的矩陣轉換4D 向量。
ms.assetid: de93f138-7cf8-43cc-8255-c053c799aea8
title: 'D3DXVec4Transform 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Transform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20192cf51a6096bbbce1f009d91d96551aec12d8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991484"
---
# <a name="d3dxvec4transform-function-d3dx9mathh"></a><span data-ttu-id="97663-103">D3DXVec4Transform 函式 (D3dx9math) </span><span class="sxs-lookup"><span data-stu-id="97663-103">D3DXVec4Transform function (D3dx9math.h)</span></span>

<span data-ttu-id="97663-104">依指定的矩陣轉換4D 向量。</span><span class="sxs-lookup"><span data-stu-id="97663-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="97663-105">語法</span><span class="sxs-lookup"><span data-stu-id="97663-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="97663-106">參數</span><span class="sxs-lookup"><span data-stu-id="97663-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97663-107">*不悅* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="97663-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="97663-108">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="97663-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="97663-109">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是作業的結果。</span><span class="sxs-lookup"><span data-stu-id="97663-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="97663-110">*pV* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97663-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97663-111">Type： **Const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="97663-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="97663-112">來源 [**D3DXVECTOR4**](d3dxvector4.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="97663-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="97663-113">*pM* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97663-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97663-114">Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="97663-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="97663-115">來源 [**D3DXMATRIX**](d3dxmatrix.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="97663-115">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97663-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="97663-116">Return value</span></span>

<span data-ttu-id="97663-117">類型： **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="97663-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="97663-118">[**D3DXVECTOR4**](d3dxvector4.md)結構的指標，此結構是轉換的4d 向量。</span><span class="sxs-lookup"><span data-stu-id="97663-118">Pointer to a [**D3DXVECTOR4**](d3dxvector4.md) structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="97663-119">備註</span><span class="sxs-lookup"><span data-stu-id="97663-119">Remarks</span></span>

<span data-ttu-id="97663-120">此函式的傳回值與 *不悅* 參數中所傳回的值相同。</span><span class="sxs-lookup"><span data-stu-id="97663-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="97663-121">如此一來， **D3DXVec4Transform** 函式就可以用來做為另一個函式的參數。</span><span class="sxs-lookup"><span data-stu-id="97663-121">In this way, the **D3DXVec4Transform** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="97663-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="97663-122">Requirements</span></span>



| <span data-ttu-id="97663-123">需求</span><span class="sxs-lookup"><span data-stu-id="97663-123">Requirement</span></span> | <span data-ttu-id="97663-124">值</span><span class="sxs-lookup"><span data-stu-id="97663-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97663-125">標頭</span><span class="sxs-lookup"><span data-stu-id="97663-125">Header</span></span><br/>  | <dl> <span data-ttu-id="97663-126"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="97663-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="97663-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="97663-127">Library</span></span><br/> | <dl> <span data-ttu-id="97663-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="97663-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="97663-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97663-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97663-130">數學函數</span><span class="sxs-lookup"><span data-stu-id="97663-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




