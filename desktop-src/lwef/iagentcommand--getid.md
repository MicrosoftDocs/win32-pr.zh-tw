---
title: IAgentCommand GetID
description: IAgentCommand GetID
ms.assetid: 4d8d8be7-7003-4ef3-abba-b5232267c993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fbe051ab91a389c7a1a0d0ee6a445a9d2eb6107ea7f6a2755daa1a0bb0215f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477643"
---
# <a name="iagentcommandgetid"></a>IAgentCommand：： GetID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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


 

 