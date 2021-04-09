---
title: 翻譯 tevdef
description: 下列程式碼範例是鳶尾花 GL 紋理環境定義，可指定電視 \_ DECAL 材質-環境參數
ms.assetid: bb4c8231-8102-4ecb-a5d2-c41243c2682d
keywords:
- 鳶尾花 GL 移植，材質
- 從鳶尾花 GL、材質移植
- 從鳶尾花 GL 移植至 OpenGL，材質
- 從鳶尾花 GL （紋理）移植的 OpenGL
- 紋理
- 鳶尾花 GL 移植，tevdef
- 從鳶尾花 GL、tevdef 移植
- 從鳶尾花 GL （tevdef）移植至 OpenGL
- 從鳶尾花 GL tevdef 的 OpenGL 移植
- tevdef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac2610d1467adb6faa1ea105fc8e8734bfb9c4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932530"
---
# <a name="translating-tevdef"></a>翻譯 tevdef

下列程式碼範例是鳶尾花 GL 紋理環境定義，可指定電視 \_ DECAL 材質環境參數：


```C++
float tevprops[] = {TV_DECAL, TV_NULL}; 
 
tevdef(1, 0, tevprops);
```



和轉譯為 OpenGL 的相同程式碼：


```C++
glTexEnvfv(GL_TEXTURE_ENV, GL_TEXTURE_ENV_MODE, GL_DECAL);
```



下表列出鳶尾花 GL 紋理環境參數及其對等的 OpenGL 參數。



| 鳶尾花 GL 參數     | OpenGL 參數             |
|-----------------------|------------------------------|
| 電視 \_ LAMBERT          | GL \_ LAMBERT                 |
| 電視 \_ DECAL             | GL \_ DECAL                    |
| 電視 \_ BLEND             | GL \_ BLEND                    |
| 電視 \_ 色彩             | GL \_ 紋理 \_ 環境 \_ 色彩      |
| 電視 \_ ALPHA             | 沒有直接 OpenGL 對等專案。 |
| TV \_ 元件 \_ 選取 | 沒有直接 OpenGL 對等專案。 |



 

如需有關紋理環境參數的詳細資訊，請參閱 [**glTexEnv**](gltexenv-functions.md)。

 

 




