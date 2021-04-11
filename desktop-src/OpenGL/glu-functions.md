---
title: X.GLU 隊函式
description: X.GLU 隊函式
ms.assetid: 8304a291-1a26-42bc-8887-386732980722
keywords:
- OpenGL、X.GLU 隊程式庫函數
- OpenGL 參考，X.GLU 隊程式庫函數
- X.GLU 隊程式庫，函數
- OpenGL 公用程式 (X.GLU 隊) ，函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fae3ece873f4e1e015861f597c0d51ebfc3436de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372059"
---
# <a name="glu-functions"></a>X.GLU 隊函式

本節包含所有 OpenGL 公用程式程式庫函式的參考頁面（依字母順序）。 如需這些函式的背景資訊，請參閱 [OpenGL 公用程式程式庫](opengl-utility-library.md)。



| 函式                                                                                           | 描述                                                                                              |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**gluBeginCurve**](glubegincurve.md)、 [ **gluEndCurve**](gluendcurve.md)                         | 分隔非統一的有理數 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 曲線定義。 |
| [**gluBeginPolygon**](glubeginpolygon.md)、 [ **gluEndPolygon**](gluendpolygon.md)                 | 分隔多邊形描述。                                                                           |
| [**gluBeginSurface**](glubeginsurface.md)、 [ **gluEndSurface**](gluendsurface.md)                 | 分隔 NURBS 介面定義。                                                                      |
| [**gluBeginTrim**](glubegintrim.md)、 [ **gluEndTrim**](gluendtrim.md)                             | 分隔 NURBS 修剪迴圈定義。                                                                |
| [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)                                                     | 建立 1-D mipmap。                                                                                     |
| [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)                                                     | 建立 2D mipmap。                                                                                     |
| [**gluCylinder**](glucylinder.md)                                                                 | 繪製圓柱。                                                                                        |
| [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md)                                           | 終結 NURBS 物件。                                                                                 |
| [**gluDeleteQuadric**](gludeletequadric.md)                                                       | 終結 quadric 物件。                                                                               |
| [**gluDeleteTess**](gludeletetess.md)                                                             | 終結鑲嵌式物件。                                                                          |
| [**gluDisk**](gludisk.md)                                                                         | 繪製磁片。                                                                                            |
| [**gluErrorString**](gluerrorstring.md)                                                           | 從 OpenGL 或 X.GLU 隊錯誤碼產生錯誤字串。 錯誤字串僅為 ANSI。                |
| [**gluGetNurbsProperty**](glugetnurbsproperty.md)                                                 | 捕獲 NURBS 屬性。                                                                              |
| [**gluGetString**](glugetstring.md)                                                               | 抓取描述 X.GLU 隊版本號碼或支援之 X.GLU 隊延伸模組呼叫的字串。               |
| [**gluGetTessProperty**](glugettessproperty.md)                                                   | 抓取鑲嵌物件屬性。                                                                |
| [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)                                         | 載入 NURBS 取樣和剔除矩陣。                                                               |
| [**gluLookAt**](glulookat.md)                                                                     | 定義「查看」轉換。                                                                        |
| [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)                                                 | 建立 NURBS 物件。                                                                                  |
| [**gluNewQuadric**](glunewquadric.md)                                                             | 建立 quadric 物件。                                                                                |
| [**gluNewTess**](glunewtess.md)                                                                   | 建立鑲嵌式物件。                                                                           |
| [**gluNextContour**](glunextcontour.md)                                                           | 標記另一個輪廓的開頭。                                                                  |
| [*gluNurbsCallback*](glunurbs.md)                                                                 | 定義 NURBS 物件的回呼。                                                                   |
| [**gluNurbsCurve**](glunurbscurve.md)                                                             | 定義 NURBS 曲線的形狀。                                                                      |
| [**gluNurbsProperty**](glunurbsproperty.md)                                                       | 設定 NURBS 屬性。                                                                                   |
| [**gluNurbsSurface**](glunurbssurface.md)                                                         | 定義 NURBS 表面的形狀。                                                                    |
| [**gluOrtho2D**](gluortho2d.md)                                                                   | 定義2D 正向投射矩陣。                                                            |
| [**gluPartialDisk**](glupartialdisk.md)                                                           | 繪製磁片的弧形。                                                                                  |
| [**gluPerspective**](gluperspective.md)                                                           | 設定透視圖投影矩陣。                                                                 |
| [**gluPickMatrix**](glupickmatrix.md)                                                             | 定義挑選區域。                                                                                |
| [**gluProject**](gluproject.md)                                                                   | 將物件座標組應至視窗座標。                                                           |
| [**gluPwlCurve**](glupwlcurve.md)                                                                 | 描述分段線性 NURBS 修剪曲線。                                                       |
| [*gluQuadricCallback*](gluquadric.md)                                                             | 定義 quadric 物件的回呼。                                                                 |
| [**gluQuadricDrawStyle**](gluquadricdrawstyle.md)                                                 | 指定 quadrics 所需的繪製樣式。                                                           |
| [**gluQuadricNormals**](gluquadricnormals.md)                                                     | 指定要用於 quadrics 的法線類型。                                              |
| [**gluQuadricOrientation**](gluquadricorientation.md)                                             | 指定 quadrics 的內部或外部方向。                                                    |
| [**gluQuadricTexture**](gluquadrictexture.md)                                                     | 指定是否要將 quadrics 設為紋理。                                                           |
| [**gluScaleImage**](gluscaleimage.md)                                                             | 將影像調整為任意大小。                                                                    |
| [**gluSphere**](glusphere.md)                                                                     | 繪製球體。                                                                                          |
| [**gluTessBeginContour**](glutessbegincontour.md)、 [ **gluTessEndContour**](glutessendcontour.md) | 分隔分佈描述。                                                                           |
| [**gluTessBeginPolygon**](glutessbeginpolygon.md)、 [ **gluTessEndPolygon**](glutessendpolygon.md) | 分隔多邊形描述。                                                                           |
| [*gluTessCallback*](glutess.md)                                                                   | 定義鑲嵌式物件的回呼。                                                            |
| [**gluTessNormal**](glutessnormal.md)                                                             | 指定多邊形的一般。                                                                        |
| [**gluTessProperty**](glutessproperty.md)                                                         | 設定鑲嵌式物件的屬性。                                                              |
| [**gluTessVertex**](glutessvertex.md)                                                             | 指定多邊形上的頂點。                                                                         |
| [**gluUnProject**](gluunproject.md)                                                               | 地圖視窗座標與物件座標。                                                           |



 

 

 




