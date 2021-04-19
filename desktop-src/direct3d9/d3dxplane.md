---
description: 描述平面。
ms.assetid: ffca4650-9788-4559-8f6b-a4e5db29ce55
title: 'D3DXPLANE 結構 (D3dx9math .h) '
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
- d3dx9math.h
ms.openlocfilehash: 260f9555313aea3443f0728f2b50189228429803
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106990013"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a><span data-ttu-id="f8f00-103">D3DXPLANE 結構 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="f8f00-103">D3DXPLANE structure (D3dx9math.h)</span></span>

<span data-ttu-id="f8f00-104">描述平面。</span><span class="sxs-lookup"><span data-stu-id="f8f00-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8f00-105">語法</span><span class="sxs-lookup"><span data-stu-id="f8f00-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="f8f00-106">成員</span><span class="sxs-lookup"><span data-stu-id="f8f00-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f8f00-107">**的**</span><span class="sxs-lookup"><span data-stu-id="f8f00-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="f8f00-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8f00-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8f00-109">一般平面方程式中裁剪平面的係數。</span><span class="sxs-lookup"><span data-stu-id="f8f00-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="f8f00-110">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="f8f00-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f8f00-111">**b**</span><span class="sxs-lookup"><span data-stu-id="f8f00-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="f8f00-112">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8f00-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8f00-113">一般平面方程式中裁剪平面的 b 係數。</span><span class="sxs-lookup"><span data-stu-id="f8f00-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="f8f00-114">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="f8f00-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f8f00-115">**c**</span><span class="sxs-lookup"><span data-stu-id="f8f00-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="f8f00-116">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8f00-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8f00-117">一般平面方程式中裁剪平面的 c 係數。</span><span class="sxs-lookup"><span data-stu-id="f8f00-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="f8f00-118">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="f8f00-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f8f00-119">**d**</span><span class="sxs-lookup"><span data-stu-id="f8f00-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="f8f00-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8f00-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f8f00-121">一般平面方程式中裁剪平面的 d 係數。</span><span class="sxs-lookup"><span data-stu-id="f8f00-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="f8f00-122">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="f8f00-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8f00-123">備註</span><span class="sxs-lookup"><span data-stu-id="f8f00-123">Remarks</span></span>

<span data-ttu-id="f8f00-124">**D3DXPLANE** 結構的成員採用一般平面方程式的形式。</span><span class="sxs-lookup"><span data-stu-id="f8f00-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="f8f00-125">它們符合一般平面 **方程式，** 因此 x + **b** y + **c** z + **d** w = 0。</span><span class="sxs-lookup"><span data-stu-id="f8f00-125">They fit into the general plane equation so that **a** x + **b** y + **c** z + **d** w = 0.</span></span>

<span data-ttu-id="f8f00-126">C + + 程式設計人員可以利用執行多載的函式和指派、一元和二元 (（包括相等) 運算子的 [**D3DXPLANE 延伸**](d3dxplane-extensions.md) 模組）來利用運算子多載和類型轉換。</span><span class="sxs-lookup"><span data-stu-id="f8f00-126">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXPLANE Extensions**](d3dxplane-extensions.md) which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8f00-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8f00-127">Requirements</span></span>



| <span data-ttu-id="f8f00-128">需求</span><span class="sxs-lookup"><span data-stu-id="f8f00-128">Requirement</span></span> | <span data-ttu-id="f8f00-129">值</span><span class="sxs-lookup"><span data-stu-id="f8f00-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f00-130">標頭</span><span class="sxs-lookup"><span data-stu-id="f8f00-130">Header</span></span><br/> | <dl> <span data-ttu-id="f8f00-131"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="f8f00-131"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8f00-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8f00-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8f00-133">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="f8f00-133">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
