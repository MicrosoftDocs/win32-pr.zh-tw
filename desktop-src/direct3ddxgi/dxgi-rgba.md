---
description: DXGI_RGBA 結構-表示使用 Alpha 的色彩值，用於透明度。
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: 'DXGI_RGBA 結構 (DXGItype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_RGBA
api_type:
- HeaderDef
api_location:
- DXGItype.h
ms.openlocfilehash: b0447d6470401d4136fbfd36f6d9c089e331b14b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114266"
---
# <a name="dxgi_rgba-structure"></a><span data-ttu-id="41de9-103">DXGI \_ RGBA 結構</span><span class="sxs-lookup"><span data-stu-id="41de9-103">DXGI\_RGBA structure</span></span>

<span data-ttu-id="41de9-104">表示使用 Alpha 的色彩值，用於透明度。</span><span class="sxs-lookup"><span data-stu-id="41de9-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="41de9-105">語法</span><span class="sxs-lookup"><span data-stu-id="41de9-105">Syntax</span></span>


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
```



## <a name="members"></a><span data-ttu-id="41de9-106">成員</span><span class="sxs-lookup"><span data-stu-id="41de9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="41de9-107">**r**</span><span class="sxs-lookup"><span data-stu-id="41de9-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="41de9-108">指定色彩之紅色元件的浮點值。</span><span class="sxs-lookup"><span data-stu-id="41de9-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="41de9-109">此值通常在0.0 到1.0 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="41de9-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="41de9-110">值為0.0 表示完全沒有紅色的元件，而值1.0 則表示完全有紅色。</span><span class="sxs-lookup"><span data-stu-id="41de9-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="41de9-111">**G**</span><span class="sxs-lookup"><span data-stu-id="41de9-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="41de9-112">指定色彩之綠色元件的浮點值。</span><span class="sxs-lookup"><span data-stu-id="41de9-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="41de9-113">此值通常在0.0 到1.0 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="41de9-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="41de9-114">值為0.0 表示完全沒有綠色的元件，而值1.0 表示綠色已完全存在。</span><span class="sxs-lookup"><span data-stu-id="41de9-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="41de9-115">**b**</span><span class="sxs-lookup"><span data-stu-id="41de9-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="41de9-116">指定色彩之藍色元件的浮點值。</span><span class="sxs-lookup"><span data-stu-id="41de9-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="41de9-117">此值通常在0.0 到1.0 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="41de9-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="41de9-118">值為0.0 表示完全沒有藍色的元件，而值1.0 則表示藍色已完全存在。</span><span class="sxs-lookup"><span data-stu-id="41de9-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="41de9-119">**的**</span><span class="sxs-lookup"><span data-stu-id="41de9-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="41de9-120">指定色彩之 Alpha 元件的浮點值。</span><span class="sxs-lookup"><span data-stu-id="41de9-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="41de9-121">此值通常在0.0 到1.0 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="41de9-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="41de9-122">值為0.0 表示完全透明，而值1.0 則表示完全不透明。</span><span class="sxs-lookup"><span data-stu-id="41de9-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41de9-123">備註</span><span class="sxs-lookup"><span data-stu-id="41de9-123">Remarks</span></span>

<span data-ttu-id="41de9-124">您可以將此結構的成員設定為0到1範圍以外的值，以實行一些不尋常的效果。</span><span class="sxs-lookup"><span data-stu-id="41de9-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="41de9-125">大於1的值會產生傾向于將場景沖蝕的強大燈。</span><span class="sxs-lookup"><span data-stu-id="41de9-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="41de9-126">負數值會產生深亮燈，以實際從場景中移除光線。</span><span class="sxs-lookup"><span data-stu-id="41de9-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="41de9-127">DXGItype 標頭類型-將 **DXGI \_ RGBA** 定義為 [**D3DCOLORVALUE**](d3dcolorvalue.md)的別名，如下所示：</span><span class="sxs-lookup"><span data-stu-id="41de9-127">The DXGItype.h header type-defines **DXGI\_RGBA** as an alias of [**D3DCOLORVALUE**](d3dcolorvalue.md), as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="41de9-128">您可以使用 **dxgi \_ RGBA** 搭配 [**IDXGISwapChain1：： SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor)、 [**IDXGISwapChain1：： GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)和 [**dxgi \_ ALPHA \_ 模式**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)。</span><span class="sxs-lookup"><span data-stu-id="41de9-128">You can use **DXGI\_RGBA** with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="41de9-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="41de9-129">Requirements</span></span>



| <span data-ttu-id="41de9-130">需求</span><span class="sxs-lookup"><span data-stu-id="41de9-130">Requirement</span></span> | <span data-ttu-id="41de9-131">值</span><span class="sxs-lookup"><span data-stu-id="41de9-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41de9-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41de9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="41de9-133">適用于 Windows 7 \[ desktop app \| UWP 應用程式的 Windows 8 和平臺更新\]</span><span class="sxs-lookup"><span data-stu-id="41de9-133">Windows 8 and Platform Update for Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="41de9-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41de9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="41de9-135">Windows server 2012 和 Windows Server 2008 R2 \[ desktop apps \| UWP 應用程式的平臺更新\]</span><span class="sxs-lookup"><span data-stu-id="41de9-135">Windows Server 2012 and Platform Update for Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="41de9-136">標頭</span><span class="sxs-lookup"><span data-stu-id="41de9-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="41de9-137"><dt>DXGItype。h</dt></span><span class="sxs-lookup"><span data-stu-id="41de9-137"><dt>DXGItype.h</dt></span></span> </dl>                      |



## <a name="see-also"></a><span data-ttu-id="41de9-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41de9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41de9-139">DXGI 結構</span><span class="sxs-lookup"><span data-stu-id="41de9-139">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="41de9-140">**D3DCOLORVALUE**</span><span class="sxs-lookup"><span data-stu-id="41de9-140">**D3DCOLORVALUE**</span></span>](d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="41de9-141">**Direct3D 9 中的 D3DCOLORVALUE ()**</span><span class="sxs-lookup"><span data-stu-id="41de9-141">**D3DCOLORVALUE (in Direct3D 9)**</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
