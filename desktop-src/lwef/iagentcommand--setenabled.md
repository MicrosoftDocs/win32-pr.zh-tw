---
title: IAgentCommand SetEnabled
description: IAgentCommand SetEnabled
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da164b6603d93496e3381ccc6938a3b6d8f520bcea887cfd11f031cec7d845a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976308"
---
# <a name="iagentcommandsetenabled"></a>IAgentCommand::SetEnabled

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

設定 [**命令**](/windows/desktop/lwef/the-command-object)的 [**Enabled**](enabled-property.md)屬性。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

布林值，設定 [**命令**](/windows/desktop/lwef/the-command-object)[**啟用**](enabled-property.md)設定的值。 **True** 會啟用 **命令**; **False** 會停用它。 無法選取已停用的 **命令** 。

</dd> </dl>

[**命令**](/windows/desktop/lwef/the-command-object)的 [**Enabled**](enabled-property.md)屬性必須設定為 **True** ，才能供選擇。 它也必須設定 [**標題**](caption-property.md) 屬性，並將其 [ [**可見**](visible-property.md) ] 屬性設定為 [ **True** ]，才會出現在字元的快顯功能表中。 若要讓 **命令** 出現在 [ **語音命令] 視窗** 中，您必須設定其 [**語音**](voice-property.md)屬性。

## <a name="see-also"></a>另請參閱

[**IAgentCommand：： GetCaption**](iagentcommand--getcaption.md)、 [**IAgentCommand：： SetVoice**](iagentcommand--setvoice.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)


 

 