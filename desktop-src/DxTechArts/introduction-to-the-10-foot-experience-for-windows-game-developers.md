---
title: Windows 遊戲開發人員的10英尺體驗簡介
description: 本文將介紹10英尺的體驗，並探索您應該先考慮這項新互動模式的事項清單，即使您不希望遊戲以這種方式播放也是一樣。
ms.assetid: 126a0aae-6a7a-8cda-5748-c364e54c304e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4814c76aeefdadbe1fd8bf9dc4c21cd84612671
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383113"
---
# <a name="introduction-to-the-10-foot-experience-for-windows-game-developers"></a><span data-ttu-id="71eed-103">Windows 遊戲開發人員的10英尺體驗簡介</span><span class="sxs-lookup"><span data-stu-id="71eed-103">Introduction to the 10-Foot Experience for Windows Game Developers</span></span>

<span data-ttu-id="71eed-104">越來越多人以全新的方式使用個人電腦。</span><span class="sxs-lookup"><span data-stu-id="71eed-104">A growing number of people are using their personal computers in a completely new way.</span></span> <span data-ttu-id="71eed-105">當您想像一般與 Windows 電腦的互動時，您可能會想到坐在一台電腦上的監視器，並使用滑鼠和鍵盤 (或可能是搖桿裝置) ;這就是所謂的2英尺經驗，它仍然是 Windows 遊戲最常見的案例，但是還有另一種趨勢，那就是使用您的電腦做為娛樂裝置，並有電視的輸出。</span><span class="sxs-lookup"><span data-stu-id="71eed-105">When you think of typical interaction with a Windows-based computer, you probably envision sitting at a desk with a monitor, and using a mouse and keyboard (or perhaps a joystick device); this is referred to as the 2-foot experience, and it's still the most common scenario for Windows gaming, but there's another trend which you'll probably start hearing more about: the 10-foot experience, which describes using your computer as an entertainment device with output to a TV.</span></span> <span data-ttu-id="71eed-106">本文將介紹10英尺的體驗，並探索您應該先考慮這項新互動模式的事項清單，即使您不希望遊戲以這種方式播放也是一樣。</span><span class="sxs-lookup"><span data-stu-id="71eed-106">This article introduces the 10-foot experience and explores the list of things that you should consider first about this new interaction pattern, even if you aren't expecting your game to be played this way.</span></span> <span data-ttu-id="71eed-107">客戶的部分會在執行 Windows Media Center 的電腦上執行您的 Windows 遊戲，最好是在客戶試用之前，先瞭解該體驗的外觀。</span><span class="sxs-lookup"><span data-stu-id="71eed-107">Some portion of your customers will run your Windows-based game on a computer running Windows Media Center—it's better that you know what that experience will be like before your customers try it.</span></span>

-   [<span data-ttu-id="71eed-108">什麼是 Windows Media Center？</span><span class="sxs-lookup"><span data-stu-id="71eed-108">What is Windows Media Center?</span></span>](#what-is-windows-media-center)
-   [<span data-ttu-id="71eed-109">10英尺體驗</span><span class="sxs-lookup"><span data-stu-id="71eed-109">The 10-Foot Experience</span></span>](#the-10-foot-experience)
    -   [<span data-ttu-id="71eed-110">安裝</span><span class="sxs-lookup"><span data-stu-id="71eed-110">Installation</span></span>](#installation)
    -   [<span data-ttu-id="71eed-111">使用者輸入</span><span class="sxs-lookup"><span data-stu-id="71eed-111">User Input</span></span>](#user-input)
    -   [<span data-ttu-id="71eed-112">顯示器</span><span class="sxs-lookup"><span data-stu-id="71eed-112">Display</span></span>](#display)
-   [<span data-ttu-id="71eed-113">外觀比例和寬螢幕</span><span class="sxs-lookup"><span data-stu-id="71eed-113">Aspect Ratio and Widescreen</span></span>](#aspect-ratio-and-widescreen)
-   [<span data-ttu-id="71eed-114">標題安全區域</span><span class="sxs-lookup"><span data-stu-id="71eed-114">Title-Safe Region</span></span>](#title-safe-region)
-   [<span data-ttu-id="71eed-115">NTSC 建議</span><span class="sxs-lookup"><span data-stu-id="71eed-115">NTSC Suggestions</span></span>](#ntsc-suggestions)
    -   [<span data-ttu-id="71eed-116">在16和235之間夾具 RGB 色彩元件值</span><span class="sxs-lookup"><span data-stu-id="71eed-116">Clamp the RGB color component values between 16 and 235</span></span>](#clamp-the-rgb-color-component-values-between-16-and-235)
    -   [<span data-ttu-id="71eed-117">避免可能出現相同色彩的相似色彩</span><span class="sxs-lookup"><span data-stu-id="71eed-117">Avoid similar colors that might appear identical</span></span>](#avoid-similar-colors-that-might-appear-identical)
    -   [<span data-ttu-id="71eed-118">避免對比中的清晰差異</span><span class="sxs-lookup"><span data-stu-id="71eed-118">Avoid sharp differences in contrast</span></span>](#avoid-sharp-differences-in-contrast)
-   [<span data-ttu-id="71eed-119">結論</span><span class="sxs-lookup"><span data-stu-id="71eed-119">Conclusion</span></span>](#conclusion)

## <a name="what-is-windows-media-center"></a><span data-ttu-id="71eed-120">什麼是 Windows Media Center？</span><span class="sxs-lookup"><span data-stu-id="71eed-120">What is Windows Media Center?</span></span>

<span data-ttu-id="71eed-121">Windows Media Center 可作為主機電腦的多媒體功能介面。</span><span class="sxs-lookup"><span data-stu-id="71eed-121">Windows Media Center can act as the interface to the multimedia capabilities of the host computer.</span></span> <span data-ttu-id="71eed-122">這項功能的網站（ [Windows Media Center 首頁](https://windows.microsoft.com/windows/products/windows-media-center/)）提供詳盡的簡介，並顯示最新版本中所有可用的絕佳東西。</span><span class="sxs-lookup"><span data-stu-id="71eed-122">The Web site for this feature, [Windows Media Center Home](https://windows.microsoft.com/windows/products/windows-media-center/), offers a thorough introduction and shows off all the good stuff available in the latest version.</span></span> <span data-ttu-id="71eed-123">Media Center 隨附于 Windows XP Media Center Edition、Windows Vista Home Premium、Windows Vista 旗艦版，以及大部分的 Windows 7 版本。</span><span class="sxs-lookup"><span data-stu-id="71eed-123">Media Center is included in Windows XP Media Center Edition, Windows Vista Home Premium, Windows Vista Ultimate, and most editions of Windows 7.</span></span>

<span data-ttu-id="71eed-124">在過去，取得 Windows Media Center 的唯一方法是從第1層系統製造商購買 Media Center 電腦，但因為 Windows Media Center 現在隨附于兩個版本的 Windows Vista 中，所以可能的 marketplace 現在更大。</span><span class="sxs-lookup"><span data-stu-id="71eed-124">In the past, the only way to get Windows Media Center was to buy a Media Center PC from a tier-1 system manufacturer, but because Windows Media Center is now included with two editions of Windows Vista, the potential marketplace is now much larger.</span></span>

## <a name="the-10-foot-experience"></a><span data-ttu-id="71eed-125">10英尺體驗</span><span class="sxs-lookup"><span data-stu-id="71eed-125">The 10-Foot Experience</span></span>

<span data-ttu-id="71eed-126">Windows Media Center 的設計目的是要讓人們可以使用 Windows 來提供豐富的客廳娛樂體驗，並遵循大部分的使用者偏好與 Windows Media Center 進行不同的互動，而不是傳統的電腦應用程式。</span><span class="sxs-lookup"><span data-stu-id="71eed-126">Windows Media Center was designed around the idea that people could use Windows for a rich living room entertainment experience, and it follows that most users prefer to interact differently with Windows Media Center differently than with traditional computer applications.</span></span> <span data-ttu-id="71eed-127">如果客戶使用的電腦位於娛樂的客廳中，則可能會在傳統電腦監視器以外的地方顯示影片：類比電視、高定義數位電視，以及任意數量的 LCD 顯示器都可能是候選項目。</span><span class="sxs-lookup"><span data-stu-id="71eed-127">For one, if the customer uses the computer in the living room for entertainment, it's likely video is displayed on something other than a conventional computer monitor: analog TVs, high-definition digital TVs, and any number of LCD displays are all likely candidates.</span></span> <span data-ttu-id="71eed-128">這些類型的顯示器通常會從大約10英尺的距離中看到，因此標籤的 *10 英尺體驗*。</span><span class="sxs-lookup"><span data-stu-id="71eed-128">These types of displays are usually viewed from a distance of roughly 10 feet, hence the label *10-foot experience*.</span></span>

<span data-ttu-id="71eed-129">10英尺的體驗不局限于 Windows Media Center 的使用者;在最近幾年，使用者將工作站或筆記本電腦連線到其電視和音訊系統會變得很普遍。</span><span class="sxs-lookup"><span data-stu-id="71eed-129">The 10-foot experience isn't confined to users of Windows Media Center; it's become common in recent years for users to connect their workstation or notebook computer to their TV and audio system.</span></span> <span data-ttu-id="71eed-130">取用者顯示器裝置在電腦上公開 RGB 或 DVI 連接（標準影片輸出埠）的情況越來越普遍。</span><span class="sxs-lookup"><span data-stu-id="71eed-130">It's increasingly common for consumer display devices to expose RGB or DVI connections, the standard video output ports on computers.</span></span> <span data-ttu-id="71eed-131">此外，S-video 埠是高階視訊卡的一般功能，並提供簡單的方式來輸出至替代顯示裝置。</span><span class="sxs-lookup"><span data-stu-id="71eed-131">In addition, S-Video ports are a typical feature of high-end video cards, and they offer an easy way to output to an alternate display device.</span></span>

<span data-ttu-id="71eed-132">您應考慮一些重要的設計指導方針，以獲得愉快的10英尺體驗：安裝、使用者輸入和顯示。</span><span class="sxs-lookup"><span data-stu-id="71eed-132">There are some important design guidelines which should be considered for a pleasant 10-foot experience: installation, user input, and display.</span></span>

### <a name="installation"></a><span data-ttu-id="71eed-133">安裝</span><span class="sxs-lookup"><span data-stu-id="71eed-133">Installation</span></span>

<span data-ttu-id="71eed-134">在平均的2英尺體驗期間，使用者會在電腦的距離內;如果在啟動或遊戲期間，使用者必須插入或切換媒體，使用者至少可以維持在最新狀態。</span><span class="sxs-lookup"><span data-stu-id="71eed-134">During the average 2-foot experience, the user is within reaching distance of the computer; if during startup or gameplay, the user is required to insert or switch media, the user can at least remain seated.</span></span> <span data-ttu-id="71eed-135">平均的10英尺體驗會將電腦放在使用者的房間內，因此，任何需要使用者實際與電腦互動的使用者，都可以強制使用者在房間內取得並跨房間。</span><span class="sxs-lookup"><span data-stu-id="71eed-135">The average 10-foot experience places the computer across the room from the user, and therefore anything that requires the user to physically interact with the computer forces the user to get up and cross the room.</span></span> <span data-ttu-id="71eed-136">基於這個理由，開發人員應避免強制使用者變更媒體;請考慮允許將應用程式完整安裝至硬碟。</span><span class="sxs-lookup"><span data-stu-id="71eed-136">For this reason, developers should avoid forcing the user to change media; consider allowing a complete installation of your application to the hard drive.</span></span>

### <a name="user-input"></a><span data-ttu-id="71eed-137">使用者輸入</span><span class="sxs-lookup"><span data-stu-id="71eed-137">User Input</span></span>

<span data-ttu-id="71eed-138">Windows Media Center 的另一項功能是支援標準遠端控制，這是一般慣用的輸入裝置。</span><span class="sxs-lookup"><span data-stu-id="71eed-138">Another feature of Windows Media Center is support for a standard remote control, which is the generally preferred input device.</span></span> <span data-ttu-id="71eed-139">雖然遊戲標題的類型大多會決定遙控器是否適合提供遊戲輸入，但您還是可以讓使用者使用遙控器來暫停遊戲並存取遊戲中的功能表;不過，請確定您也允許使用者使用主要遊戲輸入裝置來控制功能表。</span><span class="sxs-lookup"><span data-stu-id="71eed-139">Although the genre of your game title largely decides whether the remote control is suitable for providing game input, you still might want to allow the user to pause the game and access in-game menus by using the remote control; however, make certain that you also allow the user to control the menus by using the primary game input device.</span></span> <span data-ttu-id="71eed-140">如需設計和開發 Windows Media Center 及其裝置的詳細資訊，請參閱 MSDN 上的 [Windows Media Center 軟體發展工具組](/previous-versions/msdn10/bb895967(v=msdn.10)) （英文）。</span><span class="sxs-lookup"><span data-stu-id="71eed-140">For more information about designing and developing for Windows Media Center and its devices, see [Windows Media Center Software Development Kit](/previous-versions/msdn10/bb895967(v=msdn.10)) on MSDN.</span></span>

<span data-ttu-id="71eed-141">避免使用者與電腦或其周邊電腦之間的任何實體互動。</span><span class="sxs-lookup"><span data-stu-id="71eed-141">Avoid any physical interaction between the user and the computer or its peripherals.</span></span> <span data-ttu-id="71eed-142">需要使用者在遊戲期間變更輸入控制器是不必要的，因為他或她可能接近主要輸入裝置。</span><span class="sxs-lookup"><span data-stu-id="71eed-142">Requiring the user to change input controllers during gameplay is undesirable, since he or she is likely to be near only the primary input device.</span></span>

<span data-ttu-id="71eed-143">Microsoft 已建立常用的遊戲控制器控制器來搭配 Windows 和 Xbox 360-適用于 Windows 的 Xbox 360 控制器和適用于 Windows 的 Xbox 360 無線控制器。</span><span class="sxs-lookup"><span data-stu-id="71eed-143">Microsoft has created common gamepad controllers for use with both Windows and Xbox 360—the Xbox 360 Controller for Windows and the Xbox 360 Wireless Controller for Windows.</span></span> <span data-ttu-id="71eed-144">確定您的標題在通用控制器上正常運作，可減輕一些與測試您的遊戲對可能的輸入裝置相關的麻煩。</span><span class="sxs-lookup"><span data-stu-id="71eed-144">Making sure that your title plays well on the common controllers will ease some of the headache associated with testing your game against potential input devices.</span></span>

### <a name="display"></a><span data-ttu-id="71eed-145">顯示</span><span class="sxs-lookup"><span data-stu-id="71eed-145">Display</span></span>

<span data-ttu-id="71eed-146">各種可能的顯示裝置會提出有關顯示挑戰的建議，而每種類型的裝置都有特殊的警告。</span><span class="sxs-lookup"><span data-stu-id="71eed-146">The wide range of potential display devices makes advice about display challenging, and each type of device has special caveats.</span></span> <span data-ttu-id="71eed-147">本文稍後會介紹某些特定顯示器技術的相關問題。</span><span class="sxs-lookup"><span data-stu-id="71eed-147">Some of the issues surrounding specific display technologies are introduced later in this paper.</span></span> <span data-ttu-id="71eed-148">不論影片輸出裝置為何，都必須將字型和 UI 圖形大小調整為夠大，以利在10英尺的距離上取得可讀性。</span><span class="sxs-lookup"><span data-stu-id="71eed-148">Regardless of the video output device, it's important that fonts and UI graphics are sized large enough for comfortable readability at a distance of 10 feet.</span></span> <span data-ttu-id="71eed-149">另請注意，反鋸齒字型通常會提供更好的可讀性。</span><span class="sxs-lookup"><span data-stu-id="71eed-149">Also note that antialiased fonts generally offer better readability.</span></span>

<span data-ttu-id="71eed-150">您也應該避免使用單一圖元粗細或詳細資料的水平線條和靜態 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="71eed-150">You should also avoid horizontal lines and static UI elements with single-pixel thickness or detail.</span></span> <span data-ttu-id="71eed-151">較舊的電視可能無法顯示詳細資料，甚至是在最新的顯示裝置上執行時，您的內容會在交錯模式上執行時閃爍，因為單一資料列只會顯示一半的時間。</span><span class="sxs-lookup"><span data-stu-id="71eed-151">Older televisions might not display fine detail, and even on the latest display devices, your content will flicker when running on an interlaced mode, since a single row of pixels is visible only half the time.</span></span> <span data-ttu-id="71eed-152">為了取代小型詳細資料，請注意，2圖元的灰色線會顯示為2圖元的白色線條。</span><span class="sxs-lookup"><span data-stu-id="71eed-152">As a replacement for small detail, realize that a 2-pixel gray line appears thinner than a 2-pixel white line.</span></span> <span data-ttu-id="71eed-153"> (這基本上與將1圖元的白色線條模糊的方式相同。 ) </span><span class="sxs-lookup"><span data-stu-id="71eed-153">(This is essentially the same as blurring a 1-pixel white line.)</span></span>

## <a name="aspect-ratio-and-widescreen"></a><span data-ttu-id="71eed-154">外觀比例和寬螢幕</span><span class="sxs-lookup"><span data-stu-id="71eed-154">Aspect Ratio and Widescreen</span></span>

<span data-ttu-id="71eed-155">外觀比例描述顯示器的寬度和高度比例。</span><span class="sxs-lookup"><span data-stu-id="71eed-155">Aspect ratio describes the width and height proportion of the display.</span></span> <span data-ttu-id="71eed-156">標準電視和電腦監視器顯示器的外觀比例為4:3，這表示每4個圖元沿著框架緩衝區的寬度都有3圖元， (有時也會以 1.33) 表示。</span><span class="sxs-lookup"><span data-stu-id="71eed-156">Standard TV and computer monitor displays have an aspect ratio of 4:3, meaning that for every 4 pixels running along the width of the frame buffer, there are 3 pixels along the height (sometimes also represented as 1.33).</span></span>

<span data-ttu-id="71eed-157">隨著 HDTV 的出現，16：9的外觀比例（也稱為寬螢幕）已成為電視未來的標準，以及增強定義電視 (EDTV) ，您可能會遇到三種顯示模式：</span><span class="sxs-lookup"><span data-stu-id="71eed-157">With the advent of HDTV, an aspect ratio of 16:9—also known as wide screen—has become the standard for the future of TV, and along with enhanced-definition TV (EDTV), there are three display modes that you're likely to encounter:</span></span>

<dl> <dt>

<span data-ttu-id="71eed-158"><span id="480p_EDTV"></span><span id="480p_edtv"></span><span id="480P_EDTV"></span>480p EDTV</span><span class="sxs-lookup"><span data-stu-id="71eed-158"><span id="480p_EDTV"></span><span id="480p_edtv"></span><span id="480P_EDTV"></span>480p EDTV</span></span>
</dt> <dd>

<span data-ttu-id="71eed-159">480的掃描行會逐漸呈現。</span><span class="sxs-lookup"><span data-stu-id="71eed-159">480 scan lines presented progressively.</span></span> <span data-ttu-id="71eed-160">這種模式可以輸出 4:3 (，其框架緩衝區解析度為640× 480) 或 16:9 (720 × 480) 。</span><span class="sxs-lookup"><span data-stu-id="71eed-160">This mode can output either 4:3 (with a frame buffer resolution of 640×480) or 16:9 (720×480).</span></span>

</dd> <dt>

<span data-ttu-id="71eed-161"><span id="720p_HDTV"></span><span id="720p_hdtv"></span><span id="720P_HDTV"></span>720p HDTV</span><span class="sxs-lookup"><span data-stu-id="71eed-161"><span id="720p_HDTV"></span><span id="720p_hdtv"></span><span id="720P_HDTV"></span>720p HDTV</span></span>
</dt> <dd>

<span data-ttu-id="71eed-162">720的掃描行會逐漸呈現。</span><span class="sxs-lookup"><span data-stu-id="71eed-162">720 scan lines presented progressively.</span></span> <span data-ttu-id="71eed-163">此模式一律為 16:9 (1280 × 720) 。</span><span class="sxs-lookup"><span data-stu-id="71eed-163">This mode is always 16:9 (1280×720).</span></span>

</dd> <dt>

<span data-ttu-id="71eed-164"><span id="1080i_HDTV"></span><span id="1080i_hdtv"></span><span id="1080I_HDTV"></span>1080i HDTV</span><span class="sxs-lookup"><span data-stu-id="71eed-164"><span id="1080i_HDTV"></span><span id="1080i_hdtv"></span><span id="1080I_HDTV"></span>1080i HDTV</span></span>
</dt> <dd>

<span data-ttu-id="71eed-165">1080掃描行呈現交錯式。</span><span class="sxs-lookup"><span data-stu-id="71eed-165">1080 scan lines presented interlaced.</span></span> <span data-ttu-id="71eed-166">如果個別呈現交錯欄位) ，此模式一律為 16:9 (1920 x 1080 或1920×540。</span><span class="sxs-lookup"><span data-stu-id="71eed-166">This mode is always 16:9 (1920×1080, or 1920×540 if rendering the interlace fields separately).</span></span>

</dd> </dl>

<span data-ttu-id="71eed-167">如果您的遊戲以硬式編碼方式在4:3 的外觀比例中運作，則在16:9 畫面上觀看遊戲的使用者可能有三個顯示影像的選項，這些都不是特別滿足：</span><span class="sxs-lookup"><span data-stu-id="71eed-167">If your game is hard-coded to work in a 4:3 aspect ratio, a user who views your game on a 16:9 screen likely has three options for displaying the image, none of which are particularly satisfying:</span></span>

<dl> <dt>

<span data-ttu-id="71eed-168"><span id="Stretch"></span><span id="stretch"></span><span id="STRETCH"></span>伸展</span><span class="sxs-lookup"><span data-stu-id="71eed-168"><span id="Stretch"></span><span id="stretch"></span><span id="STRETCH"></span>Stretch</span></span>
</dt> <dd>

<span data-ttu-id="71eed-169">4:3 框架緩衝區會伸展，以完美涵蓋顯示的16:9 原生解析度，導致場景物件的出現範圍超出所需。</span><span class="sxs-lookup"><span data-stu-id="71eed-169">The 4:3 frame buffer is stretched to perfectly cover the 16:9 native resolution of the display, resulting in your scene objects appearing wider than desired.</span></span> <span data-ttu-id="71eed-170">有些電視提供額外的延展模式，會嘗試將外觀比例維持在顯示的中央附近，並逐漸增加影像邊的延展。</span><span class="sxs-lookup"><span data-stu-id="71eed-170">Some TVs offer additional stretch modes which attempt to preserve the aspect ratio near the center of the display and gradually increase the stretch at the image sides.</span></span>

</dd> <dt>

<span data-ttu-id="71eed-171"><span id="Center"></span><span id="center"></span><span id="CENTER"></span>中心</span><span class="sxs-lookup"><span data-stu-id="71eed-171"><span id="Center"></span><span id="center"></span><span id="CENTER"></span>Center</span></span>
</dt> <dd>

<span data-ttu-id="71eed-172">4:3 畫面格緩衝區會以 undistorted 顯示在顯示的中央，並以黑色橫條填滿側邊的剩餘圖元。</span><span class="sxs-lookup"><span data-stu-id="71eed-172">The 4:3 frame buffer is displayed undistorted in the center of the display, with solid color bars filling the remaining pixels on the sides.</span></span>

</dd> <dt>

<span data-ttu-id="71eed-173"><span id="Zoom"></span><span id="zoom"></span><span id="ZOOM"></span>縮放</span><span class="sxs-lookup"><span data-stu-id="71eed-173"><span id="Zoom"></span><span id="zoom"></span><span id="ZOOM"></span>Zoom</span></span>
</dt> <dd>

<span data-ttu-id="71eed-174">4:3 框架緩衝區會裁剪至16:9 區域，然後在不失真的情況下填滿原生顯示器解析度;請注意，裁剪矩形上方和下方的圖元會完全捨棄，這是遊戲 UI 元素的常見區域。</span><span class="sxs-lookup"><span data-stu-id="71eed-174">The 4:3 frame buffer is cropped to a 16:9 region, which then fills the native display resolution without distortion; note that the pixels above and below the clip rectangle are completely discarded, which are common regions for a game's UI elements.</span></span>

</dd> </dl>

<span data-ttu-id="71eed-175">更好的方法是將全螢幕顯示的支援新增至您的遊戲。</span><span class="sxs-lookup"><span data-stu-id="71eed-175">A better approach is to add support for wide screen display to your game.</span></span> <span data-ttu-id="71eed-176">最重要的變更是將遊戲攝影機的投射轉換設定為使用16:9 外觀比例，以避免出現延展失真。</span><span class="sxs-lookup"><span data-stu-id="71eed-176">The most important change is to set the game camera's projection transform to use a 16:9 aspect ratio, which avoids the stretching distortion.</span></span> <span data-ttu-id="71eed-177">即使您將背景緩衝區保持在4:3 的解析度，切換投影轉換以使用16:9 可大幅改善轉譯影像的認知精確度;當然，最後的影像會經過篩選，以精密4:3 的背景緩衝區解析度以符合16:9 原生顯示器解析度，但這是較不明顯的成品，比外觀比例不相符所造成的延展扭曲更顯著。</span><span class="sxs-lookup"><span data-stu-id="71eed-177">Even if you leave the back buffer at a 4:3 resolution, switching the projection transform to use 16:9 greatly improves the perceived accuracy of the rendered image; of course the final image is filtered to upscale the 4:3 back buffer resolution to meet the 16:9 native display resolution, but this is a less noticeable artifact than the stretch distortion caused by a mismatch of aspect ratios.</span></span>

<span data-ttu-id="71eed-178">將場景轉譯至16:9 攝影機的成本可能會高於4:3 攝影機 (即使是相同的解析度) ，因為更多場景物件將會顯示在更寬的視圖中。</span><span class="sxs-lookup"><span data-stu-id="71eed-178">The cost of rendering the scene through 16:9 camera may be higher than a 4:3 camera (even at identical resolutions), because more scene objects will be visible in the wider view frustum.</span></span> <span data-ttu-id="71eed-179">您也應該留意放大的可見區域可能會對遊戲有何影響;例如，具有16:9 比例的遊戲攝影機會顯示您的遊戲世界比4:3 攝影機更多。</span><span class="sxs-lookup"><span data-stu-id="71eed-179">You should also be aware of how the enlarged viewable area may influence gameplay; for example, a game camera with a 16:9 ratio would reveal more of your game world than a 4:3 camera.</span></span>

<span data-ttu-id="71eed-180">為了獲得16:9 顯示的最佳結果，您應該將轉譯為16:9 背景緩衝區，但這顯然需要填滿更多的圖元。</span><span class="sxs-lookup"><span data-stu-id="71eed-180">For the best results on a 16:9 display, you should render to a 16:9 back buffer, but this will obviously require filling more pixels.</span></span> <span data-ttu-id="71eed-181">640×480和720×480之間的差異幾乎是38400圖元，增益12.5%。</span><span class="sxs-lookup"><span data-stu-id="71eed-181">The difference between 640×480 and 720×480 is almost 38,400 pixels, a gain of 12.5%.</span></span> <span data-ttu-id="71eed-182">如果您可以負擔填滿這個較大型區域的成本，強烈建議您這樣做。</span><span class="sxs-lookup"><span data-stu-id="71eed-182">If you can afford the cost of filling this larger area, we strongly recommend doing so.</span></span>

## <a name="title-safe-region"></a><span data-ttu-id="71eed-183">Title-Safe 區域</span><span class="sxs-lookup"><span data-stu-id="71eed-183">Title-Safe Region</span></span>

<span data-ttu-id="71eed-184">影像框架緩衝區可能會部分地遮蔽于使用者，因為框線周圍的一些圖元通常會由顯示器的前擋板所涵蓋。</span><span class="sxs-lookup"><span data-stu-id="71eed-184">The image frame buffer might be partly obscured from the user, because some pixels around the border are often covered by the display's front bezel.</span></span> <span data-ttu-id="71eed-185">為了確保在各種顯示器硬體上都能看到重要的 UI 元素，您應該觀察目標顯示模式的標題安全區域需求。</span><span class="sxs-lookup"><span data-stu-id="71eed-185">To ensure that critical UI elements are visible on a wide variety of display hardware, you should observe the title-safe region requirements for your target display mode.</span></span> <span data-ttu-id="71eed-186">針對非 HDTV 模式，標題安全區域是框架緩衝區的內部85%，而針對 HDTV 模式，標題安全區域是內部90%。</span><span class="sxs-lookup"><span data-stu-id="71eed-186">For non-HDTV modes, the title-safe region is the inner 85 percent of the frame buffer, and for HDTV modes, the title-safe area is the inner 90 percent.</span></span> <span data-ttu-id="71eed-187">因此，為了達到最大的相容性，在目前和未來的顯示器硬體上，您應該將所有重要的 UI 元素和標頭顯示指標保留在框架緩衝區的內部85% 內。</span><span class="sxs-lookup"><span data-stu-id="71eed-187">Therefore, for the greatest compatibility across current and future display hardware, you should keep all critical UI elements and heads-up display indicators within the inner 85 percent of the frame buffer.</span></span>

## <a name="ntsc-suggestions"></a><span data-ttu-id="71eed-188">NTSC 建議</span><span class="sxs-lookup"><span data-stu-id="71eed-188">NTSC Suggestions</span></span>

<span data-ttu-id="71eed-189">由於 NTSC 是美國的取用者顯示器硬體最常見的影片標準，因此請務必瞭解您的輸出影像應遵循的一些指導方針。</span><span class="sxs-lookup"><span data-stu-id="71eed-189">Since NTSC is the most common video standard in the United States for consumer display hardware, it's important to know about some of the guidelines that you should follow for your output image.</span></span>

### <a name="clamp-the-rgb-color-component-values-between-16-and-235"></a><span data-ttu-id="71eed-190">在16和235之間夾具 RGB 色彩元件值</span><span class="sxs-lookup"><span data-stu-id="71eed-190">Clamp the RGB color component values between 16 and 235</span></span>

<span data-ttu-id="71eed-191">16-235 範圍以外的色彩肯定會傳送至 NTSC 電視，但很可能會將這些超出範圍的值轉譯為音訊資料。</span><span class="sxs-lookup"><span data-stu-id="71eed-191">Colors outside the range of 16-235 can certainly be sent to an NTSC TV, but it's likely that these out-of-range values will be interpreted as audio data.</span></span> <span data-ttu-id="71eed-192">這通常稱為 *音訊* 內容，如果您的內容是以純白色背景呈現，則最明顯。</span><span class="sxs-lookup"><span data-stu-id="71eed-192">This is often called *audio buzz*, and would be most apparent if your content were presented over a solid white background.</span></span> <span data-ttu-id="71eed-193">您可以輕鬆地在圖元著色器內執行輸出色彩固定。</span><span class="sxs-lookup"><span data-stu-id="71eed-193">You can easily implement output color clamping within a pixel shader.</span></span>

### <a name="avoid-similar-colors-that-might-appear-identical"></a><span data-ttu-id="71eed-194">避免可能出現相同色彩的相似色彩</span><span class="sxs-lookup"><span data-stu-id="71eed-194">Avoid similar colors that might appear identical</span></span>

<span data-ttu-id="71eed-195">NTSC 色彩區不會提供與一般電腦監視器相同的調色板，因此當遊戲需要播放機辨識不同的位置時，請避免使用類似的色彩。</span><span class="sxs-lookup"><span data-stu-id="71eed-195">The NTSC color gamut doesn't offer the same palette as a typical computer monitor, so avoid using similar colors wherever the game requires that the player to recognize the difference.</span></span>

### <a name="avoid-sharp-differences-in-contrast"></a><span data-ttu-id="71eed-196">避免對比中的清晰差異</span><span class="sxs-lookup"><span data-stu-id="71eed-196">Avoid sharp differences in contrast</span></span>

<span data-ttu-id="71eed-197">雖然這項指導方針並不一定可行，但您可以藉由為您的 UI 前景和背景元素選取適當的色彩，來減輕 NTSC 顯示器上的部分色彩不規則煩惱 (也稱為 *色度* 編目) ;彩色背景上的白色文字可能會提供比對比色彩更好的結果。</span><span class="sxs-lookup"><span data-stu-id="71eed-197">Although this guideline is not always practical to follow, you can mitigate some of the color bleeding annoyances on NTSC displays (also known as *chroma crawl*) by selecting proper colors for your UI foreground and background elements; white text on a colored background will probably give better results than contrasting colors.</span></span>

## <a name="conclusion"></a><span data-ttu-id="71eed-198">結論</span><span class="sxs-lookup"><span data-stu-id="71eed-198">Conclusion</span></span>

<span data-ttu-id="71eed-199">本文提供從 Windows 遊戲開發人員的角度來看的10英尺經驗，但這並不是完整的問卷;如果您要開發 Windows 遊戲標題 (，您應該進一步研究這些主題，即使它不適合與 Windows Media Center) 搭配使用也是一樣。</span><span class="sxs-lookup"><span data-stu-id="71eed-199">This article offered a look at the 10-foot experience from the perspective of a Windows game developer, but it is by no means a comprehensive survey; you should research these topics further if you're developing a Windows game title (even if it's not intended for use with Windows Media Center).</span></span> <span data-ttu-id="71eed-200">真正的測試是在各種影片顯示器上試用您的遊戲，以確保您的遊戲在各方面都能提供愉快的體驗。</span><span class="sxs-lookup"><span data-stu-id="71eed-200">The true test is to try your game on a variety of video displays to ensure that your game offers a pleasant experience on each.</span></span> <span data-ttu-id="71eed-201">根據 Windows 遊戲的一般存留期，以及 Windows Media Center 的使用預測成長，我們幾乎保證您今天發行的遊戲是某人的10英尺體驗的一部分，也就是客戶可以從您的 couches 玩您的遊戲，或被迫坐在辦公桌上。</span><span class="sxs-lookup"><span data-stu-id="71eed-201">Based on the typical life-span of a Windows-based game and the predicted growth in use of Windows Media Center, it's almost guaranteed that a game that you release today is part of someone's 10-foot experience—whether customers can play your game from the comfort of couches or they're forced to sit at desks is largely up to you.</span></span>

 

 