---
title: IAgentCommands GetVoice
description: IAgentCommands GetVoice
ms.assetid: ef8983bc-c70c-48c7-9c5f-1dae61028d90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b1915512c89611267df3788e5dcaa84fb0874a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375316"
---
# <a name="iagentcommandsgetvoice"></a><span data-ttu-id="81e9b-103">IAgentCommands::GetVoice</span><span class="sxs-lookup"><span data-stu-id="81e9b-103">IAgentCommands::GetVoice</span></span>

<span data-ttu-id="81e9b-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="81e9b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Commands collection
);
```

<span data-ttu-id="81e9b-105">抓取 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**Voice**](voice-property.md)屬性值。</span><span class="sxs-lookup"><span data-stu-id="81e9b-105">Retrieves the value of the [**Voice**](voice-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="81e9b-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="81e9b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="81e9b-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span><span class="sxs-lookup"><span data-stu-id="81e9b-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="81e9b-108">接收 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**語音**](voice-property.md)文字設定值之 BSTR 的位址。</span><span class="sxs-lookup"><span data-stu-id="81e9b-108">The address of a BSTR that receives the value of the [**Voice**](voice-property.md) text setting for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="81e9b-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81e9b-109">See Also</span></span>

<span data-ttu-id="81e9b-110">[**IAgentCommands：： SetVoice**](iagentcommands--setvoice.md)、 [**IAgentCommands：： GetCaption**](iagentcommands--getcaption.md)、 [**IAgentCommands：： GetVisible**](iagentcommands--getvisible.md)</span><span class="sxs-lookup"><span data-stu-id="81e9b-110">[**IAgentCommands::SetVoice**](iagentcommands--setvoice.md), [**IAgentCommands::GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands::GetVisible**](iagentcommands--getvisible.md)</span></span>


 

 