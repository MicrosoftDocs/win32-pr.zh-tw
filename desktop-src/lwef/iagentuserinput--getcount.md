---
title: IAgentUserInput GetCount
description: IAgentUserInput GetCount
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f52c296dd152fd1e31a87e21d80f8b25d52ae880b300487cdcba746e81dfa0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749515"
---
# <a name="iagentuserinputgetcount"></a>IAgentUserInput：： GetCount

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

抓取傳遞給 [**IAgentNotifySink：： command**](iagentnotifysink--command.md)回呼的 [**命令**](command-event.md)替代專案數目。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

接收伺服器所識別的 [**命令**](command-event.md) 替代專案計數之變數的位址。

</dd> </dl>

如果語音輸入不是命令的來源，例如，如果使用者從字元的快顯功能表中選取了命令， **GetCount** 會傳回1。 如果 **GetCount** 傳回零 (0) ，語音辨識引擎會偵測到說話輸入，但卻判斷沒有相符的命令。

 

 




