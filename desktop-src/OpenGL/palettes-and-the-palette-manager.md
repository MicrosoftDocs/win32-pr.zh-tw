---
title: 調色板和調色板管理員
description: Windows 元件管理員是 GDI 的一部分，特別是以8位的顯示介面卡（硬體選擇區為256色彩專案）為目標。
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- Windows 上的 OpenGL，調色板管理員
- Windows 上的 OpenGL，硬體調色板
- 調色板管理員 OpenGL
- 硬體調色板 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dac7d122ec36201e0156a141efc3291a87c7150
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965369"
---
# <a name="palettes-and-the-palette-manager"></a>調色板和調色板管理員

Windows 元件管理員是 GDI 的一部分，特別是以8位的顯示介面卡（ *硬體* 選擇區為256色彩專案）為目標。 螢幕上的圖元會以8位索引的形式儲存在硬體選擇區中。 硬體選擇區中的每個專案通常會定義24位色彩 (8，每個紅色、綠色和藍色) 。

[調色板管理員] 會維護一個 *系統元件* ，這是硬體元件的複本。 系統選擇區分為兩個部分：20個保留色彩和剩餘的236色彩，您可以使用 [調色板管理員] 設定這些色彩。

預設會選取20色 *邏輯調色板* ，並實現到裝置內容中。 您可以建立並使用新的邏輯調色板。 若要變更系統調色板，請選取並瞭解您所建立的邏輯調色板。

您可能會建立邏輯調色板，以指定您想要在 OpenGL 應用程式中顯示的色彩。 使用特定的 GDI 呼叫，您可以暫時以邏輯調色板取代大部分的系統元件。 您可以使用邏輯調色板，使用 RGBA 或色彩索引模式來定義 GDI 的圖元色彩。 邏輯元件的大小上限為8位裝置的256色彩，而真色彩裝置上的4096色彩 (16、24和32位) 。

如需 RGBA 和色彩索引模式的詳細資訊，請參閱 [Rgba 模式和 Windows 調色板管理](rgba-mode-and-windows-palette-management.md) 、 [OpenGL 色彩模式和 windows 元件管理](opengl-color-modes-and-windows-palette-management.md)。

 

 




