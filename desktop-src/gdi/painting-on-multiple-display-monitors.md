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
# <a name="painting-on-multiple-display-monitors"></a>在多個顯示監視器上繪製

系統會自動處理跨多個監視器的裝置內容 (DC) ，即使監視器具有不同的色彩深度。 這通常會產生良好的結果，但可能不是最佳的。 例如，兩個顯示器上極大不同色彩深度的視窗可能會有不良的色彩呈現。 此外，具有相同色彩深度的監視器可能會有不同的色彩 formatsfor 範例、色彩可使用不同的位數進行編碼，或位於圖元色彩值的不同位置。

若要針對跨越多個顯示器的 DC 中的每個監視器取得最佳結果，請呼叫 [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) 來列舉與 dc 相交的監視器，並根據該監視器的顯示內容，分別繪製每個監視器的交集區域。 請參閱在 [橫跨多個顯示器的 DC 上繪製](painting-on-a-dc-that-spans-multiple-displays.md)的範例。

如果您在 **wm \_ 油漆** 程式碼中進行所有繪圖，並在您 **的 \_ wm 繪圖** 程式碼中處理所有不同的影片模式，則您應該能夠在 [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors)的 **MonitorEnumProc** 中放入您的 **WM \_ 繪圖** 程式碼，只需進行一些修改。

 

 



