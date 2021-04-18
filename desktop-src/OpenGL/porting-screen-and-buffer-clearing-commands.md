---
title: 移植螢幕和緩衝區清除命令
description: OpenGL 以單一函式 glClear 來取代各種鳶尾花 GL clear 函式 (例如 zclear、aclear、sclear 等) 。 藉由將遮罩傳遞給 glClear，指定您想要清除的內容。
ms.assetid: 52ba503d-e412-4815-a039-a039b41327f4
keywords:
- 鳶尾花 GL 移植，清除功能
- 從鳶尾花 GL 進行移植，清除函式
- 從鳶尾花 GL 移植至 OpenGL，清除函式
- 從鳶尾花 GL 的 OpenGL 移植，清除函式
- 清除函式
- 鳶尾花 GL 移植，螢幕清除命令
- 從鳶尾花 GL 進行移植，螢幕清除命令
- 從鳶尾花 GL 移植至 OpenGL，螢幕清除命令
- 從鳶尾花 GL、螢幕清除命令的 OpenGL 移植
- 螢幕清除命令
- 鳶尾花 GL 移植，緩衝區清除命令
- 從鳶尾花 GL 進行移植，緩衝區清除命令
- 從鳶尾花 GL 移植至 OpenGL，緩衝區清除命令
- 從鳶尾花 GL 進行 OpenGL 移植，緩衝區清除命令
- 緩衝區清除命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53566c9fe14922f3965133cef9e30cbea4548b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965596"
---
# <a name="porting-screen-and-buffer-clearing-commands"></a>移植螢幕和緩衝區清除命令

OpenGL 以單一函式 [**glClear**](glclear.md)來取代各種鳶尾花 GL **clear** 函式 (例如 **zclear**、 **aclear**、 **sclear** 等) 。 藉由將遮罩傳遞給 **glClear**，指定您想要清除的內容。

移植螢幕和緩衝區命令時，請記住下列幾點：

-   OpenGL 會以 [**glClearColor**](glclearcolor.md) 和 [**glClearIndex**](glclearindex.md)之類的呼叫，與繪製色彩分開維護清除色彩。 清除之前，請務必為每個緩衝區設定 clear 色彩。
-   您現在不需要使用數種不同的命名明確呼叫，而是使用一個呼叫、 [**glClear**](glclear.md)、 **or** 等的緩衝區遮罩來清除數個緩衝區。 例如， **czclear** 會取代為：

    ``` syntax
    glClear( GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT )
    ```

-   鳶尾花 GL 參考多邊形 stipple 和色彩 writemask。 OpenGL 會忽略多邊形 stipple，但會參考色彩 writemask。  (**czclear** 函式會忽略多邊形 stipple 和色彩 writemask。 ) 

下表列出各種鳶尾花 GL clear 函式與其對等的 OpenGL 函數。



| 鳶尾花 GL 通話         | OpenGL 呼叫                                                               | 意義                                           |
|----------------------|---------------------------------------------------------------------------|---------------------------------------------------|
| **acbuf** (AC \_ CLEAR)  | **glClear** ( GL \_ ACCUM \_ 緩衝區 \_ 位 )                                      | 清除累積緩衝區。                    |
|                      | **glClearColor**                                                          | 設定 RGBA 清除色彩。                         |
|                      | **glClearIndex**                                                          | 設定清除色彩索引。                        |
| **清除**            | **glClear** ( GL \_ 色彩 \_ 緩衝區 \_ 位 )                                      | 清除色彩緩衝區。                           |
|                      | **glClearDepth**                                                          | 指定深度緩衝區的清除值。     |
| **zclear**           | **glClear** ( GL \_ 深度 \_ 緩衝區 \_ 位 )                                      | 清除深度緩衝區。                           |
| **czclear**          | **glClear** ( GL \_ 色彩 \_ 緩衝區 \_ 位 \| GL \_ 深度 \_ 緩衝區 \_ 位 ) <br/> | 清除色彩緩衝區和深度緩衝區。      |
|                      | **glClearAccum**                                                          | 指定累積緩衝區的明確值。 |
|                      | **glClearStencil**                                                        | 指定樣板緩衝區的清除值。   |
| **sclear**           | **glClear** ( GL \_ 樣板 \_ 緩衝區 \_ 位 )                                    | 清除樣板緩衝區。                         |



 

當您的鳶尾花 GL 程式碼同時使用 **gclear** 和 **sclear** 時，您可以將它們結合成單一 **glClear** 呼叫;可以改善您的程式效能。

 

 





