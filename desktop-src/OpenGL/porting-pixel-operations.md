---
title: 移植圖元作業
description: 移植圖元作業
ms.assetid: 57917f33-daf5-4db6-9583-ab596deab91a
keywords:
- 鳶尾花 GL 移植，圖元
- 從鳶尾花 GL 進行移植，圖元
- 從鳶尾花 GL 移植至 OpenGL，圖元
- 從鳶尾花 GL 的 OpenGL 移植，圖元
- 從鳶尾花 GL 移植的圖元
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fd484efa031bd12af59cb729c8fa20b68fe88e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674539"
---
# <a name="porting-pixel-operations"></a>移植圖元作業

移植牽涉到圖元運算的程式碼時，請記住下列幾點：

-   邏輯圖元作業不會套用到 RGBA 色彩緩衝區。 如需詳細資訊，請參閱 [**glLogicOp**](gllogicop.md)。
-   一般而言，鳶尾花 GL 會使用 ABGR 格式的圖元，而 OpenGL 則使用 RGBA。 您可以使用 [**glPixelStore**](glpixelstore-functions.md)來變更格式。
-   移植 **lrectwrite** 函式時，請注意 **lrectwrite** 正在撰寫的位置 (例如，它可能會寫入深度緩衝區) 。

OpenGL 可提供您一些額外的圖元運算彈性。 下表列出圖元作業的鳶尾花 GL 函式及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數                                   | OpenGL 函數                                                                           | 意義                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| **lrectread**、 **rectread**、**readRGB**<br/> | [**glReadPixels**](glreadpixels.md)                                                      | 從畫面格緩衝區讀取圖元區塊。                           |
| **lrectwrite**、 **rectwrite**                      | [**glDrawPixels**](gldrawpixels.md)                                                      | 將圖元區塊寫入至畫面格緩衝區。                            |
| **rectcopy**                                       | [**glCopyPixels**](glcopypixels.md)                                                      | 複製畫面格緩衝區中的圖元。                                       |
| **rectzoom**                                       | [**glPixelZoom**](glpixelzoom.md)                                                        | 指定 **glDrawPixels** 和 **glCopyPixels** 的圖元縮放因數。 |
| **cmov**                                           | [glRasterPos](glrasterpos-functions.md)                                                  | 指定圖元作業的點陣位置。                         |
| **readsource**                                     | [**glReadBuffer**](glreadbuffer.md)                                                      | 選取圖元的色彩緩衝區來源。                               |
| **pixmode**                                        | [**glPixelStore**](glpixelstore-functions.md)、[**glPixelTransfer**](glpixeltransfer.md) | 設定圖元儲存模式。設定圖元傳輸模式。                      |
| **logicop**                                        | [**glLogicOp**](gllogicop.md)                                                            | 指定圖元寫入的邏輯運算。                         |
|                                                    | [**glEnable**](glenable.md) ( GL \_ 邏輯 \_ OP )                                             | 開啟圖元邏輯作業。                                        |



 

如需可能邏輯作業的完整清單，請參閱 [**glLogicOp**](gllogicop.md)。

此鳶尾花 GL 程式碼範例顯示一般的圖元寫入：

``` syntax
unsigned long *packedRaster; 
.. 
packedRaster[k] = 0x00000000; 
.. 
lrectwrite(0, 0, xSize, ySize, packedRaster);
```

上述程式碼在轉譯為 OpenGL 時看起來像這樣：

``` syntax
glRasterPos2i( 0, 0); 
glDrawPixels( xSize + 1, ySize + 1, GL_RGBA, GL_UNSIGNED_BYTE, packedRaster);
```

 

 





