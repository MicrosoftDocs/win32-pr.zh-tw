---
title: 移植色彩、陰影和 Writemask 程式碼
description: 移植色彩、陰影和 Writemask 程式碼
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- 鳶尾花 GL 移植，色彩
- 從鳶尾花 GL 進行移植，色彩
- 從鳶尾花 GL 移植至 OpenGL，色彩
- 從鳶尾花 GL 的 OpenGL 移植，色彩
- 鳶尾花 GL 移植，網底
- 從鳶尾花 GL 進行移植，網底
- 從鳶尾花 GL 移植至 OpenGL，網底
- 從鳶尾花 GL 的 OpenGL 移植，網底
- 鳶尾花 GL 移植，writemask
- 從鳶尾花 GL、writemask 移植
- 從鳶尾花 GL （writemask）移植至 OpenGL
- 從鳶尾花 GL writemask 的 OpenGL 移植
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8bc35986bc0f9d7076411fecbd9c1fa5d7bfbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671844"
---
# <a name="porting-color-shading-and-writemask-code"></a>移植色彩、陰影和 Writemask 程式碼

將色彩、陰影和 writemask 程式碼移植至 OpenGL 時，請記住下列幾點：

-   雖然您可以使用 OpenGL [glIndex](glindex-functions.md) 函式來設定色彩對應索引，但 opengl 沒有載入色彩對應索引的函式。
-   色彩值會正規化為其資料類型。  (需色彩值的相關資訊，請參閱 [glColor](glcolor-functions.md)) 。
-   **Cpack** 沒有很簡單的對等用法。
-   您可能必須將包含 **c** 或 **color** 函數的程式碼轉譯為 [**glClearColor**](glclearcolor.md) 或 [**GlClearIndex**](glclearindex.md) ，而不是 **glColor** 或 **glIndex**。
-   RGBA writemask 適用于每個元件，但不適用每個位。
-   鳶尾花 GL 提供定義的色彩常數：黑色、藍色、紅色、綠色、洋紅、青色、黃色和白色。 OpenGL 不提供這些常數。

本主題包含下列各項的相關資訊。

-   [移植色彩呼叫](porting-color-calls.md)
-   [移植網底模型](porting-shading-models.md)

 

 




