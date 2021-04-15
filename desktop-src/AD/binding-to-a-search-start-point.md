---
title: 系結至搜尋起點
description: 搜尋的起點是直接或間接包含搜尋之物件的容器。
ms.assetid: f93c1310-7c8b-4d28-bd4d-6fab969d3353
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，系結至搜尋起點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 741986e651848c1d2a88ab016b63365db91b26b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104461969"
---
# <a name="binding-to-the-search-start-point"></a>系結至搜尋起點

搜尋的起點是直接或間接包含搜尋之物件的容器。 搜尋不會在搜尋起點上方的容器中執行。 例如，請採用下列假設目錄結構：

``` syntax
Domain A
    Container 1
        Object 1
        Object 2
    Container 2
        Object 3
        Object 4
```

如果對所有物件執行搜尋，且搜尋起點為 "Container 2"，則只會抓取 "Object 3" 和 "Object 4"。 如果使用搜尋起點在 "Container 1" 上執行相同的搜尋，則會抓取「物件1」和「物件2」。

若要系結至搜尋起點，請系結至將作為搜尋起點的容器的 ADsPath。

 

 




