---
title: IAgentCommand GetEnabled
description: IAgentCommand GetEnabled
ms.assetid: b4ec25d2-b2e0-4b1b-8dc5-10fbb44149b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7118fa06fc895729755a36872a6d092d962d2416f81ac50e5c528cf9d69f5312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477653"
---
# <a name="iagentcommandgetenabled"></a>IAgentCommand：： GetEnabled

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of Enabled setting for Command
);
```

抓取 [**命令**](/windows/desktop/lwef/the-command-object)的 [**Enabled**](enabled-property.md)屬性值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

如果已啟用 [**命令**](/windows/desktop/lwef/the-command-object)，則為收到 **True** 之變數的位址，如果已停用，則為 **False** 。 無法選取已停用的 **命令** 。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCommand：： SetCaption**](iagentcommand--setcaption.md)、 [**IAgentCommand：： SetVisible**](iagentcommand--setvisible.md)、 [**IAgentCommand：： SetVoice**](iagentcommand--setvoice.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)


 

 