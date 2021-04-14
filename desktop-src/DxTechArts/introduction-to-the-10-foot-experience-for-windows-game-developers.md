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
# <a name="introduction-to-the-10-foot-experience-for-windows-game-developers"></a>Windows 遊戲開發人員的10英尺體驗簡介

越來越多人以全新的方式使用個人電腦。 當您想像一般與 Windows 電腦的互動時，您可能會想到坐在一台電腦上的監視器，並使用滑鼠和鍵盤 (或可能是搖桿裝置) ;這就是所謂的2英尺經驗，它仍然是 Windows 遊戲最常見的案例，但是還有另一種趨勢，那就是使用您的電腦做為娛樂裝置，並有電視的輸出。 本文將介紹10英尺的體驗，並探索您應該先考慮這項新互動模式的事項清單，即使您不希望遊戲以這種方式播放也是一樣。 客戶的部分會在執行 Windows Media Center 的電腦上執行您的 Windows 遊戲，最好是在客戶試用之前，先瞭解該體驗的外觀。

-   [什麼是 Windows Media Center？](#what-is-windows-media-center)
-   [10英尺體驗](#the-10-foot-experience)
    -   [安裝](#installation)
    -   [使用者輸入](#user-input)
    -   [顯示器](#display)
-   [外觀比例和寬螢幕](#aspect-ratio-and-widescreen)
-   [標題安全區域](#title-safe-region)
-   [NTSC 建議](#ntsc-suggestions)
    -   [在16和235之間夾具 RGB 色彩元件值](#clamp-the-rgb-color-component-values-between-16-and-235)
    -   [避免可能出現相同色彩的相似色彩](#avoid-similar-colors-that-might-appear-identical)
    -   [避免對比中的清晰差異](#avoid-sharp-differences-in-contrast)
-   [結論](#conclusion)

## <a name="what-is-windows-media-center"></a>什麼是 Windows Media Center？

Windows Media Center 可作為主機電腦的多媒體功能介面。 這項功能的網站（ [Windows Media Center 首頁](https://windows.microsoft.com/windows/products/windows-media-center/)）提供詳盡的簡介，並顯示最新版本中所有可用的絕佳東西。 Media Center 隨附于 Windows XP Media Center Edition、Windows Vista Home Premium、Windows Vista 旗艦版，以及大部分的 Windows 7 版本。

在過去，取得 Windows Media Center 的唯一方法是從第1層系統製造商購買 Media Center 電腦，但因為 Windows Media Center 現在隨附于兩個版本的 Windows Vista 中，所以可能的 marketplace 現在更大。

## <a name="the-10-foot-experience"></a>10英尺體驗

Windows Media Center 的設計目的是要讓人們可以使用 Windows 來提供豐富的客廳娛樂體驗，並遵循大部分的使用者偏好與 Windows Media Center 進行不同的互動，而不是傳統的電腦應用程式。 如果客戶使用的電腦位於娛樂的客廳中，則可能會在傳統電腦監視器以外的地方顯示影片：類比電視、高定義數位電視，以及任意數量的 LCD 顯示器都可能是候選項目。 這些類型的顯示器通常會從大約10英尺的距離中看到，因此標籤的 *10 英尺體驗*。

10英尺的體驗不局限于 Windows Media Center 的使用者;在最近幾年，使用者將工作站或筆記本電腦連線到其電視和音訊系統會變得很普遍。 取用者顯示器裝置在電腦上公開 RGB 或 DVI 連接（標準影片輸出埠）的情況越來越普遍。 此外，S-video 埠是高階視訊卡的一般功能，並提供簡單的方式來輸出至替代顯示裝置。

您應考慮一些重要的設計指導方針，以獲得愉快的10英尺體驗：安裝、使用者輸入和顯示。

### <a name="installation"></a>安裝

在平均的2英尺體驗期間，使用者會在電腦的距離內;如果在啟動或遊戲期間，使用者必須插入或切換媒體，使用者至少可以維持在最新狀態。 平均的10英尺體驗會將電腦放在使用者的房間內，因此，任何需要使用者實際與電腦互動的使用者，都可以強制使用者在房間內取得並跨房間。 基於這個理由，開發人員應避免強制使用者變更媒體;請考慮允許將應用程式完整安裝至硬碟。

### <a name="user-input"></a>使用者輸入

Windows Media Center 的另一項功能是支援標準遠端控制，這是一般慣用的輸入裝置。 雖然遊戲標題的類型大多會決定遙控器是否適合提供遊戲輸入，但您還是可以讓使用者使用遙控器來暫停遊戲並存取遊戲中的功能表;不過，請確定您也允許使用者使用主要遊戲輸入裝置來控制功能表。 如需設計和開發 Windows Media Center 及其裝置的詳細資訊，請參閱 MSDN 上的 [Windows Media Center 軟體發展工具組](/previous-versions/msdn10/bb895967(v=msdn.10)) （英文）。

避免使用者與電腦或其周邊電腦之間的任何實體互動。 需要使用者在遊戲期間變更輸入控制器是不必要的，因為他或她可能接近主要輸入裝置。

Microsoft 已建立常用的遊戲控制器控制器來搭配 Windows 和 Xbox 360-適用于 Windows 的 Xbox 360 控制器和適用于 Windows 的 Xbox 360 無線控制器。 確定您的標題在通用控制器上正常運作，可減輕一些與測試您的遊戲對可能的輸入裝置相關的麻煩。

### <a name="display"></a>顯示

各種可能的顯示裝置會提出有關顯示挑戰的建議，而每種類型的裝置都有特殊的警告。 本文稍後會介紹某些特定顯示器技術的相關問題。 不論影片輸出裝置為何，都必須將字型和 UI 圖形大小調整為夠大，以利在10英尺的距離上取得可讀性。 另請注意，反鋸齒字型通常會提供更好的可讀性。

您也應該避免使用單一圖元粗細或詳細資料的水平線條和靜態 UI 元素。 較舊的電視可能無法顯示詳細資料，甚至是在最新的顯示裝置上執行時，您的內容會在交錯模式上執行時閃爍，因為單一資料列只會顯示一半的時間。 為了取代小型詳細資料，請注意，2圖元的灰色線會顯示為2圖元的白色線條。  (這基本上與將1圖元的白色線條模糊的方式相同。 ) 

## <a name="aspect-ratio-and-widescreen"></a>外觀比例和寬螢幕

外觀比例描述顯示器的寬度和高度比例。 標準電視和電腦監視器顯示器的外觀比例為4:3，這表示每4個圖元沿著框架緩衝區的寬度都有3圖元， (有時也會以 1.33) 表示。

隨著 HDTV 的出現，16：9的外觀比例（也稱為寬螢幕）已成為電視未來的標準，以及增強定義電視 (EDTV) ，您可能會遇到三種顯示模式：

<dl> <dt>

<span id="480p_EDTV"></span><span id="480p_edtv"></span><span id="480P_EDTV"></span>480p EDTV
</dt> <dd>

480的掃描行會逐漸呈現。 這種模式可以輸出 4:3 (，其框架緩衝區解析度為640× 480) 或 16:9 (720 × 480) 。

</dd> <dt>

<span id="720p_HDTV"></span><span id="720p_hdtv"></span><span id="720P_HDTV"></span>720p HDTV
</dt> <dd>

720的掃描行會逐漸呈現。 此模式一律為 16:9 (1280 × 720) 。

</dd> <dt>

<span id="1080i_HDTV"></span><span id="1080i_hdtv"></span><span id="1080I_HDTV"></span>1080i HDTV
</dt> <dd>

1080掃描行呈現交錯式。 如果個別呈現交錯欄位) ，此模式一律為 16:9 (1920 x 1080 或1920×540。

</dd> </dl>

如果您的遊戲以硬式編碼方式在4:3 的外觀比例中運作，則在16:9 畫面上觀看遊戲的使用者可能有三個顯示影像的選項，這些都不是特別滿足：

<dl> <dt>

<span id="Stretch"></span><span id="stretch"></span><span id="STRETCH"></span>伸展
</dt> <dd>

4:3 框架緩衝區會伸展，以完美涵蓋顯示的16:9 原生解析度，導致場景物件的出現範圍超出所需。 有些電視提供額外的延展模式，會嘗試將外觀比例維持在顯示的中央附近，並逐漸增加影像邊的延展。

</dd> <dt>

<span id="Center"></span><span id="center"></span><span id="CENTER"></span>中心
</dt> <dd>

4:3 畫面格緩衝區會以 undistorted 顯示在顯示的中央，並以黑色橫條填滿側邊的剩餘圖元。

</dd> <dt>

<span id="Zoom"></span><span id="zoom"></span><span id="ZOOM"></span>縮放
</dt> <dd>

4:3 框架緩衝區會裁剪至16:9 區域，然後在不失真的情況下填滿原生顯示器解析度;請注意，裁剪矩形上方和下方的圖元會完全捨棄，這是遊戲 UI 元素的常見區域。

</dd> </dl>

更好的方法是將全螢幕顯示的支援新增至您的遊戲。 最重要的變更是將遊戲攝影機的投射轉換設定為使用16:9 外觀比例，以避免出現延展失真。 即使您將背景緩衝區保持在4:3 的解析度，切換投影轉換以使用16:9 可大幅改善轉譯影像的認知精確度;當然，最後的影像會經過篩選，以精密4:3 的背景緩衝區解析度以符合16:9 原生顯示器解析度，但這是較不明顯的成品，比外觀比例不相符所造成的延展扭曲更顯著。

將場景轉譯至16:9 攝影機的成本可能會高於4:3 攝影機 (即使是相同的解析度) ，因為更多場景物件將會顯示在更寬的視圖中。 您也應該留意放大的可見區域可能會對遊戲有何影響;例如，具有16:9 比例的遊戲攝影機會顯示您的遊戲世界比4:3 攝影機更多。

為了獲得16:9 顯示的最佳結果，您應該將轉譯為16:9 背景緩衝區，但這顯然需要填滿更多的圖元。 640×480和720×480之間的差異幾乎是38400圖元，增益12.5%。 如果您可以負擔填滿這個較大型區域的成本，強烈建議您這樣做。

## <a name="title-safe-region"></a>Title-Safe 區域

影像框架緩衝區可能會部分地遮蔽于使用者，因為框線周圍的一些圖元通常會由顯示器的前擋板所涵蓋。 為了確保在各種顯示器硬體上都能看到重要的 UI 元素，您應該觀察目標顯示模式的標題安全區域需求。 針對非 HDTV 模式，標題安全區域是框架緩衝區的內部85%，而針對 HDTV 模式，標題安全區域是內部90%。 因此，為了達到最大的相容性，在目前和未來的顯示器硬體上，您應該將所有重要的 UI 元素和標頭顯示指標保留在框架緩衝區的內部85% 內。

## <a name="ntsc-suggestions"></a>NTSC 建議

由於 NTSC 是美國的取用者顯示器硬體最常見的影片標準，因此請務必瞭解您的輸出影像應遵循的一些指導方針。

### <a name="clamp-the-rgb-color-component-values-between-16-and-235"></a>在16和235之間夾具 RGB 色彩元件值

16-235 範圍以外的色彩肯定會傳送至 NTSC 電視，但很可能會將這些超出範圍的值轉譯為音訊資料。 這通常稱為 *音訊* 內容，如果您的內容是以純白色背景呈現，則最明顯。 您可以輕鬆地在圖元著色器內執行輸出色彩固定。

### <a name="avoid-similar-colors-that-might-appear-identical"></a>避免可能出現相同色彩的相似色彩

NTSC 色彩區不會提供與一般電腦監視器相同的調色板，因此當遊戲需要播放機辨識不同的位置時，請避免使用類似的色彩。

### <a name="avoid-sharp-differences-in-contrast"></a>避免對比中的清晰差異

雖然這項指導方針並不一定可行，但您可以藉由為您的 UI 前景和背景元素選取適當的色彩，來減輕 NTSC 顯示器上的部分色彩不規則煩惱 (也稱為 *色度* 編目) ;彩色背景上的白色文字可能會提供比對比色彩更好的結果。

## <a name="conclusion"></a>結論

本文提供從 Windows 遊戲開發人員的角度來看的10英尺經驗，但這並不是完整的問卷;如果您要開發 Windows 遊戲標題 (，您應該進一步研究這些主題，即使它不適合與 Windows Media Center) 搭配使用也是一樣。 真正的測試是在各種影片顯示器上試用您的遊戲，以確保您的遊戲在各方面都能提供愉快的體驗。 根據 Windows 遊戲的一般存留期，以及 Windows Media Center 的使用預測成長，我們幾乎保證您今天發行的遊戲是某人的10英尺體驗的一部分，也就是客戶可以從您的 couches 玩您的遊戲，或被迫坐在辦公桌上。

 

 