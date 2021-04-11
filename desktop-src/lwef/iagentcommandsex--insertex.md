---
title: IAgentCommandsEx InsertEx
description: IAgentCommandsEx InsertEx
ms.assetid: 037c47df-f026-42dc-8c37-2704518d3fd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d59b504cfa475c3ac63888796d7df8d800bfd72
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023393"
---
# <a name="iagentcommandsexinsertex"></a><span data-ttu-id="1141c-103">IAgentCommandsEx::InsertEx</span><span class="sxs-lookup"><span data-stu-id="1141c-103">IAgentCommandsEx::InsertEx</span></span>

<span data-ttu-id="1141c-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="1141c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT InsertEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long dwRefID,          // reference Command for insertion
   long dBefore,          // insertion position flag
   long * pdwID           // address for variable for Command ID
);
```

<span data-ttu-id="1141c-105">在 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中插入 [**Command**](/windows/desktop/lwef/the-command-object)物件。</span><span class="sxs-lookup"><span data-stu-id="1141c-105">Inserts a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="1141c-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="1141c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1141c-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span><span class="sxs-lookup"><span data-stu-id="1141c-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="1141c-108">指定針對 [**命令**](/windows/desktop/lwef/the-command-object)顯示之 [**標題**](caption-property.md)文字值的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="1141c-108">A BSTR that specifies the value of the [**Caption**](caption-property.md) text displayed for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> <dt>

<span data-ttu-id="1141c-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span><span class="sxs-lookup"><span data-stu-id="1141c-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="1141c-110">指定 [**命令**](/windows/desktop/lwef/the-command-object)之 [**語音**](voice-property.md)文字設定值的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="1141c-110">A BSTR that specifies the value of the [**Voice**](voice-property.md) text setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> <dt>

<span data-ttu-id="1141c-111"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span><span class="sxs-lookup"><span data-stu-id="1141c-111"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="1141c-112">指定針對 [**命令集合中**](/windows/desktop/lwef/the-commands-collection-object)的 [**命令**](/windows/desktop/lwef/the-command-object)顯示之 [**VoiceCaption**](voicecaption-property.md)文字值的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="1141c-112">A BSTR that specifies the value of the [**VoiceCaption**](voicecaption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="1141c-113"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="1141c-113"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="1141c-114">指定 [**命令**](/windows/desktop/lwef/the-command-object)[**已啟用**](enabled-property.md)設定的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="1141c-114">A Boolean expression that specifies the [**Enabled**](enabled-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="1141c-115">如果參數為 **True**，則會啟用並選取 **命令** ;如果 **為 False**，則表示 **命令** 已停用。</span><span class="sxs-lookup"><span data-stu-id="1141c-115">If the parameter is **True**, the **Command** is enabled and can be selected; if **False**, the **Command** is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="1141c-116"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="1141c-116"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="1141c-117">指定 [**命令**](/windows/desktop/lwef/the-command-object)之 [**可見**](visible-property.md)設定的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="1141c-117">A Boolean expression that specifies the [**Visible**](visible-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="1141c-118">如果參數為 **True**，則在字元的快顯功能表中會顯示 **命令** (如果 [**Caption**](caption-property.md) 屬性也設定為) 。</span><span class="sxs-lookup"><span data-stu-id="1141c-118">If the parameter is **True**, the **Command** will be visible in the character's pop-up menu (if the [**Caption**](caption-property.md) property is also set).</span></span>

</dd> <dt>

<span data-ttu-id="1141c-119"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span><span class="sxs-lookup"><span data-stu-id="1141c-119"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="1141c-120">與 [**Command**](/windows/desktop/lwef/the-command-object) 物件相關聯的說明主題內容編號;用來為命令提供即時線上說明。</span><span class="sxs-lookup"><span data-stu-id="1141c-120">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> <dt>

<span data-ttu-id="1141c-121"><span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*</span><span class="sxs-lookup"><span data-stu-id="1141c-121"><span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*</span></span>
</dt> <dd>

<span data-ttu-id="1141c-122">用來作為新 **命令** 之相對插入參考的 [**命令**](/windows/desktop/lwef/the-command-object)識別碼。</span><span class="sxs-lookup"><span data-stu-id="1141c-122">The ID of a [**Command**](/windows/desktop/lwef/the-command-object) used as a reference for the relative insertion of the new **Command**.</span></span>

</dd> <dt>

<span data-ttu-id="1141c-123"><span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*</span><span class="sxs-lookup"><span data-stu-id="1141c-123"><span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*</span></span>
</dt> <dd>

<span data-ttu-id="1141c-124">指定要放置 [**命令**](/windows/desktop/lwef/the-command-object)之位置的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="1141c-124">A Boolean expression that specifies where to place the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="1141c-125">如果此參數為 **True**，則會在參考的 **命令** 之前插入新的 **命令**;如果 **為 False**，則新的 **命令** 會放在參考的 **命令** 之後。</span><span class="sxs-lookup"><span data-stu-id="1141c-125">If this parameter is **True**, the new **Command** is inserted before the referenced **Command**; if **False**, the new **Command** is placed after the referenced **Command**.</span></span>

</dd> <dt>

<span data-ttu-id="1141c-126"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span><span class="sxs-lookup"><span data-stu-id="1141c-126"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span></span> 
</dt> <dd>

<span data-ttu-id="1141c-127">接收所插入 [**命令**](/windows/desktop/lwef/the-command-object)之識別碼的變數位址。</span><span class="sxs-lookup"><span data-stu-id="1141c-127">Address of a variable that receives the ID for the inserted [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="1141c-128">[**IAgentCommandsEx：： InsertEx**](https://www.bing.com/search?q=**IAgentCommandsEx::InsertEx**)藉由包含 [[**上下文**](helpcontextid-property.md)屬性] 來擴充 [**IAgentCommands：： Insert**](iagentcommands--insert.md) 。</span><span class="sxs-lookup"><span data-stu-id="1141c-128">[**IAgentCommandsEx::InsertEx**](https://www.bing.com/search?q=**IAgentCommandsEx::InsertEx**) extends [**IAgentCommands::Insert**](iagentcommands--insert.md) by including the [**HelpContextID**](helpcontextid-property.md) property.</span></span> <span data-ttu-id="1141c-129">您也可以使用 [ **IAgentCommandsEx：： SetHelpCoNtextID** 來設定屬性。](iagentcommandsex--sethelpcontextid.md)</span><span class="sxs-lookup"><span data-stu-id="1141c-129">You can also set the property using [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="1141c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1141c-130">See Also</span></span>

<span data-ttu-id="1141c-131">[**IAgentCommandsEx：： AddEx**](iagentcommandsex--addex.md)、 [**IAgentCommandsEx：： SetHelpCoNtextID**](iagentcommandsex--sethelpcontextid.md)、 [**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Remove**](iagentcommands--remove.md)、 [**IAgentCommands：： RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="1141c-131">[**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 