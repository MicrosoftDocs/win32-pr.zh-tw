---
title: IAgentCommands 新增
description: IAgentCommands 新增
ms.assetid: f6be7773-77fa-4c59-8feb-c2ebf54fd2e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee56854c302a096143e58fe6c21ef75fedfbf59
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092652"
---
# <a name="iagentcommandsadd"></a><span data-ttu-id="7156f-103">IAgentCommands：： Add</span><span class="sxs-lookup"><span data-stu-id="7156f-103">IAgentCommands::Add</span></span>

<span data-ttu-id="7156f-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="7156f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Add(
   BSTR bszCaption,  // Caption setting for Command
   BSTR bszVoice,    // Voice setting for Command
   long bEnabled,    // Enabled setting for Command
   long bVisible,    // Visible setting for Command
   long * pdwID      // address for variable for ID
);
```

<span data-ttu-id="7156f-105">將 [**命令**](/windows/desktop/lwef/the-command-object) 加入至 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合。</span><span class="sxs-lookup"><span data-stu-id="7156f-105">Adds a [**Command**](/windows/desktop/lwef/the-command-object) to a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="7156f-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="7156f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7156f-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span><span class="sxs-lookup"><span data-stu-id="7156f-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="7156f-108">指定針對 [**命令集合中**](/windows/desktop/lwef/the-commands-collection-object)的 [**命令**](/windows/desktop/lwef/the-command-object)顯示之 [**標題**](caption-property.md)文字值的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="7156f-108">A BSTR that specifies the value of the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="7156f-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span><span class="sxs-lookup"><span data-stu-id="7156f-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="7156f-110">指定 [**命令集合中**](/windows/desktop/lwef/the-commands-collection-object)[**命令**](/windows/desktop/lwef/the-command-object)之 [**語音**](voice-property.md)文字設定值的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="7156f-110">A BSTR that specifies the value of the [**Voice**](voice-property.md) text setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="7156f-111"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="7156f-111"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="7156f-112">布林運算式，指定 [**命令集合中**](/windows/desktop/lwef/the-commands-collection-object)[**命令**](/windows/desktop/lwef/the-command-object)的 [**啟用**](enabled-property.md)設定。</span><span class="sxs-lookup"><span data-stu-id="7156f-112">A Boolean expression that specifies the [**Enabled**](enabled-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="7156f-113">如果參數為 **True**，則會啟用並選取 **命令** ;如果 **為 False**，則表示 **命令** 已停用。</span><span class="sxs-lookup"><span data-stu-id="7156f-113">If the parameter is **True**, the **Command** is enabled and can be selected; if **False**, the **Command** is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="7156f-114"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="7156f-114"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="7156f-115">指定 [**命令集合中**](/windows/desktop/lwef/the-commands-collection-object)[**命令**](/windows/desktop/lwef/the-command-object)之 [**可見**](visible-property.md)設定的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="7156f-115">A Boolean expression that specifies the [**Visible**](visible-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="7156f-116">如果參數為 **True**，則在字元的快顯功能表中會顯示 **命令** (如果 [**Caption**](caption-property.md) 屬性也設定為) 。</span><span class="sxs-lookup"><span data-stu-id="7156f-116">If the parameter is **True**, the **Command** will be visible in the character's pop-up menu (if the [**Caption**](caption-property.md) property is also set).</span></span>

</dd> <dt>

<span data-ttu-id="7156f-117"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span><span class="sxs-lookup"><span data-stu-id="7156f-117"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span></span> 
</dt> <dd>

<span data-ttu-id="7156f-118">接收已新增 [**命令**](/windows/desktop/lwef/the-command-object)之識別碼的變數位址。</span><span class="sxs-lookup"><span data-stu-id="7156f-118">Address of a variable that receives the ID for the added [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="7156f-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7156f-119">See Also</span></span>

<span data-ttu-id="7156f-120">[**IAgentCommand：： SetCaption**](iagentcommand--setcaption.md)、 [**IAgentCommand：： SetEnabled**](iagentcommand--setenabled.md)、 [**IAgentCommand：： SetVisible**](iagentcommand--setvisible.md)、 [**IAgentCommand：： SetVoice**](iagentcommand--setvoice.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)、 [**IAgentCommands：： Remove**](iagentcommands--remove.md)、 [**IAgentCommands：： RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="7156f-120">[**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 