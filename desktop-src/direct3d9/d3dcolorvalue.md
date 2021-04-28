---
description: D3DCOLORVALUE 結構 (D3D9Types) -描述色彩值。
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: 'D3DCOLORVALUE 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c9b55fbf718382e9dca7e3999cce0cabe895a261
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116056"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a><span data-ttu-id="07a12-103">D3DCOLORVALUE 結構 (D3D9Types .h) </span><span class="sxs-lookup"><span data-stu-id="07a12-103">D3DCOLORVALUE structure (D3D9Types.h)</span></span>

<span data-ttu-id="07a12-104">描述色彩值。</span><span class="sxs-lookup"><span data-stu-id="07a12-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="07a12-105">語法</span><span class="sxs-lookup"><span data-stu-id="07a12-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="07a12-106">成員</span><span class="sxs-lookup"><span data-stu-id="07a12-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="07a12-107">**r**</span><span class="sxs-lookup"><span data-stu-id="07a12-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="07a12-108">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="07a12-108">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="07a12-109">指定色彩之紅色元件的浮點值。</span><span class="sxs-lookup"><span data-stu-id="07a12-109">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="07a12-110">此值通常在0.0 到1.0 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="07a12-110">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="07a12-111">值為0.0 表示完全沒有紅色的元件，而值1.0 則表示完全有紅色。</span><span class="sxs-lookup"><span data-stu-id="07a12-111">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="07a12-112">**G**</span><span class="sxs-lookup"><span data-stu-id="07a12-112">**g**</span></span>
</dt> <dd>

<span data-ttu-id="07a12-113">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="07a12-113">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="07a12-114">指定色彩之綠色元件的浮點值。</span><span class="sxs-lookup"><span data-stu-id="07a12-114">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="07a12-115">此值通常在0.0 到1.0 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="07a12-115">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="07a12-116">值為0.0 表示完全沒有綠色的元件，而值1.0 表示綠色已完全存在。</span><span class="sxs-lookup"><span data-stu-id="07a12-116">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="07a12-117">**b**</span><span class="sxs-lookup"><span data-stu-id="07a12-117">**b**</span></span>
</dt> <dd>

<span data-ttu-id="07a12-118">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="07a12-118">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="07a12-119">指定色彩之藍色元件的浮點值。</span><span class="sxs-lookup"><span data-stu-id="07a12-119">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="07a12-120">此值通常在0.0 到1.0 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="07a12-120">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="07a12-121">值為0.0 表示完全沒有藍色的元件，而值1.0 則表示藍色已完全存在。</span><span class="sxs-lookup"><span data-stu-id="07a12-121">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="07a12-122">**的**</span><span class="sxs-lookup"><span data-stu-id="07a12-122">**a**</span></span>
</dt> <dd>

<span data-ttu-id="07a12-123">類型： **float**</span><span class="sxs-lookup"><span data-stu-id="07a12-123">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="07a12-124">指定色彩之 Alpha 元件的浮點值。</span><span class="sxs-lookup"><span data-stu-id="07a12-124">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="07a12-125">此值通常在0.0 到1.0 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="07a12-125">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="07a12-126">值為0.0 表示完全透明，而值1.0 則表示完全不透明。</span><span class="sxs-lookup"><span data-stu-id="07a12-126">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07a12-127">備註</span><span class="sxs-lookup"><span data-stu-id="07a12-127">Remarks</span></span>

<span data-ttu-id="07a12-128">您可以將此結構的成員設定為0到1範圍以外的值，以實行一些不尋常的效果。</span><span class="sxs-lookup"><span data-stu-id="07a12-128">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="07a12-129">大於1的值會產生傾向于將場景沖蝕的強大燈。</span><span class="sxs-lookup"><span data-stu-id="07a12-129">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="07a12-130">負數值會產生深亮燈，以實際從場景中移除光線。</span><span class="sxs-lookup"><span data-stu-id="07a12-130">Negative values produce dark lights that actually remove light from a scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="07a12-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="07a12-131">Requirements</span></span>



| <span data-ttu-id="07a12-132">需求</span><span class="sxs-lookup"><span data-stu-id="07a12-132">Requirement</span></span> | <span data-ttu-id="07a12-133">值</span><span class="sxs-lookup"><span data-stu-id="07a12-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07a12-134">標頭</span><span class="sxs-lookup"><span data-stu-id="07a12-134">Header</span></span><br/> | <dl> <span data-ttu-id="07a12-135"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="07a12-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07a12-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07a12-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07a12-137">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="07a12-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




