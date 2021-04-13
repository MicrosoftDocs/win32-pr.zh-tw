---
title: IAgentCommand GetConfidenceText
description: IAgentCommand GetConfidenceText
ms.assetid: d98339eb-0986-497c-b43c-4e4a952328e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987dca39016a20d185fbd4b8fd2b554c8bec02f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314659"
---
# <a name="iagentcommandgetconfidencetext"></a>IAgentCommand::GetConfidenceText

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetConfidenceText(
   BSTR * pbszTipText  // address of ConfidenceText setting for Command 
);
```

抓取先前針對 [**命令**](/windows/desktop/lwef/the-command-object)設定的接聽提示文字。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbszTipText"></span><span id="pbsztiptext"></span><span id="PBSZTIPTEXT"></span>*pbszTipText*
</dt> <dd>

接收 [**命令**](/windows/desktop/lwef/the-command-object)之接聽提示文字值的 BSTR 位址。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCommand：： SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md)、 [**IAgentCommand：： GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md)、 [**IAgentCommand：： SetConfidenceText**](iagentcommand--setconfidencetext.md)、 [**IAgentUserInput：： GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 