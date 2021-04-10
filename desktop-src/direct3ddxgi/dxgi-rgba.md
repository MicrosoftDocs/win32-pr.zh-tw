---
description: 表示使用 Alpha 的色彩值，用於透明度。
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
ms.openlocfilehash: 77b526e916d43868304c6c01a7dbbe8ebbb5692b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688060"
---
# <a name="dxgi_rgba-structure"></a><span data-ttu-id="65e5f-103">DXGI \_ RGBA 結構</span><span class="sxs-lookup"><span data-stu-id="65e5f-103">DXGI\_RGBA structure</span></span>

<span data-ttu-id="65e5f-104">表示使用 Alpha 的色彩值，用於透明度。</span><span class="sxs-lookup"><span data-stu-id="65e5f-104">Represents a color value with alpha, which is used for transparency.</span></span>

## <a name="syntax"></a><span data-ttu-id="65e5f-105">語法</span><span class="sxs-lookup"><span data-stu-id="65e5f-105">Syntax</span></span>


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
```



## <a name="members"></a><span data-ttu-id="65e5f-106">成員</span><span class="sxs-lookup"><span data-stu-id="65e5f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="65e5f-107">**r**</span><span class="sxs-lookup"><span data-stu-id="65e5f-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="65e5f-108">指定色彩之紅色元件的浮點值。</span><span class="sxs-lookup"><span data-stu-id="65e5f-108">Floating-point value that specifies the red component of a color.</span></span> <span data-ttu-id="65e5f-109">此值通常在0.0 到1.0 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="65e5f-109">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="65e5f-110">值為0.0 表示完全沒有紅色的元件，而值1.0 則表示完全有紅色。</span><span class="sxs-lookup"><span data-stu-id="65e5f-110">A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="65e5f-111">**G**</span><span class="sxs-lookup"><span data-stu-id="65e5f-111">**g**</span></span>
</dt> <dd>

<span data-ttu-id="65e5f-112">指定色彩之綠色元件的浮點值。</span><span class="sxs-lookup"><span data-stu-id="65e5f-112">Floating-point value that specifies the green component of a color.</span></span> <span data-ttu-id="65e5f-113">此值通常在0.0 到1.0 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="65e5f-113">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="65e5f-114">值為0.0 表示完全沒有綠色的元件，而值1.0 表示綠色已完全存在。</span><span class="sxs-lookup"><span data-stu-id="65e5f-114">A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="65e5f-115">**b**</span><span class="sxs-lookup"><span data-stu-id="65e5f-115">**b**</span></span>
</dt> <dd>

<span data-ttu-id="65e5f-116">指定色彩之藍色元件的浮點值。</span><span class="sxs-lookup"><span data-stu-id="65e5f-116">Floating-point value that specifies the blue component of a color.</span></span> <span data-ttu-id="65e5f-117">此值通常在0.0 到1.0 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="65e5f-117">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="65e5f-118">值為0.0 表示完全沒有藍色的元件，而值1.0 則表示藍色已完全存在。</span><span class="sxs-lookup"><span data-stu-id="65e5f-118">A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.</span></span>

</dd> <dt>

<span data-ttu-id="65e5f-119">**的**</span><span class="sxs-lookup"><span data-stu-id="65e5f-119">**a**</span></span>
</dt> <dd>

<span data-ttu-id="65e5f-120">指定色彩之 Alpha 元件的浮點值。</span><span class="sxs-lookup"><span data-stu-id="65e5f-120">Floating-point value that specifies the alpha component of a color.</span></span> <span data-ttu-id="65e5f-121">此值通常在0.0 到1.0 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="65e5f-121">This value generally is in the range from 0.0 through 1.0.</span></span> <span data-ttu-id="65e5f-122">值為0.0 表示完全透明，而值1.0 則表示完全不透明。</span><span class="sxs-lookup"><span data-stu-id="65e5f-122">A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65e5f-123">備註</span><span class="sxs-lookup"><span data-stu-id="65e5f-123">Remarks</span></span>

<span data-ttu-id="65e5f-124">您可以將此結構的成員設定為0到1範圍以外的值，以實行一些不尋常的效果。</span><span class="sxs-lookup"><span data-stu-id="65e5f-124">You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.</span></span> <span data-ttu-id="65e5f-125">大於1的值會產生傾向于將場景沖蝕的強大燈。</span><span class="sxs-lookup"><span data-stu-id="65e5f-125">Values greater than 1 produce strong lights that tend to wash out a scene.</span></span> <span data-ttu-id="65e5f-126">負數值會產生深亮燈，以實際從場景中移除光線。</span><span class="sxs-lookup"><span data-stu-id="65e5f-126">Negative values produce dark lights that actually remove light from a scene.</span></span>

<span data-ttu-id="65e5f-127">DXGItype 標頭類型-將 **DXGI \_ RGBA** 定義為 [**D3DCOLORVALUE**](d3dcolorvalue.md)的別名，如下所示：</span><span class="sxs-lookup"><span data-stu-id="65e5f-127">The DXGItype.h header type-defines **DXGI\_RGBA** as an alias of [**D3DCOLORVALUE**](d3dcolorvalue.md), as follows:</span></span>


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



<span data-ttu-id="65e5f-128">您可以使用 **dxgi \_ RGBA** 搭配 [**IDXGISwapChain1：： SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor)、 [**IDXGISwapChain1：： GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)和 [**dxgi \_ ALPHA \_ 模式**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)。</span><span class="sxs-lookup"><span data-stu-id="65e5f-128">You can use **DXGI\_RGBA** with [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor), and [**DXGI\_ALPHA\_MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).</span></span>

## <a name="requirements"></a><span data-ttu-id="65e5f-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="65e5f-129">Requirements</span></span>



| <span data-ttu-id="65e5f-130">需求</span><span class="sxs-lookup"><span data-stu-id="65e5f-130">Requirement</span></span> | <span data-ttu-id="65e5f-131">值</span><span class="sxs-lookup"><span data-stu-id="65e5f-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65e5f-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65e5f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="65e5f-133">適用于 Windows 7 \[ desktop app \| UWP 應用程式的 Windows 8 和平臺更新\]</span><span class="sxs-lookup"><span data-stu-id="65e5f-133">Windows 8 and Platform Update for Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="65e5f-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65e5f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="65e5f-135">Windows server 2012 和 Windows Server 2008 R2 \[ desktop apps \| UWP 應用程式的平臺更新\]</span><span class="sxs-lookup"><span data-stu-id="65e5f-135">Windows Server 2012 and Platform Update for Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="65e5f-136">標頭</span><span class="sxs-lookup"><span data-stu-id="65e5f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="65e5f-137"><dt>DXGItype。h</dt></span><span class="sxs-lookup"><span data-stu-id="65e5f-137"><dt>DXGItype.h</dt></span></span> </dl>                      |



## <a name="see-also"></a><span data-ttu-id="65e5f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65e5f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65e5f-139">DXGI 結構</span><span class="sxs-lookup"><span data-stu-id="65e5f-139">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[<span data-ttu-id="65e5f-140">**D3DCOLORVALUE**</span><span class="sxs-lookup"><span data-stu-id="65e5f-140">**D3DCOLORVALUE**</span></span>](d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="65e5f-141">**Direct3D 9 中的 D3DCOLORVALUE ()**</span><span class="sxs-lookup"><span data-stu-id="65e5f-141">**D3DCOLORVALUE (in Direct3D 9)**</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
