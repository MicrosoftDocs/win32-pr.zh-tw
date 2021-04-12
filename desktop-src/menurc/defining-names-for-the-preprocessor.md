---
title: 定義預處理器的名稱
description: 您可以根據在 RC 命令列上使用/d 選項定義的名稱，或在檔案中指定條件式編譯，或使用 \ 定義指示詞，在檔案中指定條件式編譯。
ms.assetid: bc72911e-2aca-46a4-b6c1-60cc8ed7d82f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64b339959ace5a70d83fa8ee8beb615f1bc5ce4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300264"
---
# <a name="defining-names-for-the-preprocessor"></a>定義預處理器的名稱

您可以根據使用 **/d** 選項在 RC 命令列上定義的名稱，或在檔案中或包含 [**\# 定義**](-define.md)指示詞的 include 檔中，指定腳本中的條件式編譯。

例如，假設您的應用程式有一個快顯功能表，應該只出現在應用程式的偵錯工具版本。 當您編譯應用程式以供正常使用時，不會包含功能表。 下列範例顯示可新增至資源定義檔的語句，以定義偵錯工具功能表：

``` syntax
#include <windows.h>

MainMenu MENU
{
    //. . .
#ifdef DEBUG
    POPUP "&Debug"
    {
        MENUITEM "&Memory usage", ID_MEMORY
        MENUITEM "&Walk data heap", ID_WALK_HEAP
    }
#endif
}
```

當編譯應用程式的偵錯工具資源時，您可以使用下列命令來包含偵錯工具功能表：

**rc-d DEBUG myapp .rc**

要編譯應用程式一般版本的資源嗎？其中不包含 [Debug] 功能表？您可以使用下列命令：

**rc myapp .rc**

 

 




