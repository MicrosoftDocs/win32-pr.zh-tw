---
title: 移植材質函數
description: 移植材質函數
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- 鳶尾花 GL 移植，材質
- 從鳶尾花 GL、材質移植
- 從鳶尾花 GL 移植至 OpenGL，材質
- 從鳶尾花 GL （紋理）移植的 OpenGL
- 紋理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cba8b105089553084a93f997517d19cf371e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021674"
---
# <a name="porting-texture-functions"></a>移植材質函數

將鳶尾花 GL 材質函數移植至 OpenGL 時，請記住下列幾點：

-   OpenGL 不會維護材質的表格;它只會使用立體材質和2D 材質。 若要從鳶尾花 GL 程式碼重複使用紋理，請將它們放在顯示清單中。
-   OpenGL 不會自動產生 mipmap。 如果您使用的是 mipmap，則必須先呼叫 [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) 函數。
-   在 OpenGL 中，您可以使用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md) 來開啟和關閉紋理功能。
-   在 OpenGL 中，紋理大小比鳶尾花 GL 更嚴格。 OpenGL 材質的大小必須：

    2 *n* + 2 *b*

    其中 *n* 是整數， *b* 是：

    -   0，如果材質沒有框線
    -   1，如果材質有框線圖元 (OpenGL 材質可以有1圖元的框線。 ) 

下表列出鳶尾花 GL 紋理函式及其一般 OpenGL 對應專案。



| 鳶尾花 GL 函數 | OpenGL 函數                                                                                                                                                                                                                                                       | 意義                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **textdef2d**    | [**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/>                                                                                                           | 指定2D 材質影像。                                                              |
| **textbind**     | **glTexImage2DglTexParameter**<br/> **gluBuild2DMipmaps**<br/>                                                                                                                                                                                            | 選取材質函數。                                                                 |
| **tevdef**       | [**glTexEnv**](gltexenv-functions.md)                                                                                                                                                                                                                                | 定義材質對應環境。                                                      |
| **tevbind**      | **glTexEnv**[**glTexImage1D**](glteximage1d.md)<br/>                                                                                                                                                                                                           | 選取材質環境。                                                              |
| <bpt id="p1">**</bpt>t2<ept id="p1">**</ept>           | [**glTexCoord**](gltexcoord-functions.md)                                                                                                                                                                                                                            | 設定目前的材質座標。                                                       |
| **texgen**       | [**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)<br/> [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/> [**gluScaleImage**](gluscaleimage.md)<br/> | 控制材質座標的產生。將影像調整為任意大小。<br/> |



 

如需有關紋理的詳細資訊，請參閱 *OpenGL 程式設計指南*。

本主題包含下列各項的相關資訊。

-   [翻譯 tevdef](translating-tevdef.md)
-   [翻譯 texdef](translating-texdef.md)
-   [翻譯 texgen](translating-texgen.md)

 

 





