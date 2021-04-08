---
title: 翻譯 texdef
description: 下列程式碼範例是鳶尾花 GL 材質定義
ms.assetid: bb2d257d-ee74-4a65-b364-c7a97bccaa78
keywords:
- 鳶尾花 GL 移植，材質
- 從鳶尾花 GL、材質移植
- 從鳶尾花 GL 移植至 OpenGL，材質
- 從鳶尾花 GL （紋理）移植的 OpenGL
- 紋理
- 鳶尾花 GL 移植，texdef
- 從鳶尾花 GL、texdef 移植
- 從鳶尾花 GL （texdef）移植至 OpenGL
- 從鳶尾花 GL texdef 的 OpenGL 移植
- texdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479af06bcfd3a50daf56fb0629e4c32f24750081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840695"
---
# <a name="translating-texdef"></a>翻譯 texdef

下列程式碼範例是鳶尾花 GL 材質定義：


```C++
float texprops[] = { TX_MINFILTER, TX_POINT, 
                         TX_MAGFILTER, TX_POINT, 
                         TX_WRAP_S, TX_REPEAT, 
                         TX_WRAP_T, TX_REPEAT, 
                         TX_NULL }; 
 
textdef2d(1, 1, 6, 6, granite_texture, 7, texprops);
```



在上述範例中， **texdef** 會將 tx \_ 點篩選指定為縮放比例和最小化篩選，並將 tx \_ 重複作為包裝機制。 它也會指定材質影像： **花崗岩 \_ 材質**。

在 OpenGL 中， [**glTexImage**](glteximage1d.md) 會指定影像，而 [glTexParameter](gltexparameter-functions.md) 會設定屬性。 若要轉譯鳶尾花 GL 材質定義，請以 **glTexImage** 和一或多個 **glTexParameter** 呼叫來取代 **textdef** 函數。

上述鳶尾花 GL 程式碼在轉譯為 OpenGL 時看起來像這樣：


```C++
GLfloat nearest[] = {GL_NEAREST}; 
GLfloat repeat = {GL_REPEAT}; 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MIN_FILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_MAGILTER, nearest); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_S, repeat); 
glTexParameterfv( GL_TEXTURE_1D, GL_TEXTURE_WRAP_T, nearest); 
glTexImage1D( GL_TEXTURE_1D, 0, 1, 6, 0, GL_RGB, GL_UNSIGNED_SHORT, granite_texture);
```



下表列出鳶尾花 GL 材質參數及其對等的 OpenGL 參數。



| 鳶尾花 GL 材質參數 | OpenGL 材質參數                                  |
|---------------------------|-----------------------------------------------------------|
| TX \_ MINFILTER             | GL \_ 材質 \_ 最小 \_ 篩選                                  |
| TX \_ MAGFILTER             | GL \_ 紋理 \_ MAG \_ 篩選                                  |
| 德克薩斯 \_ 換行，德克薩斯 \_ 換行 \_     | GL \_ 材質 \_ 換行 \_                                      |
| 德克薩斯 \_ 換行，德克薩斯 \_ 換行 \_ T     | GL \_ 紋理 \_ WRAP \_ TGL \_ 材質 \_ 框線 \_ 色彩<br/> |



 

下表列出鳶尾花 GL 材質參數的可能值，以及其對等的 OpenGL 參數。



| 鳶尾花 GL 材質參數 | OpenGL 材質參數     |
|---------------------------|------------------------------|
| TX \_ 點                 | \_最接近的 GL                  |
| TX \_ 雙線性              | GL \_ 線性                   |
| TX \_ MIPMAP \_ 點         | 最接近最接近 MIPMAP 的 GL \_ \_ \_ |
| TX \_ MIPMAP \_ 雙線性      | \_最接近的 GL 線性 \_ MIPMAP \_  |
| TX \_ MIPMAP \_ 線性        | GL \_ 最接近 \_ MIPMAP \_ 線性  |
| TX \_ 三線性             | GL \_ 線性 \_ MIPMAP \_ 線性   |



 

 

 





