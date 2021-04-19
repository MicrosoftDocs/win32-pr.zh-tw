---
title: IAgentCommand GetVoice
description: IAgentCommand GetVoice
ms.assetid: 69f3c91b-2ccf-4bea-8034-0c3e0a5e4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2365019f71447e9d9c5a560c6506ee1dae7423df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106995564"
---
# <a name="iagentcommandgetvoice"></a><span data-ttu-id="ed842-103">IAgentCommand::GetVoice</span><span class="sxs-lookup"><span data-stu-id="ed842-103">IAgentCommand::GetVoice</span></span>

<span data-ttu-id="ed842-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="ed842-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Command
);
```

<span data-ttu-id="ed842-105">抓取 [**命令**](/windows/desktop/lwef/the-command-object)的 [**語音**](voice-property.md)文字屬性值。</span><span class="sxs-lookup"><span data-stu-id="ed842-105">Retrieves the value of the [**Voice**](voice-property.md) text property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="ed842-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="ed842-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ed842-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span><span class="sxs-lookup"><span data-stu-id="ed842-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="ed842-108">接收 [**命令**](/windows/desktop/lwef/the-command-object)之 [**語音**](voice-property.md)文字屬性之 BSTR 的位址。</span><span class="sxs-lookup"><span data-stu-id="ed842-108">The address of a BSTR that receives the [**Voice**](voice-property.md) text property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="ed842-109">將 [**語音**](voice-property.md)屬性集和其 [**Enabled**](enabled-property.md)屬性設定為 **True** 的 [**命令**](/windows/desktop/lwef/the-command-object)將可存取語音。</span><span class="sxs-lookup"><span data-stu-id="ed842-109">A [**Command**](/windows/desktop/lwef/the-command-object) with its [**Voice**](voice-property.md) property set and its [**Enabled**](enabled-property.md) property set to **True** will be voice-accessible.</span></span> <span data-ttu-id="ed842-110">如果也設定 [**標題**](caption-property.md) 屬性，它會出現在 [語音命令] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="ed842-110">If its [**Caption**](caption-property.md) property is also set it appears in the Voice Commands Window.</span></span> <span data-ttu-id="ed842-111">如果其 [**Visible**](visible-property.md) 屬性設定為 **True**，則會出現在字元的快顯功能表中。</span><span class="sxs-lookup"><span data-stu-id="ed842-111">If its [**Visible**](visible-property.md) property is set to **True**, it appears in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed842-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed842-112">See Also</span></span>

<span data-ttu-id="ed842-113">[**IAgentCommand：： SetVoice**](iagentcommand--setvoice.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="ed842-113">[**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 