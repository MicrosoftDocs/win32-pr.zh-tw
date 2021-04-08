---
title: 移植色彩呼叫
description: 下表列出鳶尾花 GL 色彩函數及其對等的 OpenGL 函數。
ms.assetid: 4ca6c311-d6c8-4d10-9e9c-770a8e6de4bb
keywords:
- 鳶尾花 GL 移植，色彩
- 從鳶尾花 GL 進行移植，色彩
- 從鳶尾花 GL 移植至 OpenGL，色彩
- 從鳶尾花 GL 的 OpenGL 移植，色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 856b9f9d0a62b866ac1c9981d9fbb716cf243341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671843"
---
# <a name="porting-color-calls"></a>移植色彩呼叫

下表列出鳶尾花 GL 色彩函數及其對等的 OpenGL 函數。



| 鳶尾花 GL 函數                  | OpenGL 函數                                                                                                                               | 意義                                              |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **c**                             | [glColor](glcolor-functions.md)                                                                                                              | 設定 RGB 色彩。                                      |
| **color**                         | [glIndex](glindex-functions.md)                                                                                                              | 設定色彩索引。                                |
| **getcolor**                      | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ 目前 \_ 索引 )                                                | 傳回目前的色彩索引。                     |
| **getmcolor**                     |                                                                                                                                               | 取得色彩對應專案的 RGB 值複本。 |
| **gRGBcolor**                     | **glGet** ( GL \_ 目前 \_ 色彩 )                                                                                                                | 取得目前的 RGB 色彩值。                   |
| **mapcolor**                      |                                                                                                                                               |                                                      |
| **RGBcolor**                      | **glColor**                                                                                                                                   | 設定 RGB 色彩。                                      |
| **writemask**                     | [**glIndexMask**](glindexmask.md)                                                                                                            | 設定色彩索引模式的色遮罩。                |
| **wmpackRGBwritemask**<br/> | [**glColorMask**](glcolormask.md)                                                                                                            | 設定 RGB 色彩模式遮罩。                        |
| **getwritemask**                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( gl \_ COLOR \_ WRITEMASK ) **glGet** ( gl \_ INDEX \_ WRITEMASK ) <br/> | 取得色遮罩。                                 |
| **gRGBmask**                      | **glGet** ( GL \_ 色彩 \_ WRITEMASK )                                                                                                              | 取得色遮罩。                                 |
| **zwritemask**                    | [**glDepthMask**](gldepthmask.md)                                                                                                            |                                                      |



 

> [!Note]
>
> 以 [**glDepthMask**](gldepthmask.md)取代 **zwritemask** 時請務必小心;**glDepthMask** 接受布林值引數，而 **zwritemask** 則會使用位欄位。

 

如果您想要使用多個色彩對應，您需要使用適當的 Windows 色彩對應功能。 因此， **multimap**、 **onemap**、 **getcmmode**、 **setmap** 和 **getmap** 沒有 OpenGL 對等專案。

 

 





