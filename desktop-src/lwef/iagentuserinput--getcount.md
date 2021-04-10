---
title: IAgentUserInput GetCount
description: IAgentUserInput GetCount
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac4b597f7367eff10154bde256698ef371c3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182932"
---
# <a name="iagentuserinputgetcount"></a>IAgentUserInput：： GetCount

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

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

 

 




