---
title: IAgentCommand SetConfidenceText
description: IAgentCommand SetConfidenceText
ms.assetid: e776a2ba-3592-4f26-a3e3-2c044eed7f0c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cff1ae34c03f8ff67da61bea1834c25d6844ab2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104374992"
---
# <a name="iagentcommandsetconfidencetext"></a><span data-ttu-id="861c0-103">IAgentCommand::SetConfidenceText</span><span class="sxs-lookup"><span data-stu-id="861c0-103">IAgentCommand::SetConfidenceText</span></span>

<span data-ttu-id="861c0-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="861c0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetConfidenceText(
   BSTR bszTipText  // ConfidenceText setting for Command 
);
```

<span data-ttu-id="861c0-105">設定 [**命令**](/windows/desktop/lwef/the-command-object)之接聽提示文字的值。</span><span class="sxs-lookup"><span data-stu-id="861c0-105">Sets the value of the Listening Tip text for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="861c0-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="861c0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="861c0-107"><span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*bszTipText*</span><span class="sxs-lookup"><span data-stu-id="861c0-107"><span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*bszTipText*</span></span>
</dt> <dd>

<span data-ttu-id="861c0-108">指定 [**命令**](/windows/desktop/lwef/the-command-object)之 [**ConfidenceText**](confidencetext-property.md)屬性文字的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="861c0-108">A BSTR that specifies the text for the [**ConfidenceText**](confidencetext-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="861c0-109">如果在 [**命令**](/windows/desktop/lwef/the-command-object) 事件中傳回之最符合專案的信賴價值不超過針對 [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) 屬性設定的值，則 *bszTipText* 中提供的文字會顯示在接聽提示中。</span><span class="sxs-lookup"><span data-stu-id="861c0-109">If the confidence value returned of the best match returned in the [**Command**](/windows/desktop/lwef/the-command-object) event does not exceed the value set for the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property, the text supplied in *bszTipText* is displayed in the Listening Tip.</span></span>

## <a name="see-also"></a><span data-ttu-id="861c0-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="861c0-110">See Also</span></span>

<span data-ttu-id="861c0-111">[**IAgentCommand：： SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md)、 [**IAgentCommand：： GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md)、 [**IAgentCommand：： GetConfidenceText**](iagentcommand--getconfidencetext.md)、 [**IAgentUserInput：： GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="861c0-111">[**IAgentCommand::SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::GetConfidenceText**](iagentcommand--getconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 