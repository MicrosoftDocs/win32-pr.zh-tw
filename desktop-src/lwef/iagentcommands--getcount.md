---
title: IAgentCommands GetCount
description: IAgentCommands GetCount
ms.assetid: 17140eda-17b0-49c2-8d50-5a38a553191a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 810f9fc268bc13558e4e51a3b64dd6f5b1d54caa5a055d9c90b6a8d11c48b3c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749822"
---
# <a name="iagentcommandsgetcount"></a>IAgentCommands：： GetCount

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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

 

 