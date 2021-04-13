---
description: 表示使用 Alpha 的色彩值，用於透明度。
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
title: 'D3DCOLORVALUE 結構 (Dxgitype .h) '
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
- dxgitype.h
ms.openlocfilehash: 2b7d768af9e471f3183c6a400622c2b0e0719a2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322880"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a><span data-ttu-id="3e4f4-103">D3DCOLORVALUE 結構 (Dxgitype .h) </span><span class="sxs-lookup"><span data-stu-id="3e4f4-103">D3DCOLORVALUE structure (Dxgitype.h)</span></span>

<span data-ttu-id="3e4f4-104">表示使用 Alpha 的色彩值，用於透明度。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e4f4-105">語法</span><span class="sxs-lookup"><span data-stu-id="3e4f4-105">Syntax</span></span>


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a><span data-ttu-id="3e4f4-106">成員</span><span class="sxs-lookup"><span data-stu-id="3e4f4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3e4f4-107">**r**</span><span class="sxs-lookup"><span data-stu-id="3e4f4-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="3e4f4-108">指定色彩之紅色元件的浮點值。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="3e4f4-109">此值通常在0.0 到1.0 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="3e4f4-110">值為0.0 表示完全沒有紅色的元件，而值1.0 則表示完全有紅色。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="3e4f4-111">**G**</span><span class="sxs-lookup"><span data-stu-id="3e4f4-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="3e4f4-112">指定色彩之綠色元件的浮點值。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="3e4f4-113">此值通常在0.0 到1.0 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="3e4f4-114">值為0.0 表示完全沒有綠色的元件，而值1.0 表示綠色已完全存在。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="3e4f4-115">**b**</span><span class="sxs-lookup"><span data-stu-id="3e4f4-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="3e4f4-116">指定色彩之藍色元件的浮點值。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="3e4f4-117">此值通常在0.0 到1.0 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="3e4f4-118">值為0.0 表示完全沒有藍色的元件，而值1.0 則表示藍色已完全存在。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="3e4f4-119">**的**</span><span class="sxs-lookup"><span data-stu-id="3e4f4-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="3e4f4-120">指定色彩之 Alpha 元件的浮點值。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="3e4f4-121">此值通常在0.0 到1.0 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="3e4f4-122">值為0.0 表示完全透明，而值1.0 則表示完全不透明。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e4f4-123">備註</span><span class="sxs-lookup"><span data-stu-id="3e4f4-123">Remarks</span></span>

<span data-ttu-id="3e4f4-124">您可以將此結構的成員設定為0到1範圍以外的值，以實行一些不尋常的效果。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="3e4f4-125">大於1的值會產生傾向于將場景沖蝕的強大燈。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="3e4f4-126">負數值會產生深亮燈，以實際從場景中移除光線。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="3e4f4-127">DXGItype 標頭類型-將 [**DXGI \_ RGBA**](dxgi-rgba.md) 定義為 **D3DCOLORVALUE** 的別名，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3e4f4-127">The DXGItype.h header type-defines [**DXGI\_RGBA**](dxgi-rgba.md) as an alias of **D3DCOLORVALUE**, as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="3e4f4-128">您可以使用 D3DCOLORVALUE 或 [**dxgi \_ RGBA**](dxgi-rgba.md) 搭配 [**IDXGISwapChain1：： SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor)、 [**IDXGISwapChain1：： GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)和 [**DXGI \_ ALPHA \_ 模式**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)。</span><span class="sxs-lookup"><span data-stu-id="3e4f4-128">You can use D3DCOLORVALUE or [**DXGI\_RGBA**](dxgi-rgba.md) with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e4f4-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e4f4-129">Requirements</span></span>



| <span data-ttu-id="3e4f4-130">需求</span><span class="sxs-lookup"><span data-stu-id="3e4f4-130">Requirement</span></span> | <span data-ttu-id="3e4f4-131">值</span><span class="sxs-lookup"><span data-stu-id="3e4f4-131">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3e4f4-132">標頭</span><span class="sxs-lookup"><span data-stu-id="3e4f4-132">Header</span></span><br/> | <dl> <span data-ttu-id="3e4f4-133"><dt>Dxgitype。h</dt></span><span class="sxs-lookup"><span data-stu-id="3e4f4-133"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e4f4-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e4f4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e4f4-135">DXGI 結構</span><span class="sxs-lookup"><span data-stu-id="3e4f4-135">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="3e4f4-136">**DXGI \_ RGBA**</span><span class="sxs-lookup"><span data-stu-id="3e4f4-136">**DXGI\_RGBA**</span></span>](dxgi-rgba.md)
</dt> </dl>

 

 




