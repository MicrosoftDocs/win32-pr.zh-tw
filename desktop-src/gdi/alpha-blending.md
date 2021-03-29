---
description: Alpha 混色用來顯示 Alpha 點陣圖，也就是具有透明或半透明圖元的點陣圖。
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: " (Windows GDI) 的 Alpha 混合"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68cb34d189fb80d23cbb5eeec9d9006aa93a1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972785"
---
# <a name="alpha-blending-windows-gdi"></a><span data-ttu-id="bd62a-103"> (Windows GDI) 的 Alpha 混合</span><span class="sxs-lookup"><span data-stu-id="bd62a-103">Alpha Blending (Windows GDI)</span></span>

<span data-ttu-id="bd62a-104">*Alpha 混色* 用來顯示 Alpha 點陣圖，也就是具有透明或半透明圖元的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="bd62a-104">*Alpha blending* is used to display an alpha bitmap, which is a bitmap that has transparent or semi-transparent pixels.</span></span> <span data-ttu-id="bd62a-105">除了紅色、綠色和藍色色頻外，Alpha 點陣圖中的每個圖元都有一個透明元件，稱為 *Alpha* 色板。</span><span class="sxs-lookup"><span data-stu-id="bd62a-105">In addition to a red, green, and blue color channel, each pixel in an alpha bitmap has a transparency component known as its *alpha channel*.</span></span> <span data-ttu-id="bd62a-106">Alpha 色板通常會包含與色頻一樣多的位數。</span><span class="sxs-lookup"><span data-stu-id="bd62a-106">The alpha channel typically contains as many bits as a color channel.</span></span> <span data-ttu-id="bd62a-107">例如，8位 Alpha 通道可以代表256的透明度層級，從 0 (整個點陣圖) 至 255 (整個點陣圖是不透明的) 。</span><span class="sxs-lookup"><span data-stu-id="bd62a-107">For example, an 8-bit alpha channel can represent 256 levels of transparency, from 0 (the entire bitmap is transparent) to 255 (the entire bitmap is opaque).</span></span>

<span data-ttu-id="bd62a-108">藉由呼叫 [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend)來叫用 Alpha 混色機制，它會參考 [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) 結構。</span><span class="sxs-lookup"><span data-stu-id="bd62a-108">Alpha blending mechanisms are invoked by calling [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), which references the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span>

<span data-ttu-id="bd62a-109">只有 32-bpp BI RGB 支援每圖元的 Alpha 值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bd62a-109">Alpha values per pixel are only supported for 32-bpp BI\_RGB.</span></span> <span data-ttu-id="bd62a-110">此公式定義如下：</span><span class="sxs-lookup"><span data-stu-id="bd62a-110">This formula is defined as:</span></span>


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



<span data-ttu-id="bd62a-111">這會在記憶體中表示，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="bd62a-111">This is represented in memory as shown in the following table.</span></span>



|       |       |       |       |
|-------|-------|-------|-------|
| <span data-ttu-id="bd62a-112">31:24</span><span class="sxs-lookup"><span data-stu-id="bd62a-112">31:24</span></span> | <span data-ttu-id="bd62a-113">23:16</span><span class="sxs-lookup"><span data-stu-id="bd62a-113">23:16</span></span> | <span data-ttu-id="bd62a-114">15:08</span><span class="sxs-lookup"><span data-stu-id="bd62a-114">15:08</span></span> | <span data-ttu-id="bd62a-115">07:00</span><span class="sxs-lookup"><span data-stu-id="bd62a-115">07:00</span></span> |
| <span data-ttu-id="bd62a-116">Alpha</span><span class="sxs-lookup"><span data-stu-id="bd62a-116">Alpha</span></span> | <span data-ttu-id="bd62a-117">紅色</span><span class="sxs-lookup"><span data-stu-id="bd62a-117">Red</span></span>   | <span data-ttu-id="bd62a-118">綠色</span><span class="sxs-lookup"><span data-stu-id="bd62a-118">Green</span></span> | <span data-ttu-id="bd62a-119">藍色</span><span class="sxs-lookup"><span data-stu-id="bd62a-119">Blue</span></span>  |



 

<span data-ttu-id="bd62a-120">點陣圖也可能會以套用至整個點陣圖的透明因數來顯示。</span><span class="sxs-lookup"><span data-stu-id="bd62a-120">Bitmaps may also be displayed with a transparency factor applied to the entire bitmap.</span></span> <span data-ttu-id="bd62a-121">您可以藉由在 [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction)結構中設定 **SourceConstantAlpha** ，來顯示任何點陣圖格式和全域常數 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="bd62a-121">Any bitmap format can be displayed with a global constant alpha value by setting **SourceConstantAlpha** in the [**BLENDFUNCTION**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) structure.</span></span> <span data-ttu-id="bd62a-122">全域常數 Alpha 值具有256的透明度層級，從 0 (整個點陣圖完全透明) 至 255 (整個點陣圖完全不透明) 。</span><span class="sxs-lookup"><span data-stu-id="bd62a-122">The global constant alpha value has 256 levels of transparency, from 0 (entire bitmap is completely transparent) to 255 (entire bitmap is completely opaque).</span></span> <span data-ttu-id="bd62a-123">全域常數 Alpha 值會與每圖元的 Alpha 值結合。</span><span class="sxs-lookup"><span data-stu-id="bd62a-123">The global constant alpha value is combined with the per-pixel alpha value.</span></span>

<span data-ttu-id="bd62a-124">如需範例，請參閱 [Alpha 混色點陣圖](alpha-blending-a-bitmap.md)。</span><span class="sxs-lookup"><span data-stu-id="bd62a-124">For an example, see [Alpha Blending a Bitmap](alpha-blending-a-bitmap.md).</span></span>

 

 



