---
title: 調色板和調色板管理員
description: Windows 的 [調色板管理員] 是 GDI 的一部分，特別是以8位的顯示配接器為目標，並以256色彩專案的硬體選擇區為目標。
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- Windows 上的 OpenGL、調色板管理員
- Windows 上的 OpenGL，硬體調色板
- 調色板管理員 OpenGL
- 硬體調色板 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58407a5ddafe862caa73edd498c4da529b0ac987880828177d0d0b284601efed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936274"
---
# <a name="palettes-and-the-palette-manager"></a>調色板和調色板管理員

Windows 的 [調色板管理員] 是 GDI 的一部分，特別是以8位的顯示配接器為目標，並以256色彩專案的 *硬體* 選擇區為目標。 螢幕上的圖元會以8位索引的形式儲存在硬體選擇區中。 硬體選擇區中的每個專案通常會定義24位色彩 (8，每個紅色、綠色和藍色) 。

[調色板管理員] 會維護一個 *系統元件* ，這是硬體元件的複本。 系統選擇區分為兩個部分：20個保留色彩和剩餘的236色彩，您可以使用 [調色板管理員] 設定這些色彩。

預設會選取20色 *邏輯調色板* ，並實現到裝置內容中。 您可以建立並使用新的邏輯調色板。 若要變更系統調色板，請選取並瞭解您所建立的邏輯調色板。

您可能會建立邏輯調色板，以指定您想要在 OpenGL 應用程式中顯示的色彩。 使用特定的 GDI 呼叫，您可以暫時以邏輯調色板取代大部分的系統元件。 您可以使用邏輯調色板，使用 RGBA 或色彩索引模式來定義 GDI 的圖元色彩。 邏輯元件的大小上限為8位裝置的256色彩，而真色彩裝置上的4096色彩 (16、24和32位) 。

如需 rgba 和色彩索引模式的詳細資訊，請參閱[rgba 模式和 Windows 調色板管理](rgba-mode-and-windows-palette-management.md)和[OpenGL 色彩模式，以及 Windows 的管理元件管理](opengl-color-modes-and-windows-palette-management.md)。

 

 




