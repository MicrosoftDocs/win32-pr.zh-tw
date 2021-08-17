---
title: 移植顯示清單
description: 顯示清單的 OpenGL 執行類似于鳶尾花 GL 的執行，在 OpenGL 中有兩個例外狀況：當您建立顯示清單並無法從顯示清單中呼叫函式時，就無法編輯顯示清單。
ms.assetid: 617e19ff-6a55-4f7c-b229-075cdee8f1cf
keywords:
- 鳶尾花 GL 移植，顯示清單
- 從鳶尾花 GL 進行移植，顯示清單
- 從鳶尾花 GL 移植至 OpenGL，顯示清單
- 從鳶尾花 GL 的 OpenGL 移植，顯示清單
- 顯示清單，從鳶尾花 GL 進行移植
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858f1f3be180b3ef09c81bb8d61b18705fc9485742d7384562eecff142f4bfb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980800"
---
# <a name="porting-display-lists"></a>移植顯示清單

顯示清單的 OpenGL 執行類似于鳶尾花 GL 的執行，但有兩個例外：在 OpenGL 中，您無法在建立後編輯顯示清單，也無法從顯示清單中呼叫函數。

因為您無法在顯示清單內編輯或呼叫函式，所以這些鳶尾花 GL 函式在 OpenGL 中沒有對等專案：

-   **editobj**
-   **objdelete**、 **objinsert** 和 **objreplace**
-   **maketag**、 **gentag**、 **istag** 和 **deltag**
-   **callfunc**

在鳶尾花 GL 中，您可以使用 **makeobj** 和 **closeobj** 函數來建立顯示清單。 在 OpenGL 中，您會使用 [**glNewList**](glnewlist.md) 和 [**glEndList**](glendlist.md)。

下表列出鳶尾花 GL 顯示清單函式與其對等的 OpenGL 函數。



| 鳶尾花 GL 函數 | OpenGL 函數                                                      | 意義                                                       |
|------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| **makeobj**      | **glNewList**                                                        | 建立新的顯示清單。                                   |
| **closeobj**     | **glEndList**                                                        | 信號顯示清單的結尾。                                  |
| **callobj**      | [**glCallList**](glcalllist.md)、 [ **glCallLists**](glcalllists.md) | 執行顯示清單或清單。                               |
| **isobj**        | [**glIsList**](glislist.md)                                         | 顯示清單存在的測試。                             |
| **delobj**       | [**glDeleteLists**](gldeletelists.md)                               | 刪除連續的顯示清單群組。                    |
| **genobj**       | [**glGenLists**](glgenlists.md)                                     | 產生指定數目的連續空白顯示清單。 |



 

本主題包含下列各項的相關資訊。

-   [移植 bbox2 函式](porting-the-bbox2-function.md)
-   [移植已編輯的顯示清單](porting-edited-display-lists.md)
-   [顯示清單的範例埠](a-sample-port-of-a-display-list.md)

 

 




