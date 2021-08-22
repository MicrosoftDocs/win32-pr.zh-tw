---
title: 重迭、基礎和主要平面
description: 您可以在應用程式中使用硬體層平面 (重迭和基礎平面) 。
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- Windows 上的 OpenGL、硬體層平面
- 硬體層平面 OpenGL
- 覆蓋平面 OpenGL
- 基礎平面 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b968a0ab028fd0a699e31ad3a3601d7140435e2b36d0188bef46c5dca7cbad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936487"
---
# <a name="overlay-underlay-and-main-planes"></a>重迭、基礎和主要平面

您可以在應用程式中使用硬體層平面 (重迭和基礎平面) 。 使用 Windows，像素格式會描述圖形裝置的圖元設定。 每個像素格式都會描述主要色彩緩衝區的深度和其他特性，並描述其他緩衝區 (例如主要平面使用的深度、累積、樣板和輔助) 。 像素格式現在已擴充，以包含重迭和基礎緩衝區。

圖層平面一律具有 front 左邊的色彩緩衝區，也可以包含 front 和上一頁色彩緩衝區。 每個圖層平面都有特定的轉譯內容，可轉譯成圖層緩衝區。 您無法在圖層平面中使用 GDI 繪圖函數。

視窗會管理圖層平面的色彩緩衝區，與管理主平面色彩緩衝區的方式相似。 您可以同時顯示多個具有重迭及/或基礎平面的視窗。 您無法擁有可在主要繪圖平面中的任何視窗上移動的自由浮動重迭視窗。 此外，因為它會在視窗中隨時遮蔽基礎平面，所以您無法使用沒有透明色彩的硬體快顯平面。

視窗中的每個圖層平面都有相關聯的調色板。 您可以設定 [色彩索引圖層] 平面的 [調色板]，但您可以修正 RGBA 色彩平面的調色板。 當視窗在前景時，您必須實現適當的調色板。 圖層平面具有透明的圖元色彩或索引，可讓任何基礎圖層平面顯示。

您可以在不同的分層平面中，將轉譯內容的狀態複製到另一個呈現內容。 您也可以在不同的分層平面中，共用轉譯內容之間的顯示清單。

下列函式適用于圖層平面：

-   [**wglCopyCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [**wglCreateLayerCoNtext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [**wglDescribeLayerPlane**](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [**wglGetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [**wglRealizeLayerPalette**](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [**wglSetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [**wglSwapLayerBuffers**](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




