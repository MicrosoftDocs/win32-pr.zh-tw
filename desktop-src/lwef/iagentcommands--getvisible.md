---
title: IAgentCommands GetVisible
description: IAgentCommands GetVisible
ms.assetid: 229a02c8-f0a1-4ee5-9bae-961b63792038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853a47f6136779415a08adc3c891d9b5cc95dcca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106999795"
---
# <a name="iagentcommandsgetvisible"></a>IAgentCommands：： GetVisible

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Commands collection
);
```

抓取 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Visible**](visible-property.md)屬性值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

接收 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合之 [**Visible**](visible-property.md)屬性值的變數位址。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCommands：： SetVisible**](iagentcommands--setvisible.md)、 [ **IAgentCommands：： SetCaption**](iagentcommands--setcaption.md)


 

 