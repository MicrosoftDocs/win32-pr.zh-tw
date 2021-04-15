---
title: IAgentCommand GetID
description: IAgentCommand GetID
ms.assetid: 4d8d8be7-7003-4ef3-abba-b5232267c993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1f5887123df19496c0610c53fe59a3f64961cd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104374996"
---
# <a name="iagentcommandgetid"></a>IAgentCommand：： GetID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetID(
   long * pdwID  // address of ID for Command
);
```

抓取 [**命令**](/windows/desktop/lwef/the-command-object)的識別碼。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*
</dt> <dd>

接收 [**命令**](/windows/desktop/lwef/the-command-object)識別碼之變數的位址。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)、 [**IAgentCommands：： Remove**](iagentcommands--remove.md)


 

 