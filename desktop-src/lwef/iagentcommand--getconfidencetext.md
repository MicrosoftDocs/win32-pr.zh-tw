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
# <a name="iagentcommandgetconfidencetext"></a><span data-ttu-id="65a3a-103">IAgentCommand::GetConfidenceText</span><span class="sxs-lookup"><span data-stu-id="65a3a-103">IAgentCommand::GetConfidenceText</span></span>

<span data-ttu-id="65a3a-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="65a3a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetConfidenceText(
   BSTR * pbszTipText  // address of ConfidenceText setting for Command 
);
```

<span data-ttu-id="65a3a-105">抓取先前針對 [**命令**](/windows/desktop/lwef/the-command-object)設定的接聽提示文字。</span><span class="sxs-lookup"><span data-stu-id="65a3a-105">Retrieves the Listening Tip text previously set for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="65a3a-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="65a3a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="65a3a-107"><span id="pbszTipText"></span><span id="pbsztiptext"></span><span id="PBSZTIPTEXT"></span>*pbszTipText*</span><span class="sxs-lookup"><span data-stu-id="65a3a-107"><span id="pbszTipText"></span><span id="pbsztiptext"></span><span id="PBSZTIPTEXT"></span>*pbszTipText*</span></span>
</dt> <dd>

<span data-ttu-id="65a3a-108">接收 [**命令**](/windows/desktop/lwef/the-command-object)之接聽提示文字值的 BSTR 位址。</span><span class="sxs-lookup"><span data-stu-id="65a3a-108">The address of a BSTR that receives the value of the Listening Tip text for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="65a3a-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65a3a-109">See Also</span></span>

<span data-ttu-id="65a3a-110">[**IAgentCommand：： SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md)、 [**IAgentCommand：： GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md)、 [**IAgentCommand：： SetConfidenceText**](iagentcommand--setconfidencetext.md)、 [**IAgentUserInput：： GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="65a3a-110">[**IAgentCommand::SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 