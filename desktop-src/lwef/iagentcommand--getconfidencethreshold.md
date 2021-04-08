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
# <a name="iagentcommandgetconfidencethreshold"></a><span data-ttu-id="d05ec-103">IAgentCommand::GetConfidenceThreshold</span><span class="sxs-lookup"><span data-stu-id="d05ec-103">IAgentCommand::GetConfidenceThreshold</span></span>

<span data-ttu-id="d05ec-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="d05ec-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetConfidenceThreshold(
long * plConfidenceThreshold  // address of ConfidenceThreshold 
);                            // setting for Command
```

<span data-ttu-id="d05ec-105">抓取 [**命令**](/windows/desktop/lwef/the-command-object)的 [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property)屬性值。</span><span class="sxs-lookup"><span data-stu-id="d05ec-105">Retrieves the value of the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="d05ec-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="d05ec-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d05ec-107"><span id="plConfidenceThreshold"></span><span id="plconfidencethreshold"></span><span id="PLCONFIDENCETHRESHOLD"></span>*plConfidenceThreshold*</span><span class="sxs-lookup"><span data-stu-id="d05ec-107"><span id="plConfidenceThreshold"></span><span id="plconfidencethreshold"></span><span id="PLCONFIDENCETHRESHOLD"></span>*plConfidenceThreshold*</span></span>
</dt> <dd>

<span data-ttu-id="d05ec-108">接收命令的 [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) 屬性值之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="d05ec-108">The address of a variable that receives the value of the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property for a Command.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="d05ec-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d05ec-109">See Also</span></span>

<span data-ttu-id="d05ec-110">[**IAgentCommand：： SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md)、 [**IAgentCommand：： SetConfidenceText**](iagentcommand--setconfidencetext.md)、 [**IAgentUserInput：： GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="d05ec-110">[**IAgentCommand::SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 