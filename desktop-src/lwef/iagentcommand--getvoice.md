---
title: IAgentCommand GetVoice
description: IAgentCommand GetVoice
ms.assetid: 69f3c91b-2ccf-4bea-8034-0c3e0a5e4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120e27996f06a0446f7aaab944df8638134990fffe951400d94c690f52f78cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750425"
---
# <a name="iagentcommandgetvoice"></a>IAgentCommand::GetVoice

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Command
);
```

抓取 [**命令**](/windows/desktop/lwef/the-command-object)的 [**語音**](voice-property.md)文字屬性值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*
</dt> <dd>

接收 [**命令**](/windows/desktop/lwef/the-command-object)之 [**語音**](voice-property.md)文字屬性之 BSTR 的位址。

</dd> </dl>

將 [**語音**](voice-property.md)屬性集和其 [**Enabled**](enabled-property.md)屬性設定為 **True** 的 [**命令**](/windows/desktop/lwef/the-command-object)將可存取語音。 如果也設定 [**標題**](caption-property.md) 屬性，它會出現在 [語音命令] 視窗中。 如果其 [**Visible**](visible-property.md) 屬性設定為 **True**，則會出現在字元的快顯功能表中。

## <a name="see-also"></a>另請參閱

[**IAgentCommand：： SetVoice**](iagentcommand--setvoice.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)


 

 