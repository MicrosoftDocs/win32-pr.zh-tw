---
title: IAgentCommand GetVisible
description: IAgentCommand GetVisible
ms.assetid: cac07737-6a0b-4587-ae16-2137ce0d412c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1058c3855214dada0f1567f9fef81a3efc7e20a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375272"
---
# <a name="iagentcommandgetvisible"></a>IAgentCommand：： GetVisible

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Command
);
```

抓取 [**命令**](/windows/desktop/lwef/the-command-object)的 [**Visible**](visible-property.md)屬性值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

接收 [**命令**](/windows/desktop/lwef/the-command-object)之 [**Visible**](visible-property.md)屬性之變數的位址。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCommand：： SetVisible**](iagentcommand--setvisible.md)、 [**IAgentCommand：： SetCaption**](iagentcommand--setcaption.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)


 

 