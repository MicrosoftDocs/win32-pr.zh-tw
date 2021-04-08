---
title: 需要目前圖形位置的埠程式碼
description: OpenGL 不會維護目前的圖形位置。 相依于目前圖形位置的鳶尾花 GL 函式（例如 move、draw 和 rmv）在 OpenGL 中沒有對等專案。
ms.assetid: d6c42d9c-6fbb-4b72-8097-285d19b619c2
keywords:
- 鳶尾花 GL 移植，目前圖形位置
- 從鳶尾花 GL、目前的圖形位置進行移植
- 從鳶尾花 GL 移植至 OpenGL，目前的圖形位置
- 從鳶尾花 GL、目前圖形位置的 OpenGL 移植
- 目前的圖形位置
- 點陣位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd7e7cbbaf0a22385c83569775758e24f70cd210
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/27/2019
ms.locfileid: "103679264"
---
# <a name="port-code-that-needs-a-current-graphics-position"></a>需要目前圖形位置的埠程式碼

OpenGL 不會維護目前的圖形位置。 相依于目前圖形位置的鳶尾花 GL 函式（例如 **move**、 **draw** 和 **rmv**）在 OpenGL 中沒有對等專案。

較舊版本的鳶尾花 GL 包含依賴目前圖形位置的繪圖命令，但不建議使用它們。 如果您以任何方式使用目前的圖形位置，或使用下列任何常式，您將需要重寫程式碼：

-   **繪製** 和 **移動**
-   **pmv**、 **寮國** 和 **pclos**
-   **rdr**、 **rmv**、 **rpdr** 和 **rpmv**
-   **getgpos**

OpenGL 具有對應至鳶尾花 GL 目前字元位置的點陣位置概念。 如需有關點陣定位的詳細資訊，請參閱 [移植圖元作業](porting-pixel-operations.md)。

本主題包含下列各項的相關資訊。

-   [移植螢幕和緩衝區清除命令](porting-screen-and-buffer-clearing-commands.md)
-   [移植矩陣和轉換函數](porting-matrix-and-transformation-functions.md)
-   [移植 MSINGLE 模式程式碼](porting-msingle-mode-code.md)
-   [移植可取得矩陣和轉換的函式](porting-functions-that-get-matrices-and-transformations.md)
-   [移植區、Screenmasks 和 Scrboxes](porting-viewports--screenmasks--and-scrboxes.md)
-   [移植裁剪平面](porting-clipping-planes.md)

 

 




