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
# <a name="palettes-and-the-palette-manager"></a><span data-ttu-id="fb0fb-107">調色板和調色板管理員</span><span class="sxs-lookup"><span data-stu-id="fb0fb-107">Palettes and the Palette Manager</span></span>

<span data-ttu-id="fb0fb-108">Windows 元件管理員是 GDI 的一部分，特別是以8位的顯示介面卡（ *硬體* 選擇區為256色彩專案）為目標。</span><span class="sxs-lookup"><span data-stu-id="fb0fb-108">The Windows Palette Manager, which is part of the GDI, specifically targets 8-bit display adapters with a *hardware palette* of 256 color entries.</span></span> <span data-ttu-id="fb0fb-109">螢幕上的圖元會以8位索引的形式儲存在硬體選擇區中。</span><span class="sxs-lookup"><span data-stu-id="fb0fb-109">Pixels on the screen are stored as an 8-bit index into the hardware palette.</span></span> <span data-ttu-id="fb0fb-110">硬體選擇區中的每個專案通常會定義24位色彩 (8，每個紅色、綠色和藍色) 。</span><span class="sxs-lookup"><span data-stu-id="fb0fb-110">Each entry in the hardware palette usually defines a 24-bit color (8 each of red, green, and blue).</span></span>

<span data-ttu-id="fb0fb-111">[調色板管理員] 會維護一個 *系統元件* ，這是硬體元件的複本。</span><span class="sxs-lookup"><span data-stu-id="fb0fb-111">The Palette Manager maintains a *system palette* that is a copy of the hardware palette.</span></span> <span data-ttu-id="fb0fb-112">系統選擇區分為兩個部分：20個保留色彩和剩餘的236色彩，您可以使用 [調色板管理員] 設定這些色彩。</span><span class="sxs-lookup"><span data-stu-id="fb0fb-112">The system palette is divided into two sections: 20 reserved colors and the remaining 236 colors, which you can set using the Palette Manager.</span></span>

<span data-ttu-id="fb0fb-113">預設會選取20色 *邏輯調色板* ，並實現到裝置內容中。</span><span class="sxs-lookup"><span data-stu-id="fb0fb-113">A default 20-color *logical palette* is selected and realized into a device context.</span></span> <span data-ttu-id="fb0fb-114">您可以建立並使用新的邏輯調色板。</span><span class="sxs-lookup"><span data-stu-id="fb0fb-114">You can create and use a new logical palette.</span></span> <span data-ttu-id="fb0fb-115">若要變更系統調色板，請選取並瞭解您所建立的邏輯調色板。</span><span class="sxs-lookup"><span data-stu-id="fb0fb-115">To change the system palette, select and realize the logical palette you created.</span></span>

<span data-ttu-id="fb0fb-116">您可能會建立邏輯調色板，以指定您想要在 OpenGL 應用程式中顯示的色彩。</span><span class="sxs-lookup"><span data-stu-id="fb0fb-116">You'll probably create a logical palette to specify the colors you want displayed in your OpenGL application.</span></span> <span data-ttu-id="fb0fb-117">使用特定的 GDI 呼叫，您可以暫時以邏輯調色板取代大部分的系統元件。</span><span class="sxs-lookup"><span data-stu-id="fb0fb-117">Using certain GDI calls, you can temporarily replace most of the system palette with a logical palette.</span></span> <span data-ttu-id="fb0fb-118">您可以使用邏輯調色板，使用 RGBA 或色彩索引模式來定義 GDI 的圖元色彩。</span><span class="sxs-lookup"><span data-stu-id="fb0fb-118">Using a logical palette, you can define pixel colors for the GDI using either the RGBA or the color-index mode.</span></span> <span data-ttu-id="fb0fb-119">邏輯元件的大小上限為8位裝置的256色彩，而真色彩裝置上的4096色彩 (16、24和32位) 。</span><span class="sxs-lookup"><span data-stu-id="fb0fb-119">The maximum size of a logical palette is 256 colors for 8-bit devices and 4,096 colors on a true-color device (16, 24, and 32 bits).</span></span>

<span data-ttu-id="fb0fb-120">如需 RGBA 和色彩索引模式的詳細資訊，請參閱 [Rgba 模式和 Windows 調色板管理](rgba-mode-and-windows-palette-management.md) 、 [OpenGL 色彩模式和 windows 元件管理](opengl-color-modes-and-windows-palette-management.md)。</span><span class="sxs-lookup"><span data-stu-id="fb0fb-120">For more information on the RGBA and color-index modes, see [RGBA Mode and Windows Palette Management](rgba-mode-and-windows-palette-management.md) and [OpenGL Color Modes and Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).</span></span>

 

 




