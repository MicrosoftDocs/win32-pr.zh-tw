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
# <a name="cleartype-antialiasing"></a>ClearType 消除鋸齒功能

Microsoft ClearType 消除鋸齒是一種平滑方法，可改善傳統消除鋸齒的字型顯示解析度。 它利用數位介面大幅改善色彩 LCD 監視器的可讀性，例如膝上型電腦上的色彩，以及高品質的平面桌面顯示器。 CRT 螢幕的可讀性也稍微改進。

不過，ClearType 取決於 LCD 條紋的方向和順序。 目前，ClearType 僅針對具有以 RGB 順序排列之分隔號紋的 Lcd 執行。 尤其是，這會影響 tablet Pc，也就是可在任何方向導向的顯示器，以及可以從橫向轉換成直向的畫面。

允許 ClearType 消除鋸齒：

-   針對16、24和32位色彩 (針對256色彩或較少) 停用
-   若為螢幕 DC 和記憶體 DC (不適用於印表機 DC) 
-   Truetype 字型和 OpenType 字型與 TrueType 大綱

ClearType 消除鋸齒已停用：

-   在 [終端機伺服器用戶端] 底下
-   適用于點陣圖字型、向量字型、裝置字型、類型1字型，或不含 TrueType 大綱的 Postscript OpenType 字型
-   如果字型已微調內嵌點陣圖，則僅適用于包含內嵌點陣圖的字型大小

若要啟用 ClearType 消除鋸齒，請呼叫 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) 一次以開啟字型平滑處理，然後再按第二次將平滑類型設定為 FE \_ FONTSMOOTHINGCLEARTYPE，如下列程式碼範例所示：


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



您可以藉由變更 ClearType 演算法中所使用的對比值來調整文字的外觀。 預設值是1400，但它可以是從1000到2200的任何值。 根據顯示裝置和使用者對色彩的敏感度，較高或較低的對比值可能會改善可讀性。 若要變更對比，請使用 SPI SETFONTSMOOTHINGCONTRAST 呼叫 [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) \_ 。 下列程式碼會將對比值設定為1600。


```C++
SystemParametersInfo(SPI_SETFONTSMOOTHINGCONTRAST,
                     0,
                     (PVOID)1600,
                     SPIF_UPDATEINIFILE | SPIF_SENDCHANGE); 
```



針對應用程式相容性，您應該考慮下列詳細資料：

-   使用 ClearType 的文字轉譯比使用標準消除鋸齒稍微慢一點。
-   應用程式不應使用 XOR 來顯示選取的文字。 應用程式應該設定背景色彩，然後重新顯示選取的文字。
-   應用程式不應該在透明模式中，于本身的上方繪製相同的文字。 如果發生這種情況，反鋸齒的邊緣圖元將會以自己的色彩合併，而不是使用背景色彩。 這會導致變暗且彩色的邊緣。
-   應用程式不應該在不透明模式下個別繪製字元來繪製文字，因為字元的邊緣可能會被下列字元裁剪。 發生這種情況是因為以 ClearType 平滑的字元可能具有負 A 或 C 的寬度，其中的一般字元具有正 A 或 C 寬度。 只有字元的 B 寬度保證是相同的。 同樣地，如果平滑文字是 unsmoothed 文字的旁邊，則應用程式應該要小心。
-   如果應用程式轉譯文字，然後操作點陣圖，則應該將 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的 **lfQuality** 成員設定為 NONANTIALIASED 品質，以關閉字型凹凸貼圖 \_ 。 例如，遊戲可能會新增點陣圖陰影效果，或者可以調整轉譯成點陣圖的文字以產生 thumbview。
-   如果使用者是在直向模式下執行 (也就是，則必須停用監視器等量的水準) ClearType 消除鋸齒。

[**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta)中的 *FdwQuality* 參數和 [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)的 **lfQuality** 成員接受 CLEARTYPE \_ 品質旗標。 使用此旗標建立的字型柵格化將會使用 ClearType 轉譯器。 此旗標不會影響舊版的作業系統。

 

 
