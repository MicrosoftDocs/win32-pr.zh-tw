---
title: 窗框
description: 大部分的程式都應該使用標準的視窗框架。 沉浸式應用程式可以有隱藏視窗框架的全螢幕模式。 請考慮策略性地使用半透明，以提供更簡單、更淺、更緊密的外觀。
ms.assetid: 6613e07a-2466-4283-88a9-02f2a3fea079
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 40aa58ab48c032519f55afa7c269be6452956912
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104566080"
---
# <a name="window-frames"></a>窗框

> [!NOTE]
> 此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。 大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。

大部分的程式都應該使用標準的視窗框架。 沉浸式應用程式可以有隱藏視窗框架的全螢幕模式。 請考慮策略性地使用半透明，以提供更簡單、更淺、更緊密的外觀。

在視窗框架中，使用者可以操作視窗並查看標題和圖示，以識別其內容。

![[記事本] 視窗周圍視窗框架的螢幕擷取畫面 ](images/win-window-frames-image1.png)

典型的視窗框架。

**注意：** 與 [視窗管理](win-window-mgt.md) 和 [商標](exper-branding.md) 相關的指導方針會顯示在不同的文章中。

## <a name="design-concepts"></a>設計概念

### <a name="glass-window-frames"></a>半透明視窗框架

半透明視窗框架是 Microsoft Windows 美觀嶄新的一環，也就是吸引人和輕量。 這些半透明框架提供 windows 開放式且較不侵入的外觀，協助使用者專注于內容和功能，而不是周圍的介面。

![圍繞計算機之半透明畫面格的螢幕擷取畫面 ](images/win-window-frames-image2.png)

半透明視窗框架。

您可以策略性地在觸控視窗框架的視窗內的小型區域中使用半透明。 這類區域似乎是視窗框架的一部分，雖然技術上而言，它們是視窗工作區的一部分。

![具有半透明邊緣之視窗的螢幕擷取畫面 ](images/win-window-frames-image3.png)

在此範例中，會在工作區中使用半透明，使其看起來像框架的一部分。

### <a name="hidden-frames"></a>隱藏的框架

有時候，最佳的視窗框架根本不是畫面格。 這種情況通常是因為沒有與其他程式（例如 media player、遊戲和 kiosk 應用程式）一起使用的沉浸式[全螢幕](glossary.md)應用程式[主視窗](glossary.md)。

內容檢視器通常可讓您選擇顯示全螢幕內容的選項。 範例包括 Windows Internet Explorer、Windows Live 影像中心、Windows Movie Maker HD、Microsoft PowerPoint 和 Microsoft Word。

![全螢幕視圖中媒體播放程式的螢幕擷取畫面 ](images/win-window-frames-image4.png)

在此範例中，Windows Media Player 可以全螢幕顯示其內容。

### <a name="custom-frames"></a>自訂框架

大部分的 Windows 應用程式都應該使用標準的視窗框架。 不過，對於沉浸式全螢幕的獨立應用程式（如遊戲和 kiosk 應用程式），可能適合將自訂框架用於任何未顯示全螢幕的視窗。 使用自訂框架的動機應該是為整體體驗提供獨特的感覺，而不只是針對 [商標](exper-branding.md)。

![影像謎題和框架的插圖 ](images/win-window-frames-image5.png)

自訂框架適用于沉浸式全螢幕、獨立的應用程式（例如遊戲）。

## <a name="guidelines"></a>指導方針

### <a name="window-frames"></a>窗框

-   使用標準視窗框架。
    -   **例外狀況：** 為了提供沉浸式全螢幕的獨立應用程式，獨特的風格如下：
        -   請考慮隱藏 [主視窗](glossary.md)的視窗框架。
        -   考慮針對 [次要視窗](glossary.md)使用自訂框架。
        -   如果有適當的自訂框架，請選擇輕量的設計，而不會對本身太有太多的關注。

            **不正確：**

            ![分散畫面格的螢幕擷取畫面 ](images/win-window-frames-image6.png)

            在此範例中，自訂框架會將太多注意力吸引到本身。
-   請勿將控制項加入至視窗框架。 請改將控制項放在視窗中。

    **不正確：**

    ![視窗框架中控制項的螢幕擷取畫面 ](images/win-window-frames-image7.png)

    **正確：**

    ![在工作區中控制項的螢幕擷取畫面 ](images/win-window-frames-image8.png)

    在正確的範例中，控制項位於工作區，而不是視窗框架內。

### <a name="full-screen-mode"></a>全螢幕模式

-   針對具有選擇性全螢幕模式的程式，啟用全螢幕模式：
    -   在功能表列或工具列中具有模式全螢幕命令。 當使用者按一下命令時，會在其選取的狀態中顯示命令。

        ![具有全螢幕功能表項目之視窗的螢幕擷取畫面 ](images/win-window-frames-image9.png)

        此範例會顯示全螢幕命令及其標準快速鍵。

-   使用 F11 鍵來取得全螢幕快速鍵。
-   如果有工具列和全螢幕模式經常使用，也有一個具有全螢幕工具提示的圖形工具列按鈕。

    ![全螢幕和 [還原] 按鈕的螢幕擷取畫面 ](images/win-window-frames-image10.png)

    全螢幕工具列按鈕的範例。

-   若要從全螢幕模式還原：
    -   在功能表列或工具列中具有模式全螢幕命令。 當使用者按一下命令時，會以其已清除的狀態顯示命令。
    -   使用 F11 鍵來取得全螢幕快速鍵。 如果尚未指派，也可以使用 Esc 來進行此用途。

### <a name="glass"></a>玻璃

標準視窗框架會在視窗中自動使用玻璃，但您也可以在接觸視窗框架的區域中使用玻璃。

-   **在不使用文字的情況下，于小型區域中策略性地使用半透明的範圍。** 這樣做可以讓某個程式更簡單、更淺、更緊密的外觀，讓區域看起來像是框架的一部分。
-   ![具有半透明邊緣之視窗的螢幕擷取畫面 ](images/win-window-frames-image3.png)
-   在此範例中，玻璃著重于使用者對內容的關注，而不是控制項。
-   **請勿在一般視窗背景更吸引人或更容易使用的情況下使用半透明。**

**正確：**

![具有四個圖形和標籤之視窗的螢幕擷取畫面 ](images/win-window-frames-image11.png)

在此範例中，會使用半透明來為 Alt + Tab 視窗提供輕量外觀。 玻璃適用于此視窗，因為它包含圖形和單一的強式文字標籤。

**不正確：**

![具有十二個圖形之視窗的螢幕擷取畫面 ](images/win-window-frames-image12.png)

在此不正確的範例中，使用半透明會造成干擾。 一般視窗背景是較佳的選擇。

 

 