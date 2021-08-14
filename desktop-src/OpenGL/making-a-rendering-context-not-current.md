---
title: 使轉譯內容不是最新的
description: 若要從執行緒卸離轉譯內容，請使它不是最新的。 您可以藉由呼叫 wglMakeCurrent 函式，並將參數設定為 Null 來完成這項作業。 以下是這項簡單工作的範例。
ms.assetid: fe76e3d3-5480-448d-95aa-a5af0da309f3
keywords:
- Windows 上的 OpenGL，轉譯內容
- 轉譯內容 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914bbed6e2d595d23cfcf8dc38820efc18153f4433a2a48446090ec16818b671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937361"
---
# <a name="making-a-rendering-context-not-current"></a>使轉譯內容不是最新的

若要從執行緒卸離轉譯內容，請使它不是最新的。 您可以藉由呼叫 [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) 函式，並將參數設定為 **Null** 來完成這項作業。 以下是這項簡單工作的範例。

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




