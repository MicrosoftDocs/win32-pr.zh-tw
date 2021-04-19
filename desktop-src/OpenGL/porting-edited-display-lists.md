---
title: 移植已編輯的顯示清單
description: 雖然您無法編輯 OpenGL 顯示清單，但您可以藉由嵌套顯示清單來取得類似的結果，然後終結和建立新版本的清單子。
ms.assetid: b7f7ffed-c3de-43d4-bff2-f244faa3a27a
keywords:
- 鳶尾花 GL 移植，顯示清單
- 從鳶尾花 GL 進行移植，顯示清單
- 從鳶尾花 GL 移植至 OpenGL，顯示清單
- 從鳶尾花 GL 的 OpenGL 移植，顯示清單
- 顯示清單，從鳶尾花 GL 進行移植
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5555c850d4695ba3732b61c0a41b7aedd8af0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106984931"
---
# <a name="porting-edited-display-lists"></a><span data-ttu-id="2136f-108">移植已編輯的顯示清單</span><span class="sxs-lookup"><span data-stu-id="2136f-108">Porting Edited Display Lists</span></span>

<span data-ttu-id="2136f-109">雖然您無法編輯 OpenGL 顯示清單，但您可以藉由嵌套顯示清單來取得類似的結果，然後終結和建立新版本的清單子。</span><span class="sxs-lookup"><span data-stu-id="2136f-109">Although you can't edit OpenGL display lists, you can get similar results by nesting display lists and then destroying and creating new versions of the sublists.</span></span> <span data-ttu-id="2136f-110">例如：</span><span class="sxs-lookup"><span data-stu-id="2136f-110">For example:</span></span>

``` syntax
glNewList (1, GL_COMPILE); 
    glIndexi(MY_RED); 
glEndlist(); 
 
glNewList(2, GL_COMPILE); 
    glScalef(1.2, 1.2, 1.0); 
glEndList(); 
 
glNewList(3, GL_COMPILE); 
    glCallList(1); 
    glCallList(2); 
glEndList(); 
 
glDeleteLists(1, 2); 
glNewList(1, GL_COMPILE); 
    glIndexi(MY_CYAN); 
glEndList(); 
glNewList(2, GL_COPILE); 
    glScalef(0.5, 0.5, 1.0); 
glEndList;
```

 

 




