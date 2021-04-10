---
title: IAgentCommand SetConfidenceThreshold
description: IAgentCommand SetConfidenceThreshold
ms.assetid: f62d646a-895d-468c-9397-0495680109a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a6ba352f9385c57d0f3d1f01070f4b46e147d3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092719"
---
# <a name="iagentcommandsetconfidencethreshold"></a><span data-ttu-id="56f46-103">IAgentCommand::SetConfidenceThreshold</span><span class="sxs-lookup"><span data-stu-id="56f46-103">IAgentCommand::SetConfidenceThreshold</span></span>

<span data-ttu-id="56f46-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="56f46-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetConfidenceThreshold(
   long lConfidence  // Confidence setting for Command
);
```

<span data-ttu-id="56f46-105">設定 [**命令**](/windows/desktop/lwef/the-command-object)的 [**信賴**](confidence-property.md)屬性值。</span><span class="sxs-lookup"><span data-stu-id="56f46-105">Sets the value of the [**Confidence**](confidence-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="56f46-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="56f46-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="56f46-107"><span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lConfidence*</span><span class="sxs-lookup"><span data-stu-id="56f46-107"><span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lConfidence*</span></span>
</dt> <dd>

<span data-ttu-id="56f46-108">[**命令**](/windows/desktop/lwef/the-command-object)的 [**信賴**](confidence-property.md)屬性值。</span><span class="sxs-lookup"><span data-stu-id="56f46-108">The value for the [**Confidence**](confidence-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="56f46-109">如果在 [**命令**](/windows/desktop/lwef/the-command-object) 事件中傳回之最符合專案的信賴價值不超過針對 [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) 屬性設定的值，則 [**SetConfidenceText**](iagentcommand--setconfidencetext.md) 中提供的文字會顯示在接聽提示中。</span><span class="sxs-lookup"><span data-stu-id="56f46-109">If the confidence value returned of the best match returned in the [**Command**](/windows/desktop/lwef/the-command-object) event does not exceed the value set for the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property, the text supplied in [**SetConfidenceText**](iagentcommand--setconfidencetext.md) is displayed in the Listening Tip.</span></span>

## <a name="see-also"></a><span data-ttu-id="56f46-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56f46-110">See Also</span></span>

<span data-ttu-id="56f46-111">[**IAgentCommand：： GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md)、 [**IAgentCommand：： SetConfidenceText**](iagentcommand--setconfidencetext.md)、 [**IAgentUserInput：： GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="56f46-111">[**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 