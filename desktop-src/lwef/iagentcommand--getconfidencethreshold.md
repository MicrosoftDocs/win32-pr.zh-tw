---
title: IAgentCommand GetConfidenceThreshold
description: IAgentCommand GetConfidenceThreshold
ms.assetid: dfbaba7c-ed45-464e-82ab-39e33c023e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6557ad4e6831734106ee2c2e8021f923ef8806
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682019"
---
# <a name="iagentcommandgetconfidencethreshold"></a>IAgentCommand::GetConfidenceThreshold

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT GetConfidenceThreshold(
long * plConfidenceThreshold  // address of ConfidenceThreshold 
);                            // setting for Command
```

抓取 [**命令**](/windows/desktop/lwef/the-command-object)的 [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property)屬性值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plConfidenceThreshold"></span><span id="plconfidencethreshold"></span><span id="PLCONFIDENCETHRESHOLD"></span>*plConfidenceThreshold*
</dt> <dd>

接收命令的 [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) 屬性值之變數的位址。

</dd> </dl>

## <a name="see-also"></a>另請參閱

[**IAgentCommand：： SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md)、 [**IAgentCommand：： SetConfidenceText**](iagentcommand--setconfidencetext.md)、 [**IAgentUserInput：： GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 