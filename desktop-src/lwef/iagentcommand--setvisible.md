---
title: IAgentCommand SetVisible
description: IAgentCommand SetVisible
ms.assetid: 58a383f4-6c98-4037-b469-ae68f06c852d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b583f79a93a5b13914486fb3e1a9cb513a682e63
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965017"
---
# <a name="iagentcommandsetvisible"></a>IAgentCommand::SetVisible

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Visible setting for Command
);
```

設定 [**命令**](/windows/desktop/lwef/the-command-object)的 [**Visible**](visible-property.md)屬性值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

布林值，決定 [**命令**](/windows/desktop/lwef/the-command-object)的 [**Visible**](visible-property.md)屬性。 **True** 會顯示 **命令**; **False** 會隱藏它。

</dd> </dl>

[**命令**](/windows/desktop/lwef/the-command-object)的 [**Visible**](visible-property.md)屬性必須設定為 **True** ，而且其 [**標題**](caption-property.md)屬性設定為顯示在字元的快顯功能表中。

## <a name="see-also"></a>另請參閱

[**IAgentCommand：： GetVisible**](iagentcommand--getvisible.md)、 [**IAgentCommand：： SetCaption**](iagentcommand--setcaption.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)


 

 