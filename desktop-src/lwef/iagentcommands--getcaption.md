---
title: IAgentCommands GetCaption
description: IAgentCommands GetCaption
ms.assetid: bbaaaa20-c8c2-41af-a6fc-cf8849daa399
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f886413ae6bfbfe104306d7280d8c66b08bf311a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106968489"
---
# <a name="iagentcommandsgetcaption"></a>IAgentCommands::GetCaption

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption text for Commands collection
);
```

抓取 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**標題**](caption-property.md)。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*
</dt> <dd>

BSTR 的位址，這個位址會接收針對 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合顯示之 [**標題**](caption-property.md)文字設定的值。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCommands：： SetCaption**](iagentcommands--setcaption.md)、 [**IAgentCommands：： GetVisible**](iagentcommands--getvisible.md)、 [**IAgentCommands：： GetVoice**](iagentcommands--getvoice.md)


 

 