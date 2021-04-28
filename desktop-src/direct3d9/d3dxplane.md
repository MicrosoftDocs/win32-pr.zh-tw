---
description: D3DXPLANE 結構 (D3dx9math) -描述平面。
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
ms.openlocfilehash: 3df0c94dbd49cf38d9230a2c5392df8497c64761
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115716"
---
# <a name="d3dxplane-structure-d3dx9mathh"></a><span data-ttu-id="ba12e-103">D3DXPLANE 結構 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="ba12e-103">D3DXPLANE structure (D3dx9math.h)</span></span>

<span data-ttu-id="ba12e-104">描述平面。</span><span class="sxs-lookup"><span data-stu-id="ba12e-104">Describes a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba12e-105">語法</span><span class="sxs-lookup"><span data-stu-id="ba12e-105">Syntax</span></span>


```C++
typedef struct D3DXPLANE {
  FLOAT a;
  FLOAT b;
  FLOAT c;
  FLOAT d;
} D3DXPLANE, *LPD3DXPLANE;
```



## <a name="members"></a><span data-ttu-id="ba12e-106">成員</span><span class="sxs-lookup"><span data-stu-id="ba12e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ba12e-107">**的**</span><span class="sxs-lookup"><span data-stu-id="ba12e-107">**a**</span></span>
</dt> <dd>

<span data-ttu-id="ba12e-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba12e-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba12e-109">一般平面方程式中裁剪平面的係數。</span><span class="sxs-lookup"><span data-stu-id="ba12e-109">The a coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="ba12e-110">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="ba12e-110">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ba12e-111">**b**</span><span class="sxs-lookup"><span data-stu-id="ba12e-111">**b**</span></span>
</dt> <dd>

<span data-ttu-id="ba12e-112">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba12e-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba12e-113">一般平面方程式中裁剪平面的 b 係數。</span><span class="sxs-lookup"><span data-stu-id="ba12e-113">The b coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="ba12e-114">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="ba12e-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ba12e-115">**c**</span><span class="sxs-lookup"><span data-stu-id="ba12e-115">**c**</span></span>
</dt> <dd>

<span data-ttu-id="ba12e-116">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba12e-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba12e-117">一般平面方程式中裁剪平面的 c 係數。</span><span class="sxs-lookup"><span data-stu-id="ba12e-117">The c coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="ba12e-118">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="ba12e-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ba12e-119">**d**</span><span class="sxs-lookup"><span data-stu-id="ba12e-119">**d**</span></span>
</dt> <dd>

<span data-ttu-id="ba12e-120">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba12e-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ba12e-121">一般平面方程式中裁剪平面的 d 係數。</span><span class="sxs-lookup"><span data-stu-id="ba12e-121">The d coefficient of the clipping plane in the general plane equation.</span></span> <span data-ttu-id="ba12e-122">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="ba12e-122">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba12e-123">備註</span><span class="sxs-lookup"><span data-stu-id="ba12e-123">Remarks</span></span>

<span data-ttu-id="ba12e-124">**D3DXPLANE** 結構的成員採用一般平面方程式的形式。</span><span class="sxs-lookup"><span data-stu-id="ba12e-124">The members of the **D3DXPLANE** structure take the form of the general plane equation.</span></span> <span data-ttu-id="ba12e-125">它們符合一般平面 **方程式，** 因此 x + **b** y + **c** z + **d** w = 0。</span><span class="sxs-lookup"><span data-stu-id="ba12e-125">They fit into the general plane equation so that **a** x + **b** y + **c** z + **d** w = 0.</span></span>

<span data-ttu-id="ba12e-126">C + + 程式設計人員可以利用執行多載的函式和指派、一元和二元 (（包括相等) 運算子的 [**D3DXPLANE 延伸**](d3dxplane-extensions.md) 模組）來利用運算子多載和類型轉換。</span><span class="sxs-lookup"><span data-stu-id="ba12e-126">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXPLANE Extensions**](d3dxplane-extensions.md) which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba12e-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba12e-127">Requirements</span></span>



| <span data-ttu-id="ba12e-128">需求</span><span class="sxs-lookup"><span data-stu-id="ba12e-128">Requirement</span></span> | <span data-ttu-id="ba12e-129">值</span><span class="sxs-lookup"><span data-stu-id="ba12e-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba12e-130">標頭</span><span class="sxs-lookup"><span data-stu-id="ba12e-130">Header</span></span><br/> | <dl> <span data-ttu-id="ba12e-131"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="ba12e-131"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba12e-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba12e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba12e-133">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="ba12e-133">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
