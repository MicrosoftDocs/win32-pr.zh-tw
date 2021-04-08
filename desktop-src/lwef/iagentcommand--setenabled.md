---
title: IAgentCommand SetEnabled
description: IAgentCommand SetEnabled
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8377307d66257f7a9b74ac82512edc6e4ec64034
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023350"
---
# <a name="iagentcommandsetenabled"></a><span data-ttu-id="bcb89-103">IAgentCommand::SetEnabled</span><span class="sxs-lookup"><span data-stu-id="bcb89-103">IAgentCommand::SetEnabled</span></span>

<span data-ttu-id="bcb89-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="bcb89-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

<span data-ttu-id="bcb89-105">設定 [**命令**](/windows/desktop/lwef/the-command-object)的 [**Enabled**](enabled-property.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="bcb89-105">Sets the [**Enabled**](enabled-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="bcb89-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="bcb89-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bcb89-107"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="bcb89-107"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="bcb89-108">布林值，設定 [**命令**](/windows/desktop/lwef/the-command-object)[**啟用**](enabled-property.md)設定的值。</span><span class="sxs-lookup"><span data-stu-id="bcb89-108">A Boolean value that sets the value of the [**Enabled**](enabled-property.md) setting of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="bcb89-109">**True** 會啟用 **命令**; **False** 會停用它。</span><span class="sxs-lookup"><span data-stu-id="bcb89-109">**True** enables the **Command**; **False** disables it.</span></span> <span data-ttu-id="bcb89-110">無法選取已停用的 **命令** 。</span><span class="sxs-lookup"><span data-stu-id="bcb89-110">A disabled **Command** cannot be selected.</span></span>

</dd> </dl>

<span data-ttu-id="bcb89-111">[**命令**](/windows/desktop/lwef/the-command-object)的 [**Enabled**](enabled-property.md)屬性必須設定為 **True** ，才能供選擇。</span><span class="sxs-lookup"><span data-stu-id="bcb89-111">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Enabled**](enabled-property.md) property set to **True** to be selectable.</span></span> <span data-ttu-id="bcb89-112">它也必須設定 [**標題**](caption-property.md) 屬性，並將其 [ [**可見**](visible-property.md) ] 屬性設定為 [ **True** ]，才會出現在字元的快顯功能表中。</span><span class="sxs-lookup"><span data-stu-id="bcb89-112">It also must have its [**Caption**](caption-property.md) property set and its [**Visible**](visible-property.md) property set to **True** to appear in the character's pop-up menu.</span></span> <span data-ttu-id="bcb89-113">若要讓 **命令** 出現在 [ **語音命令] 視窗** 中，您必須設定其 [**語音**](voice-property.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="bcb89-113">To make the **Command** appear in the **Voice Commands Window**, you must set its [**Voice**](voice-property.md)property.</span></span>

## <a name="see-also"></a><span data-ttu-id="bcb89-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bcb89-114">See Also</span></span>

<span data-ttu-id="bcb89-115">[**IAgentCommand：： GetCaption**](iagentcommand--getcaption.md)、 [**IAgentCommand：： SetVoice**](iagentcommand--setvoice.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="bcb89-115">[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 