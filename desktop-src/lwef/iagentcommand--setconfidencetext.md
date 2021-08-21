---
title: IAgentCommand SetConfidenceText
description: IAgentCommand SetConfidenceText
ms.assetid: e776a2ba-3592-4f26-a3e3-2c044eed7f0c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bae8889c8c8c52f392a368c38a91510e112adbeeca42c611cdc0adcadad94f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976338"
---
# <a name="iagentcommandsetconfidencetext"></a>IAgentCommand::SetConfidenceText

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetConfidenceText(
   BSTR bszTipText  // ConfidenceText setting for Command 
);
```

設定 [**命令**](/windows/desktop/lwef/the-command-object)之接聽提示文字的值。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*bszTipText*
</dt> <dd>

指定 [**命令**](/windows/desktop/lwef/the-command-object)之 [**ConfidenceText**](confidencetext-property.md)屬性文字的 BSTR。

</dd> </dl>

如果在 [**命令**](/windows/desktop/lwef/the-command-object) 事件中傳回之最符合專案的信賴價值不超過針對 [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) 屬性設定的值，則 *bszTipText* 中提供的文字會顯示在接聽提示中。

## <a name="see-also"></a>另請參閱

[**IAgentCommand：： SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md)、 [**IAgentCommand：： GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md)、 [**IAgentCommand：： GetConfidenceText**](iagentcommand--getconfidencetext.md)、 [**IAgentUserInput：： GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 