---
title: 調色板
description: 調色板
ms.assetid: ee048f9a-3036-40dc-a6d7-f612b9ef767c
keywords:
- DrawDib，調色板
- DrawDibRealize 函式
- DrawDibDraw 函式
- DrawDibSetPalette 函式
- DrawDibGetPalette 函式
- DrawDibChangePalette 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5935831d8996c424a386f86082282f9cf7c1c12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933195"
---
# <a name="palettes"></a><span data-ttu-id="93b5f-109">調色板</span><span class="sxs-lookup"><span data-stu-id="93b5f-109">Palettes</span></span>

<span data-ttu-id="93b5f-110">DrawDib 函式要求應用程式必須回應兩個以元件為導向的訊息： [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) 和 [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged)。</span><span class="sxs-lookup"><span data-stu-id="93b5f-110">The DrawDib functions require that an application respond to two palette-oriented messages: [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) and [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged).</span></span> <span data-ttu-id="93b5f-111">如果您的應用程式不是可辨識的元件，您必須為每個訊息加入處理常式。</span><span class="sxs-lookup"><span data-stu-id="93b5f-111">If your application is not palette-aware, you will need to add a handler for each of these messages.</span></span> <span data-ttu-id="93b5f-112">如需處理 **wm \_ QUERYNEWPALETTE** 和 **WM \_ PALETTECHANGED** 訊息的詳細資訊，請參閱 [加入調色板訊息處理常式](adding-palette-message-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="93b5f-112">For more information about processing the **WM\_QUERYNEWPALETTE** and **WM\_PALETTECHANGED** messages, see [Adding Palette Message Handlers](adding-palette-message-handlers.md).</span></span>

<span data-ttu-id="93b5f-113">您可以使用 [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) 函式，將目前的 DrawDib 調色板實現到 DC。</span><span class="sxs-lookup"><span data-stu-id="93b5f-113">You can realize the current DrawDib palette to the DC by using the [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) function.</span></span> <span data-ttu-id="93b5f-114">您應該瞭解選擇區以回應 [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) 或 [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) 訊息，或是當您準備使用 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 函式來顯示影像序列時。</span><span class="sxs-lookup"><span data-stu-id="93b5f-114">You should realize the palette in response to the [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) or [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) message, or when you prepare to display an image sequence by using the [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) function.</span></span>

<span data-ttu-id="93b5f-115">您可以使用 [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) 函式，繪製對應到另一個調色板的影像。</span><span class="sxs-lookup"><span data-stu-id="93b5f-115">You can draw an image mapped to another palette by using the [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) function.</span></span> <span data-ttu-id="93b5f-116">此函式會強制 DrawDib DC 使用指定的調色板，這可能會影響影像品質。</span><span class="sxs-lookup"><span data-stu-id="93b5f-116">This function forces the DrawDib DC to use the specified palette, which can affect the image quality.</span></span> <span data-ttu-id="93b5f-117">例如，具有調色板感知的應用程式可能已經實現了一個調色板，而且需要防止 DrawDib 取得自己的調色板。</span><span class="sxs-lookup"><span data-stu-id="93b5f-117">For example, an application that is palette-aware might have realized a palette and needs to prevent DrawDib from realizing its own palette.</span></span> <span data-ttu-id="93b5f-118">應用程式可以使用 **DrawDibSetPalette** 通知 DrawDib 要使用的調色板。</span><span class="sxs-lookup"><span data-stu-id="93b5f-118">The application can use **DrawDibSetPalette** to notify DrawDib of the palette to use.</span></span>

<span data-ttu-id="93b5f-119">您可以使用 [**DrawDibGetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetpalette) 函數來取得目前前景調色板的控制碼。</span><span class="sxs-lookup"><span data-stu-id="93b5f-119">You can obtain a handle of the current foreground palette by using the [**DrawDibGetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetpalette) function.</span></span> <span data-ttu-id="93b5f-120">如果您的應用程式使用目前的前景調色板，它並不會獨佔使用此元件，而另一個應用程式可能會使調色板控制碼失效。</span><span class="sxs-lookup"><span data-stu-id="93b5f-120">If your application uses the current foreground palette, it does not have exclusive use of the palette and another application can invalidate the palette handle.</span></span> <span data-ttu-id="93b5f-121">當您的應用程式使用完畢時，您的應用程式不應該釋出該調色板。</span><span class="sxs-lookup"><span data-stu-id="93b5f-121">Your application should not free the palette when you finish using it.</span></span> <span data-ttu-id="93b5f-122">釋放調色板可能使另一個應用程式的調色板控制碼失效。</span><span class="sxs-lookup"><span data-stu-id="93b5f-122">Freeing the palette could invalidate the palette handle for another application.</span></span>

<span data-ttu-id="93b5f-123">您可以使用 [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette) 函數來準備 DrawDib，以接收其調色板的新色彩值。</span><span class="sxs-lookup"><span data-stu-id="93b5f-123">You can prepare DrawDib to receive new color values for its palette by using the [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette) function.</span></span> <span data-ttu-id="93b5f-124">在 **DrawDibChangePalette** 之後的程式碼中，您可以為 [調色板色彩表] 指派新值。</span><span class="sxs-lookup"><span data-stu-id="93b5f-124">In the code following **DrawDibChangePalette**, you assign new values for the palette color table.</span></span> <span data-ttu-id="93b5f-125">當您呼叫 **DrawDibChangePalette** 時，如果 DrawDib DC 中未設定 **DDF \_ 動畫** 旗標，您可以使用 [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize)來實現調色板的變更。</span><span class="sxs-lookup"><span data-stu-id="93b5f-125">If the **DDF\_ANIMATE** flag is not set in the DrawDib DC when you call **DrawDibChangePalette**, you can enact the palette changes by using [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) to realize the palette.</span></span> <span data-ttu-id="93b5f-126">然後，您可以使用 [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) 來重繪映射。</span><span class="sxs-lookup"><span data-stu-id="93b5f-126">You can then use [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) to redraw the image.</span></span> <span data-ttu-id="93b5f-127">如果已在 DrawDib DC 中設定 **DDF \_ 動畫** 旗標，您可以使用 **DrawDibDraw** 或 **DrawDibRealize**，以動畫顯示調色板以及顯示點陣圖的色彩。</span><span class="sxs-lookup"><span data-stu-id="93b5f-127">If the **DDF\_ANIMATE** flag is set in the DrawDib DC, you can animate the palette and the colors of the displayed bitmap by using **DrawDibDraw** or **DrawDibRealize**.</span></span> <span data-ttu-id="93b5f-128">您可以使用 [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend)和 [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)函數來更新 **DDF \_ 動畫** 旗標。</span><span class="sxs-lookup"><span data-stu-id="93b5f-128">You can update the **DDF\_ANIMATE** flag by using the [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) and [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) functions.</span></span>

> [!Note]  
> <span data-ttu-id="93b5f-129">如果您在 DC 選取 DrawDib 元件時將其釋出，當 DC 使用調色板時，會導致圖形裝置介面 (GDI) 錯誤。</span><span class="sxs-lookup"><span data-stu-id="93b5f-129">If you free the DrawDib palette while it is selected by a DC, a graphics device interface (GDI) error can result when the DC uses the palette.</span></span> <span data-ttu-id="93b5f-130">相反地，您的應用程式應該使用 [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) 來變更 DrawDib DC，以使用預設的調色板或其他調色板。</span><span class="sxs-lookup"><span data-stu-id="93b5f-130">Instead, your application should use [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) to change the DrawDib DC to use the default palette or another palette.</span></span>

 

<span data-ttu-id="93b5f-131">[**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend)、 [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose)和 [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin)函數可以釋放 DrawDib 調色板。</span><span class="sxs-lookup"><span data-stu-id="93b5f-131">The [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend), [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose), and [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) functions can free the DrawDib palette.</span></span> <span data-ttu-id="93b5f-132">不過，只有當 DC 尚未選取元件時，才應該使用這些函數。</span><span class="sxs-lookup"><span data-stu-id="93b5f-132">However, these functions should be used only when the palette has not been selected by the DC.</span></span> <span data-ttu-id="93b5f-133">DrawDibDraw 函式使用相同的 DrawDib DC 時，也可以釋出調色板，但會指定不同的繪圖參數 (*lpbi*、 *dxDst*、 *dyDst*、 *dxSrc* 或 *dySrc*) 或不同的格式。</span><span class="sxs-lookup"><span data-stu-id="93b5f-133">The DrawDibDraw function can also free the palette when it uses the same DrawDib DC, but specifies different drawing parameters (*lpbi*, *dxDst*, *dyDst*, *dxSrc*, or *dySrc*) or a different format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93b5f-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="93b5f-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93b5f-135">影像轉譯</span><span class="sxs-lookup"><span data-stu-id="93b5f-135">Image Rendering</span></span>](image-rendering.md)
</dt> </dl>

 

 