---
title: IAgentCommands GetCount
description: IAgentCommands GetCount
ms.assetid: 17140eda-17b0-49c2-8d50-5a38a553191a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ece3e007b644b370ee721cef2d273fa50d43ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104374961"
---
# <a name="iagentcommandsgetcount"></a>IAgentCommands：： GetCount

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of count of commands
);                    
```

抓取 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中的 [**命令**](/windows/desktop/lwef/the-command-object)物件數目。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

接收 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中 [**命令**](/windows/desktop/lwef/the-command-object)數目之變數的位址。

</dd> </dl>

*pdwCount* 僅包含您在 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中定義的 [**命令**](/windows/desktop/lwef/the-command-object)數目。 不包含伺服器或其他用戶端專案。

 

 