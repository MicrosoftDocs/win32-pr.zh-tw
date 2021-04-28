---
description: D3DXCOLOR 結構 (D3dx9math) -描述色彩值。
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: 'D3DXCOLOR 結構 (D3dx9math .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 58b02abc49b695169674a2579b73dc2359801a73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115926"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a><span data-ttu-id="ce170-103">D3DXCOLOR 結構 (D3dx9math .h) </span><span class="sxs-lookup"><span data-stu-id="ce170-103">D3DXCOLOR structure (D3dx9math.h)</span></span>

<span data-ttu-id="ce170-104">描述色彩值。</span><span class="sxs-lookup"><span data-stu-id="ce170-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce170-105">語法</span><span class="sxs-lookup"><span data-stu-id="ce170-105">Syntax</span></span>


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a><span data-ttu-id="ce170-106">成員</span><span class="sxs-lookup"><span data-stu-id="ce170-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ce170-107">**r**</span><span class="sxs-lookup"><span data-stu-id="ce170-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="ce170-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce170-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ce170-109">色彩的紅色元件。</span><span class="sxs-lookup"><span data-stu-id="ce170-109">Red component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="ce170-110">**G**</span><span class="sxs-lookup"><span data-stu-id="ce170-110">**g**</span></span>
</dt> <dd>

<span data-ttu-id="ce170-111">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce170-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ce170-112">色彩的綠色元件。</span><span class="sxs-lookup"><span data-stu-id="ce170-112">Green component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="ce170-113">**b**</span><span class="sxs-lookup"><span data-stu-id="ce170-113">**b**</span></span>
</dt> <dd>

<span data-ttu-id="ce170-114">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce170-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ce170-115">色彩的藍色元件。</span><span class="sxs-lookup"><span data-stu-id="ce170-115">Blue component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="ce170-116">**的**</span><span class="sxs-lookup"><span data-stu-id="ce170-116">**a**</span></span>
</dt> <dd>

<span data-ttu-id="ce170-117">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce170-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ce170-118">色彩的 Alpha 元件。</span><span class="sxs-lookup"><span data-stu-id="ce170-118">Alpha component of the color.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce170-119">備註</span><span class="sxs-lookup"><span data-stu-id="ce170-119">Remarks</span></span>

<span data-ttu-id="ce170-120">C + + 程式設計人員可以利用 [**D3DXCOLOR 擴充**](d3dxcolor-extensions.md)功能來利用運算子多載和類型轉換，以執行多載的函式，以及指派、一元和二元 (包括相等) 運算子。</span><span class="sxs-lookup"><span data-stu-id="ce170-120">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXCOLOR Extensions**](d3dxcolor-extensions.md), which implement overloaded constructors, as well as assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce170-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce170-121">Requirements</span></span>



| <span data-ttu-id="ce170-122">需求</span><span class="sxs-lookup"><span data-stu-id="ce170-122">Requirement</span></span> | <span data-ttu-id="ce170-123">值</span><span class="sxs-lookup"><span data-stu-id="ce170-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce170-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ce170-124">Header</span></span><br/> | <dl> <span data-ttu-id="ce170-125"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce170-125"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce170-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce170-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce170-127">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="ce170-127">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
