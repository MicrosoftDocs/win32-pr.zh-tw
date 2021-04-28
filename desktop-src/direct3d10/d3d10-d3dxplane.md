---
description: D3DXPLANE 結構 (D3DX10Math) -描述平面。
ms.assetid: c6da7343-a4f3-4cac-855b-14bd70c0d3c2
title: 'D3DXPLANE 結構 (D3DX10Math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 440246fb47a851f9f5339c72a484a2cb59e8f662
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103326"
---
# <a name="d3dxplane-structure-d3dx10mathh"></a><span data-ttu-id="f026c-103">D3DXPLANE 結構 (D3DX10Math .h) </span><span class="sxs-lookup"><span data-stu-id="f026c-103">D3DXPLANE structure (D3DX10Math.h)</span></span>

<span data-ttu-id="f026c-104">描述平面。</span><span class="sxs-lookup"><span data-stu-id="f026c-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="f026c-105">語法</span><span class="sxs-lookup"><span data-stu-id="f026c-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="f026c-106">成員</span><span class="sxs-lookup"><span data-stu-id="f026c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f026c-107">**的**</span><span class="sxs-lookup"><span data-stu-id="f026c-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="f026c-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f026c-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f026c-109">一般平面方程式中裁剪平面的係數。</span><span class="sxs-lookup"><span data-stu-id="f026c-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="f026c-110">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="f026c-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f026c-111">**b**</span><span class="sxs-lookup"><span data-stu-id="f026c-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="f026c-112">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f026c-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f026c-113">一般平面方程式中裁剪平面的 b 係數。</span><span class="sxs-lookup"><span data-stu-id="f026c-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="f026c-114">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="f026c-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f026c-115">**c**</span><span class="sxs-lookup"><span data-stu-id="f026c-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="f026c-116">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f026c-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f026c-117">一般平面方程式中裁剪平面的 c 係數。</span><span class="sxs-lookup"><span data-stu-id="f026c-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="f026c-118">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="f026c-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f026c-119">**d**</span><span class="sxs-lookup"><span data-stu-id="f026c-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="f026c-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f026c-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f026c-121">一般平面方程式中裁剪平面的 d 係數。</span><span class="sxs-lookup"><span data-stu-id="f026c-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="f026c-122">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="f026c-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f026c-123">備註</span><span class="sxs-lookup"><span data-stu-id="f026c-123">Remarks</span></span>

<span data-ttu-id="f026c-124">**D3DXPLANE** 結構的成員採用一般平面方程式的形式。</span><span class="sxs-lookup"><span data-stu-id="f026c-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="f026c-125">它們符合一般平面方程式，因此 ax + by + cz + dw = 0。</span><span class="sxs-lookup"><span data-stu-id="f026c-125">They fit into the general plane equation so that ax + by + cz + dw = 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="f026c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f026c-126">Requirements</span></span>



| <span data-ttu-id="f026c-127">需求</span><span class="sxs-lookup"><span data-stu-id="f026c-127">Requirement</span></span> | <span data-ttu-id="f026c-128">值</span><span class="sxs-lookup"><span data-stu-id="f026c-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f026c-129">標頭</span><span class="sxs-lookup"><span data-stu-id="f026c-129">Header</span></span><br/> | <dl> <span data-ttu-id="f026c-130"><dt>D3DX10Math。h</dt></span><span class="sxs-lookup"><span data-stu-id="f026c-130"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f026c-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f026c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f026c-132">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="f026c-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
