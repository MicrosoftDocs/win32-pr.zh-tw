---
description: 系統會自動處理跨多個監視器的裝置內容 (DC) ，即使監視器具有不同的色彩深度。
ms.assetid: 2f03f612-293a-4a42-a13b-1e08e49d9e54
title: 在多個顯示監視器上繪製
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b6a3e3699000399c61e641137a951ed321fd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691848"
---
# <a name="painting-on-multiple-display-monitors"></a><span data-ttu-id="8f03d-103">在多個顯示監視器上繪製</span><span class="sxs-lookup"><span data-stu-id="8f03d-103">Painting on Multiple Display Monitors</span></span>

<span data-ttu-id="8f03d-104">系統會自動處理跨多個監視器的裝置內容 (DC) ，即使監視器具有不同的色彩深度。</span><span class="sxs-lookup"><span data-stu-id="8f03d-104">The system automatically handles painting into a device context (DC) that spans more than one monitor, even when the monitors have different color depths.</span></span> <span data-ttu-id="8f03d-105">這通常會產生良好的結果，但可能不是最佳的。</span><span class="sxs-lookup"><span data-stu-id="8f03d-105">Usually this produces good results, but it may not be optimal.</span></span> <span data-ttu-id="8f03d-106">例如，兩個顯示器上極大不同色彩深度的視窗可能會有不良的色彩呈現。</span><span class="sxs-lookup"><span data-stu-id="8f03d-106">For example, a window on two monitors of vastly different color depths could have poor color rendition.</span></span> <span data-ttu-id="8f03d-107">此外，具有相同色彩深度的監視器可能會有不同的色彩 formatsfor 範例、色彩可使用不同的位數進行編碼，或位於圖元色彩值的不同位置。</span><span class="sxs-lookup"><span data-stu-id="8f03d-107">Also, monitors with the same color depth may have different color formatsfor example, colors could be encoded with different numbers of bits, or be located in different places in a pixel's color value.</span></span>

<span data-ttu-id="8f03d-108">若要針對跨越多個顯示器的 DC 中的每個監視器取得最佳結果，請呼叫 [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) 來列舉與 dc 相交的監視器，並根據該監視器的顯示內容，分別繪製每個監視器的交集區域。</span><span class="sxs-lookup"><span data-stu-id="8f03d-108">To get the best results for each of the monitors in a DC that spans more than one display, call [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) to enumerate the monitors that intersect your DC and paint the intersecting area in each of them separately according to the display attributes for that monitor.</span></span> <span data-ttu-id="8f03d-109">請參閱在 [橫跨多個顯示器的 DC 上繪製](painting-on-a-dc-that-spans-multiple-displays.md)的範例。</span><span class="sxs-lookup"><span data-stu-id="8f03d-109">See the example in [Painting on a DC That Spans Multiple Displays](painting-on-a-dc-that-spans-multiple-displays.md).</span></span>

<span data-ttu-id="8f03d-110">如果您在 **wm \_ 油漆** 程式碼中進行所有繪圖，並在您 **的 \_ wm 繪圖** 程式碼中處理所有不同的影片模式，則您應該能夠在 [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors)的 **MonitorEnumProc** 中放入您的 **WM \_ 繪圖** 程式碼，只需進行一些修改。</span><span class="sxs-lookup"><span data-stu-id="8f03d-110">If you do all of your drawing in your **WM\_PAINT** code and if your **WM\_PAINT** code handles all of the various video modes, then you should be able to place your **WM\_PAINT** code in the **MonitorEnumProc** of [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) with only a few modifications.</span></span>

 

 



