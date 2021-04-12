---
title: 移植 NURBS 物件
description: OpenGL 會將 NURBS 視為物件，類似于 quadrics 您建立 NURBS 物件的方式，然後指定其呈現方式。 下表列出用來管理 NURBS 物件的 OpenGL X.GLU 隊函數。
ms.assetid: baddf81b-219f-44bb-aa17-37404028b258
keywords:
- 鳶尾花 GL 移植，NURBS 物件
- 從鳶尾花 GL、NURBS 物件移植
- 從鳶尾花 GL （NURBS 物件）移植至 OpenGL
- 鳶尾花 GL、NURBS 物件的 OpenGL 移植
- NURBS 物件
- 'NURBS (非統一的有理 B 曲線) '
- '非統一的有理 B 曲線 (NURBS) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0e56c06eea4e4a9a48f9062205277f8b999499
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372365"
---
# <a name="porting-nurbs-objects"></a>移植 NURBS 物件

OpenGL 會將 NURBS 視為物件，類似于其處理 quadrics 的方式：您會建立 NURBS 物件，然後指定其呈現方式。 下表列出用來管理 NURBS 物件的 OpenGL X.GLU 隊函數。



| OpenGL X.GLU 隊函式                                      | 意義                                                        |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)       | 建立新的 NURBS 物件。                                    |
| [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) | 刪除 NURBS 物件。                                        |
| [*gluNurbsCallback*](glunurbs.md)                       | 將回呼與 NURBS 物件產生關聯，以進行錯誤處理。 |



 

將鳶尾花 GL NURBS 程式碼移植至 OpenGL 時，請記住下列幾點：

-   NURBS 控制點是浮點數，不是雙精度浮點數。
-   Stride 參數會以浮點數計算，而不是以位元組計算。
-   如果您使用的是光源，但未指定法線，請以 GL AUTO NORMAL 呼叫 [**glEnable**](glenable.md) ， \_ \_ 以自動產生法線的參數。

??

 

 




