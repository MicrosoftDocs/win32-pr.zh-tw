---
title: 翻譯 texgen
description: 鳶尾花 GL 函數 texgen 會轉譯為適用于 OpenGL 的 glTexGen。
ms.assetid: ddf398ed-37d4-4fb6-97be-20fe0564cb77
keywords:
- 鳶尾花 GL 移植，材質
- 從鳶尾花 GL、材質移植
- 從鳶尾花 GL 移植至 OpenGL，材質
- 從鳶尾花 GL （紋理）移植的 OpenGL
- 紋理
- 鳶尾花 GL 移植，texgen
- 從鳶尾花 GL、texgen 移植
- 從鳶尾花 GL （texgen）移植至 OpenGL
- 從鳶尾花 GL texgen 的 OpenGL 移植
- texgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07654fc35e20096ed71c3fe74ff9279214eb45c8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106999786"
---
# <a name="translating-texgen"></a>翻譯 texgen

鳶尾花 GL 函數 **texgen** 會轉譯為適用于 OpenGL 的 [glTexGen](gltexgen-functions.md) 。

使用鳶尾花 GL，您可以呼叫 **texgen** 兩次：一次設定模式和平面方程式，以及啟用紋理座標產生。 例如：


```C++
texgen(TX_S, TG_LINEAR, planeParams); 
texgen(TX_S, TG_ON, NULL);
```



使用 OpenGL 時，您會進行三次呼叫：兩個到 **glTexGen** (一次設定模式，一次是設定平面方程式) ，另一次則是 [**glEnable**](glenable.md)。 例如，與上述鳶尾花 GL 程式碼相等的 OpenGL 為：


```C++
glTexGen(GL_S, GLTEXTURE_GEN_MODE, modeName); 
glTextGen(GL_S, GL_OBJECT_PLANE, planeParameters); 
glEnable(GL_TEXTURE_GEN_S);
```



下表列出鳶尾花 GL 紋理座標名稱及其 OpenGL 對應專案。



| 鳶尾花 GL 紋理座標 | OpenGL 材質座標 | glEnable 引數   |
|----------------------------|---------------------------|---------------------|
| 德克薩斯 \_ 州                      | GL \_ S                     | GL \_ 材質 \_ GEN \_ S |
| TX \_ T                      | GL \_ T                     | GL \_ 材質 \_ GEN \_ T |
| TX \_ R                      | GL \_ R                     | GL \_ 材質 \_ GEN \_ R |
| 德克薩斯州 \_ Q                      | GL \_ Q                     | GL \_ 材質 \_ GEN \_ Q |



 

下表列出鳶尾花 GL 材質產生模式及其對等的 OpenGL 材質模式和平面名稱。



| 鳶尾花 GL 材質模式 | OpenGL 材質模式 | OpenGL 平面名稱 |
|----------------------|---------------------|-------------------|
| TG \_ 線性           | GL \_ 物件 \_ 線性  | GL \_ 物件 \_ 平面 |
| TG \_ 輪廓          | GL \_ 眼 \_ 線性     | GL \_ 眼 \_ 平面    |
| TG \_ SPHEREMAP        | GL \_ 球體 \_ 地圖     |                   |



 

 

 




