---
title: 移植網底模型
description: OpenGL 與鳶尾花 GL 一樣，可讓您在平滑 (Gouraud) 陰影和平坦陰影之間切換。 下表列出鳶尾花 GL 陰影和遞色函式，以及其對等的 OpenGL 函數。
ms.assetid: 93e8f437-381f-4620-ad6f-52ce830d99b6
keywords:
- 鳶尾花 GL 移植，網底
- 從鳶尾花 GL 進行移植，網底
- 從鳶尾花 GL 移植至 OpenGL，網底
- 從鳶尾花 GL 的 OpenGL 移植，網底
- 平滑陰影
- Gouraud 網底
- 平面網底
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124bb002f6f133b4d47dd40e1a0e8738c512ce99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301380"
---
# <a name="porting-shading-models"></a>移植網底模型

OpenGL 與鳶尾花 GL 一樣，可讓您在平滑 (Gouraud) 陰影和平坦陰影之間切換。 下表列出鳶尾花 GL 陰影和遞色函式，以及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數                                   | OpenGL 函數                                                                                    | 意義                      |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|------------------------------|
| **shademodel** (一般)                                | [**glShadeModel**](glshademodel.md) ( GL 一般 \_ )                                                   | 會進行平面陰影。           |
| **shademodel** (GOURAUD)                             | **glShadeModel** ( GL \_ 平滑 )                                                                      | 會順暢地陰影。         |
| **getsm**                                          | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ 網底 \_ 模型 )       | 傳回目前的陰影模型。 |
|  \_) **遞色** 上的遞色 (dt (DT \_ 關閉)  <br/> | [**glEnable**](glenable.md) ( gl \_ 遞色 ) [**glDisable**](gldisable.md) ( gl \_ 遞色 ) <br/> | 開啟/關閉遞色。      |



 

??

 

 





