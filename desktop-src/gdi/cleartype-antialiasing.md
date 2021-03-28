---
description: Microsoft ClearType 消除鋸齒是一種平滑方法，可改善傳統消除鋸齒的字型顯示解析度。
ms.assetid: b9896934-1e4f-4ae1-922a-ef30e0edf94f
title: ClearType 消除鋸齒功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbe7ae1a6c99fcee826c576b7671aea6e9ce6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972760"
---
# <a name="cleartype-antialiasing"></a><span data-ttu-id="5f62c-103">ClearType 消除鋸齒功能</span><span class="sxs-lookup"><span data-stu-id="5f62c-103">ClearType Antialiasing</span></span>

<span data-ttu-id="5f62c-104">Microsoft ClearType 消除鋸齒是一種平滑方法，可改善傳統消除鋸齒的字型顯示解析度。</span><span class="sxs-lookup"><span data-stu-id="5f62c-104">Microsoft ClearType antialiasing is a smoothing method that improves font display resolution over traditional antialiasing.</span></span> <span data-ttu-id="5f62c-105">它利用數位介面大幅改善色彩 LCD 監視器的可讀性，例如膝上型電腦上的色彩，以及高品質的平面桌面顯示器。</span><span class="sxs-lookup"><span data-stu-id="5f62c-105">It dramatically improves readability on color LCD monitors with a digital interface, such as those in laptops and high-quality flat desktop displays.</span></span> <span data-ttu-id="5f62c-106">CRT 螢幕的可讀性也稍微改進。</span><span class="sxs-lookup"><span data-stu-id="5f62c-106">Readability on CRT screens is also somewhat improved.</span></span>

<span data-ttu-id="5f62c-107">不過，ClearType 取決於 LCD 條紋的方向和順序。</span><span class="sxs-lookup"><span data-stu-id="5f62c-107">However, ClearType is dependent on the orientation and ordering of the LCD stripes.</span></span> <span data-ttu-id="5f62c-108">目前，ClearType 僅針對具有以 RGB 順序排列之分隔號紋的 Lcd 執行。</span><span class="sxs-lookup"><span data-stu-id="5f62c-108">Currently, ClearType is implemented only for LCDs with vertical stripes that are ordered RGB.</span></span> <span data-ttu-id="5f62c-109">尤其是，這會影響 tablet Pc，也就是可在任何方向導向的顯示器，以及可以從橫向轉換成直向的畫面。</span><span class="sxs-lookup"><span data-stu-id="5f62c-109">In particular, this affects tablet PCs, where the display can be oriented in any direction, and those screens that can be turned from landscape to portrait.</span></span>

<span data-ttu-id="5f62c-110">允許 ClearType 消除鋸齒：</span><span class="sxs-lookup"><span data-stu-id="5f62c-110">ClearType antialiasing is allowed:</span></span>

-   <span data-ttu-id="5f62c-111">針對16、24和32位色彩 (針對256色彩或較少) 停用</span><span class="sxs-lookup"><span data-stu-id="5f62c-111">For 16-, 24-, and 32-bit color (disabled for 256 colors or less)</span></span>
-   <span data-ttu-id="5f62c-112">若為螢幕 DC 和記憶體 DC (不適用於印表機 DC) </span><span class="sxs-lookup"><span data-stu-id="5f62c-112">For screen DC and memory DC (not for printer DC)</span></span>
-   <span data-ttu-id="5f62c-113">Truetype 字型和 OpenType 字型與 TrueType 大綱</span><span class="sxs-lookup"><span data-stu-id="5f62c-113">For TrueType fonts and OpenType fonts with TrueType outlines</span></span>

<span data-ttu-id="5f62c-114">ClearType 消除鋸齒已停用：</span><span class="sxs-lookup"><span data-stu-id="5f62c-114">ClearType antialiasing is disabled:</span></span>

-   <span data-ttu-id="5f62c-115">在 [終端機伺服器用戶端] 底下</span><span class="sxs-lookup"><span data-stu-id="5f62c-115">Under terminal server client</span></span>
-   <span data-ttu-id="5f62c-116">適用于點陣圖字型、向量字型、裝置字型、類型1字型，或不含 TrueType 大綱的 Postscript OpenType 字型</span><span class="sxs-lookup"><span data-stu-id="5f62c-116">For bitmap fonts, vector fonts, device fonts, Type 1 fonts, or Postscript OpenType fonts without TrueType outlines</span></span>
-   <span data-ttu-id="5f62c-117">如果字型已微調內嵌點陣圖，則僅適用于包含內嵌點陣圖的字型大小</span><span class="sxs-lookup"><span data-stu-id="5f62c-117">If the font has tuned embedded bitmaps, only for those font sizes that contain the embedded bitmaps</span></span>

<span data-ttu-id="5f62c-118">若要啟用 ClearType 消除鋸齒，請呼叫 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) 一次以開啟字型平滑處理，然後再按第二次將平滑類型設定為 FE \_ FONTSMOOTHINGCLEARTYPE，如下列程式碼範例所示：</span><span class="sxs-lookup"><span data-stu-id="5f62c-118">To activate ClearType antialiasing, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) once to turn on font smoothing and then a second time to set the smoothing type to FE\_FONTSMOOTHINGCLEARTYPE, as shown in the following code sample:</span></span>


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHING,
                     TRUE,
                     0,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE);
SystemParametersInfo(SPI_SETFONTSMOOTHINGTYPE,
                     0,
                     (PVOID)FE_FONTSMOOTHINGCLEARTYPE,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



<span data-ttu-id="5f62c-119">您可以藉由變更 ClearType 演算法中所使用的對比值來調整文字的外觀。</span><span class="sxs-lookup"><span data-stu-id="5f62c-119">You can adjust the appearance of text by changing the contrast value used in the ClearType algorithm.</span></span> <span data-ttu-id="5f62c-120">預設值是1400，但它可以是從1000到2200的任何值。</span><span class="sxs-lookup"><span data-stu-id="5f62c-120">The default is 1,400, but it can be any value from 1,000 to 2,200.</span></span> <span data-ttu-id="5f62c-121">根據顯示裝置和使用者對色彩的敏感度，較高或較低的對比值可能會改善可讀性。</span><span class="sxs-lookup"><span data-stu-id="5f62c-121">Depending on the display device and the user's sensitivity to colors, a higher or lower contrast value may improve readability.</span></span> <span data-ttu-id="5f62c-122">若要變更對比，請使用 SPI SETFONTSMOOTHINGCONTRAST 呼叫 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) \_ 。</span><span class="sxs-lookup"><span data-stu-id="5f62c-122">To change the contrast, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) with SPI\_SETFONTSMOOTHINGCONTRAST.</span></span> <span data-ttu-id="5f62c-123">下列程式碼會將對比值設定為1600。</span><span class="sxs-lookup"><span data-stu-id="5f62c-123">The following code sets the contrast value to 1,600.</span></span>


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



<span data-ttu-id="5f62c-124">針對應用程式相容性，您應該考慮下列詳細資料：</span><span class="sxs-lookup"><span data-stu-id="5f62c-124">You should consider the following details for application compatibility:</span></span>

-   <span data-ttu-id="5f62c-125">使用 ClearType 的文字轉譯比使用標準消除鋸齒稍微慢一點。</span><span class="sxs-lookup"><span data-stu-id="5f62c-125">Text rendering with ClearType is slightly slower than with standard antialiasing.</span></span>
-   <span data-ttu-id="5f62c-126">應用程式不應使用 XOR 來顯示選取的文字。</span><span class="sxs-lookup"><span data-stu-id="5f62c-126">Applications should not use XOR to display selected text.</span></span> <span data-ttu-id="5f62c-127">應用程式應該設定背景色彩，然後重新顯示選取的文字。</span><span class="sxs-lookup"><span data-stu-id="5f62c-127">Applications should set the background color and redisplay the selected text.</span></span>
-   <span data-ttu-id="5f62c-128">應用程式不應該在透明模式中，于本身的上方繪製相同的文字。</span><span class="sxs-lookup"><span data-stu-id="5f62c-128">Applications should not paint the same text on top of itself in transparent mode.</span></span> <span data-ttu-id="5f62c-129">如果發生這種情況，反鋸齒的邊緣圖元將會以自己的色彩合併，而不是使用背景色彩。</span><span class="sxs-lookup"><span data-stu-id="5f62c-129">If this occurs, the edge pixels that are antialiased will color merge with themselves instead of with the background color.</span></span> <span data-ttu-id="5f62c-130">這會導致變暗且彩色的邊緣。</span><span class="sxs-lookup"><span data-stu-id="5f62c-130">This results in darkened and colorful edges.</span></span>
-   <span data-ttu-id="5f62c-131">應用程式不應該在不透明模式下個別繪製字元來繪製文字，因為字元的邊緣可能會被下列字元裁剪。</span><span class="sxs-lookup"><span data-stu-id="5f62c-131">Applications should not paint text by painting the characters individually when in opaque mode because the edge of a character may be clipped by the following character.</span></span> <span data-ttu-id="5f62c-132">發生這種情況是因為以 ClearType 平滑的字元可能具有負 A 或 C 的寬度，其中的一般字元具有正 A 或 C 寬度。</span><span class="sxs-lookup"><span data-stu-id="5f62c-132">This occurs because a character that is smoothed with ClearType may have a negative A or C width where the regular character has a positive A or C width.</span></span> <span data-ttu-id="5f62c-133">只有字元的 B 寬度保證是相同的。</span><span class="sxs-lookup"><span data-stu-id="5f62c-133">Only the B width of the character is guaranteed to be the same.</span></span> <span data-ttu-id="5f62c-134">同樣地，如果平滑文字是 unsmoothed 文字的旁邊，則應用程式應該要小心。</span><span class="sxs-lookup"><span data-stu-id="5f62c-134">Likewise, applications should be careful if smoothed text is next to unsmoothed text.</span></span>
-   <span data-ttu-id="5f62c-135">如果應用程式轉譯文字，然後操作點陣圖，則應該將 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的 **lfQuality** 成員設定為 NONANTIALIASED 品質，以關閉字型凹凸貼圖 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5f62c-135">If an application renders text and then manipulates the bitmap, font smoothing should be turned off by setting the **lfQuality** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure to NONANTIALIASED\_QUALITY.</span></span> <span data-ttu-id="5f62c-136">例如，遊戲可能會新增點陣圖陰影效果，或者可以調整轉譯成點陣圖的文字以產生 thumbview。</span><span class="sxs-lookup"><span data-stu-id="5f62c-136">For example, a game may add a bitmap shadow effect, or text rendered into a bitmap may be scaled to produce a thumbview.</span></span>
-   <span data-ttu-id="5f62c-137">如果使用者是在直向模式下執行 (也就是，則必須停用監視器等量的水準) ClearType 消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="5f62c-137">If the user is running in portrait mode (that is, monitor striping is horizontal) ClearType antialiasing should be disabled.</span></span>

<span data-ttu-id="5f62c-138">[**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta)中的 *FdwQuality* 參數和 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)的 **lfQuality** 成員接受 CLEARTYPE \_ 品質旗標。</span><span class="sxs-lookup"><span data-stu-id="5f62c-138">The *fdwQuality* parameter in [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta) and the **lfQuality** member of [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) accept the CLEARTYPE\_QUALITY flag.</span></span> <span data-ttu-id="5f62c-139">使用此旗標建立的字型柵格化將會使用 ClearType 轉譯器。</span><span class="sxs-lookup"><span data-stu-id="5f62c-139">Rasterization of fonts created with this flag will use the ClearType rasterizer.</span></span> <span data-ttu-id="5f62c-140">此旗標不會影響舊版的作業系統。</span><span class="sxs-lookup"><span data-stu-id="5f62c-140">This flag has no effect on previous versions of the operating system.</span></span>

 

 
