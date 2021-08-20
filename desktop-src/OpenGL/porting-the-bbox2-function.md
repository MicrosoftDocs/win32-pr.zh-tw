---
title: 移植 bbox2 函式
description: 鳶尾花 GL bbox2 函數沒有任何 OpenGL 對等專案。
ms.assetid: 2d8082bf-c2c3-41d9-9bf7-b4ac2fdefbd6
keywords:
- 鳶尾花 GL 移植，bbox2 函式
- 從鳶尾花 GL、bbox2 函式移植
- 從鳶尾花 GL、bbox2 函式移植至 OpenGL
- 從鳶尾花 GL、bbox2 函式移植的 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f34bc9035e9aa9fac884a14946a0593cb70702cf19f22d5d4c82011b58077e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012006"
---
# <a name="porting-the-bbox2-function"></a>移植 bbox2 函式

鳶尾花 GL **bbox2** 函數沒有任何 OpenGL 對等專案。

**若要移植包含 bbox2 函式的程式碼**

1.  建立新的 (OpenGL) 顯示清單，其中包含對等鳶尾花 GL 顯示清單中的所有專案，但呼叫 **bbox2** 除外。
2.  使用適當的 Windows 程式碼來繪製與鳶尾花 GL **bbox** 相同大小的矩形。

 

 




