---
title: 使用 MCIWnd 調色板
description: 使用 MCIWnd 調色板
ms.assetid: 2b99ca57-f321-4286-8ebf-ae3344d8d2c9
keywords:
- MCIWndGetPalette 宏
- MCIWndSetPalette 宏
- MCIWndRealize 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970e0e33c9dd03c7f1133576f371b713f7174df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933207"
---
# <a name="using-mciwnd-palettes"></a><span data-ttu-id="8cc55-106">使用 MCIWnd 調色板</span><span class="sxs-lookup"><span data-stu-id="8cc55-106">Using MCIWnd Palettes</span></span>

<span data-ttu-id="8cc55-107">使用8位色彩深度播放影片剪輯 (256-色彩容量) 需要有一個調色板來定義所要使用的色彩。</span><span class="sxs-lookup"><span data-stu-id="8cc55-107">Playing video clips with 8-bit color depth (256-color capacity) requires a palette to define the colors being used.</span></span> <span data-ttu-id="8cc55-108">有時候，影片剪輯隨附的調色板不是播放期間最適合使用的調色板。</span><span class="sxs-lookup"><span data-stu-id="8cc55-108">Sometimes, the palette included with a video clip is not the most appropriate palette to use during playback.</span></span> <span data-ttu-id="8cc55-109">在此情況下，MCIWnd 提供三種方式來管理用來播放的調色板：</span><span class="sxs-lookup"><span data-stu-id="8cc55-109">In this case, MCIWnd provides three ways to manage palettes for playback:</span></span>

-   <span data-ttu-id="8cc55-110">使用 [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) 宏，取出與 MCIWnd 視窗相關聯之調色板的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8cc55-110">Retrieve a handle to the palette associated with an MCIWnd window by using the [**MCIWndGetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpalette) macro.</span></span> <span data-ttu-id="8cc55-111">選擇區不一定會與 [MCIWnd] 視窗建立關聯。</span><span class="sxs-lookup"><span data-stu-id="8cc55-111">The palette is not necessarily associated exclusively with the MCIWnd window.</span></span> <span data-ttu-id="8cc55-112">其他應用程式可以存取，甚至使調色板控制碼失效。</span><span class="sxs-lookup"><span data-stu-id="8cc55-112">Other applications can access, and even invalidate, the palette handle.</span></span> <span data-ttu-id="8cc55-113">因此，您的應用程式應該預期會使用調色板的全域使用方式，而且在使用調色板完成時，不應該釋放它。</span><span class="sxs-lookup"><span data-stu-id="8cc55-113">Consequently, your application should anticipate the global use of the palette and, when finished with the palette, should not free it.</span></span>
-   <span data-ttu-id="8cc55-114">使用 [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) 宏，指定與 MCIWnd 視窗相關聯之影片剪輯要使用的新調色板。</span><span class="sxs-lookup"><span data-stu-id="8cc55-114">Specify a new palette to use with the video clip associated with an MCIWnd window by using the [**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette) macro.</span></span>
-   <span data-ttu-id="8cc55-115">使用 [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) 宏，藉此實現與 MCIWnd 視窗相關聯的元件至系統元件。</span><span class="sxs-lookup"><span data-stu-id="8cc55-115">Realize the palette associated with an MCIWnd window to the system palette by using the [**MCIWndRealize**](/windows/desktop/api/Vfw/nf-vfw-mciwndrealize) macro.</span></span> <span data-ttu-id="8cc55-116">此宏會使用與 [MCIWnd] 視窗相關聯的調色板來呼叫 [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) 函數。</span><span class="sxs-lookup"><span data-stu-id="8cc55-116">This macro calls the [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) function with the palette associated with the MCIWnd window.</span></span> <span data-ttu-id="8cc55-117">如果您的應用程式訊息處理常式適用于 [**wm \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) 和 [**Wm \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) 只呼叫 **RealizePalette** 或 **MCIWndRealize**，則必須將這些訊息轉送到 MCIWnd，如果您未自行處理它們。</span><span class="sxs-lookup"><span data-stu-id="8cc55-117">If your application message handlers for [**WM\_PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) and [**WM\_QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) call only **RealizePalette** or **MCIWndRealize**, you must forward these messages to MCIWnd if you do not handle them yourself.</span></span>

> [!Note]  
> <span data-ttu-id="8cc55-118">當有8位色彩深度的影片剪輯載入至 MCIWnd 視窗時，該剪輯隨附的調色板會取代與 [MCIWnd] 視窗相關聯的調色板。</span><span class="sxs-lookup"><span data-stu-id="8cc55-118">When a video clip with 8-bit color depth is loaded into the MCIWnd window, the palette included with that clip replaces the palette associated with the MCIWnd window.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8cc55-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="8cc55-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cc55-120">播放增強功能</span><span class="sxs-lookup"><span data-stu-id="8cc55-120">Playback Enhancements</span></span>](playback-enhancements.md)
</dt> </dl>

 

 