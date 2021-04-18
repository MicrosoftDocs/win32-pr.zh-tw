---
title: 使用調色板
description: 使用調色板
ms.assetid: 0ad0d78b-4c2c-499c-ad5e-8324b59e89fc
keywords:
- WM_CAP_PAL_PASTE 訊息
- capPalettePaste 宏
- WM_CAP_PAL_OPEN 訊息
- capPaletteOpen 宏
- WM_CAP_PAL_AUTOCREATE 訊息
- capPaletteAuto 宏
- WM_CAP_PAL_MANUALCREATE 訊息
- capPaletteManual 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09cbbe3ffc8ea21d1ecf8545f036f5ba6dfb927
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968622"
---
# <a name="working-with-palettes"></a><span data-ttu-id="e58ce-111">使用調色板</span><span class="sxs-lookup"><span data-stu-id="e58ce-111">Working with Palettes</span></span>

<span data-ttu-id="e58ce-112">一開始，如果影片拍攝格式需要調色板，則 [捕獲] 視窗會使用 capture 驅動程式所提供的調色板。</span><span class="sxs-lookup"><span data-stu-id="e58ce-112">Initially, if the video capture format requires a palette, the capture window uses the palette supplied by the capture driver.</span></span> <span data-ttu-id="e58ce-113">這個調色板可能包含黑白重制的灰色縮放值，或廣泛的色彩值選取。</span><span class="sxs-lookup"><span data-stu-id="e58ce-113">This palette might consist of gray-scale values for black-and-white reproduction, or a broad selection of color values.</span></span> <span data-ttu-id="e58ce-114">您可以使用 [ [**wm \_ cap \_ pal \_ 貼**](wm-cap-pal-paste.md) 上] 或 [ [**wm \_ cap \_ pal \_ 開啟**](wm-cap-pal-open.md) 訊息 (] 或 [ [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) 或 [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) 宏]) ，來取出現有的調色板來取代預設的調色板。</span><span class="sxs-lookup"><span data-stu-id="e58ce-114">You can retrieve an existing palette to replace the default palette by using the [**WM\_CAP\_PAL\_PASTE**](wm-cap-pal-paste.md) or [**WM\_CAP\_PAL\_OPEN**](wm-cap-pal-open.md) message (or the [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) or [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) macro).</span></span> <span data-ttu-id="e58ce-115">或者，您也可以建立自訂調色盤來取代預設的調色板，方法是使用 [**WM \_ cap \_ pal \_**](wm-cap-pal-autocreate.md) 自動建立或 [**WM \_ cap \_ pal \_ MANUALCREATE**](wm-cap-pal-manualcreate.md) message (或 [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) 或 [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) 宏) 。</span><span class="sxs-lookup"><span data-stu-id="e58ce-115">Alternatively, you can create a custom palette to replace the default palette by using the [**WM\_CAP\_PAL\_AUTOCREATE**](wm-cap-pal-autocreate.md) or [**WM\_CAP\_PAL\_MANUALCREATE**](wm-cap-pal-manualcreate.md) message (or the [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) or [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) macro).</span></span> <span data-ttu-id="e58ce-116">取代預設的調色板之後，[捕獲] 視窗和驅動程式會使用取代的調色板，直到您建立或開啟另一個調色板為止。</span><span class="sxs-lookup"><span data-stu-id="e58ce-116">After you replace the default palette, the capture window and driver use the replacement palette until you create or open another palette.</span></span>

<span data-ttu-id="e58ce-117">WM \_ cap pal 自動建立 \_ \_ 或 WM \_ cap \_ pal \_ MANUALCREATE 訊息會根據目前的影片輸入建立優化的調色板。</span><span class="sxs-lookup"><span data-stu-id="e58ce-117">The WM\_CAP\_PAL\_AUTOCREATE or WM\_CAP\_PAL\_MANUALCREATE message creates an optimized palette based on the current video input.</span></span> <span data-ttu-id="e58ce-118">此自訂調色盤提供最佳色彩精確度的影片順序，因為它是以存在於序列中的色彩為基礎。</span><span class="sxs-lookup"><span data-stu-id="e58ce-118">This custom palette gives a video sequence the best color fidelity because it is based on colors that exist in the sequence.</span></span> <span data-ttu-id="e58ce-119">[Capture （capture）] 視窗會建立其範例色彩的三維長條圖。</span><span class="sxs-lookup"><span data-stu-id="e58ce-119">The capture window creates a three-dimensional histogram of the colors it samples.</span></span> <span data-ttu-id="e58ce-120">它會藉由檢查相鄰色彩之間的絕對誤差，並以最小誤差值進行合併，來減少色彩數目。</span><span class="sxs-lookup"><span data-stu-id="e58ce-120">It reduces the number of colors by examining the absolute error between adjacent colors and consolidating those with the smallest error value.</span></span>

<span data-ttu-id="e58ce-121">當您自動加入 WM \_ CAP \_ PAL 時 \_ ，您必須指定 AVICap 至範例的框架數目，並指定色調色板的大小。</span><span class="sxs-lookup"><span data-stu-id="e58ce-121">When sending WM\_CAP\_PAL\_AUTOCREATE, you must specify the number of frames for AVICap to sample, and specify the size of the color palette.</span></span> <span data-ttu-id="e58ce-122">指定畫面格數目時，請包含足夠的畫面格，以確保會取樣序列中的所有色彩。</span><span class="sxs-lookup"><span data-stu-id="e58ce-122">When specifying the number of frames, include enough frames to ensure that all colors in the sequence are sampled.</span></span>

<span data-ttu-id="e58ce-123">您可以使用 WM \_ CAP PAL MANUALCREATE 來取樣目前的畫面格 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="e58ce-123">You can sample the current frame by using WM\_CAP\_PAL\_MANUALCREATE.</span></span> <span data-ttu-id="e58ce-124">藉由使用此訊息搭配數個手動選取的畫面格，您可以建立包含您想要在調色板中顯示之色彩的調色板。</span><span class="sxs-lookup"><span data-stu-id="e58ce-124">By using this message with several manually selected frames, you can create a palette that contains the colors you want to appear in the palette.</span></span>

<span data-ttu-id="e58ce-125">一個調色板最多可包含256的色彩。</span><span class="sxs-lookup"><span data-stu-id="e58ce-125">A palette can contain up to 256 colors.</span></span> <span data-ttu-id="e58ce-126">如果您合併調色板或影片序列要同時與其他影片或影像一起顯示，您應該使用較小的色彩選取範圍，讓每個影像或影片剪輯的色彩可以並存。</span><span class="sxs-lookup"><span data-stu-id="e58ce-126">If you merge palettes or if the video sequence is to be displayed simultaneously with other video or images, you should use a smaller color selection so that colors from each image or video clip can coexist.</span></span>

<span data-ttu-id="e58ce-127">您可以使用 [**wm \_ cap \_ pal 的 \_ Save**](wm-cap-pal-save.md) message (或 [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) 宏) 來儲存新的調色板，並在稍後使用 [**wm \_ cap \_ pal \_ 開啟**](wm-cap-pal-open.md) 的訊息來取得它。</span><span class="sxs-lookup"><span data-stu-id="e58ce-127">You save a new palette by using the [**WM\_CAP\_PAL\_SAVE**](wm-cap-pal-save.md) message (or the [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) macro) and later retrieve it by using the [**WM\_CAP\_PAL\_OPEN**](wm-cap-pal-open.md) message.</span></span> <span data-ttu-id="e58ce-128">您可以儲存調色板以進行後置處理，或在另一個應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="e58ce-128">You can save a palette for post-processing of the palette or for use in another application.</span></span>

<span data-ttu-id="e58ce-129">您可以使用 [**WM \_ CAP \_ PAL \_ 貼**](wm-cap-pal-paste.md) 上訊息，將 [剪貼簿] 從 [剪貼簿] 貼到 [捕獲] 視窗。</span><span class="sxs-lookup"><span data-stu-id="e58ce-129">You can paste a palette from the clipboard into the capture window by using the [**WM\_CAP\_PAL\_PASTE**](wm-cap-pal-paste.md) message.</span></span> <span data-ttu-id="e58ce-130">[捕獲] 視窗會將此選擇區傳送至 capture 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="e58ce-130">The capture window passes the palette to the capture driver.</span></span> <span data-ttu-id="e58ce-131">其他應用程式可以將調色板複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="e58ce-131">Other applications can copy palettes to the clipboard.</span></span> <span data-ttu-id="e58ce-132">您也可以使用 [ [**WM \_ CAP \_ 編輯 \_ 複製**](wm-cap-edit-copy.md) 訊息 (] 或 [ [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) 宏) ，將調色板複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="e58ce-132">You can also copy a palette to the clipboard by using the [**WM\_CAP\_EDIT\_COPY**](wm-cap-edit-copy.md) message (or the [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) macro).</span></span> <span data-ttu-id="e58ce-133">此訊息會將影片框架緩衝區（包括調色板）複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="e58ce-133">This message copies the video frame buffer, including the palette, onto the clipboard.</span></span>

 

 




