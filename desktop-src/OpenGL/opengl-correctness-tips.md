---
title: OpenGL 正確性秘訣
description: OpenGL 正確性秘訣
ms.assetid: 48397fbf-823d-4ea0-adfd-2c639e20e38f
keywords:
- OpenGL、正確性秘訣
- OpenGL、最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5294d2e989591216ea8cf66aa380933718776f2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372052"
---
# <a name="opengl-correctness-tips"></a>OpenGL 正確性秘訣

遵循下列指導方針來建立可依您預期執行的 OpenGL 應用程式：

-   假設 OpenGL 實作為未來版本中的錯誤行為可能會變更。 OpenGL 錯誤語義在未來的修訂版本中可能會變更。
-   使用投影矩陣將所有幾何折迭為單一平面。 如果使用模型矩陣，則以眼睛座標運作的 OpenGL 功能 (例如光源和應用程式定義的裁剪平面) 可能會失敗。
-   請勿對單一矩陣進行大量變更。 例如，請勿以增量角度持續呼叫 [**glRotate**](glrotate.md) ，以建立旋轉的動畫。 相反地，請使用 [**glLoadIdentity**](glloadidentity.md) 為每個框架初始化指定的矩陣，然後使用該框架所需的完整角度來呼叫 **glRotate** 。
-   只有在針對符合規範的 OpenGL 執行所建立的 invariance 規則保證此行為時，才會通過轉譯資料庫的多個傳遞來產生相同的圖元片段。 否則，多個階段可能會產生不同的片段集。
-   在定義顯示清單時，不預期會回報錯誤。 只有在執行清單時，顯示清單中的命令才會產生錯誤。
-   若要優化深度緩衝區的作業，請盡可能將接近的錐錐平面放在最接近的觀點。
-   呼叫 [**glFlush**](glflush.md) 來強制執行所有先前的 OpenGL 命令。 請勿在 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 或 [**glIsEnabled**](glisenabled.md) 上計算，以排清轉譯資料流程。 查詢命令會排清傳回有效資料所需的資料流程數量，但不一定會完成所有暫止的轉譯命令。
-   在轉譯 predithered 影像時關閉遞色 (例如， [**glCopyPixels**](glcopypixels.md) 被呼叫時) 。
-   利用累積緩衝區的完整範圍。 例如，如果累積四個映射，則會在每一季累積時進行調整。
-   若要取得精確的二維柵格化，請仔細地指定要進行柵格化之基本專案的正向投射和頂點。 使用整數座標指定正射投射，如下列範例所示。

    ``` syntax
    gluOrtho2D(0, width, 0, height); 
    ```

    參數的 *寬度* 和 *高度* 是區的維度。 在指定此投射矩陣的情況下，將多邊形頂點和圖元影像位置放在整數座標，以可預測的方式表示。 例如， [glRecti](glrect-functions.md) ( 0，0，1，1 ) 可靠地填滿了此區的左下圖元，而 [glRasterPos2i](glrasterpos-functions.md) ( 0、0 ) 可靠地將 unzoomed 影像放置在此區的左下圖元。 不過，點頂點、線條頂點和點陣圖位置應該放在半整數位置。 例如，從 (*x* (1) ，0.5) 到 (*x* (2) ) ，0.5 (將會在圖格中的最底部資料列中可靠地轉譯，而以) 0.5，0.5 ( 繪製的點會可靠地填滿與 glRecti ) 0，0，1，1相同的圖元。

    一種最佳的危害，可讓您在整數位置指定所有基本型別，同時仍然確保可預測的點陣化，也就是將 *x* 和 *y* 轉譯為0.375，如下列程式碼範例所示。 這類轉譯會將多邊形和圖元影像邊緣安全地遠離圖元的中心，同時將線條頂點移至接近圖元中心。

    ``` syntax
    glViewport(0, 0, width, height);
    glMatrixMode(GL_PROJECTION);
    glLoadIdentity( );
    gluOrtho2D(0, width, 0, height);
    glMatrixMode(GL_MODELVIEW);
    glLoadIdentity( );
    glTranslatef(0.375, 0.375, 0.0);
    /* render all primitives at integer positions */
    ```

-   避免使用負 *w* 頂點座標和負 *q* 材質座標。 OpenGL 可能無法正確地裁剪這類座標，而且可能會在這類座標所定義的網底基本專案時產生插補錯誤。

 

 




