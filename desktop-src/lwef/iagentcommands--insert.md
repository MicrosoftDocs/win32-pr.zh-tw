---
title: IAgentCommands 插入
description: IAgentCommands 插入
ms.assetid: f450aae4-db6f-4326-ae14-ddb68ab0953a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f15df0c24e16a7554881cf3d0e6c41c4ee42b2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375121"
---
# <a name="iagentcommandsinsert"></a><span data-ttu-id="06266-103">IAgentCommands：： Insert</span><span class="sxs-lookup"><span data-stu-id="06266-103">IAgentCommands::Insert</span></span>

<span data-ttu-id="06266-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="06266-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Insert(
   BSTR bszCaption,  // Caption setting for Command
   BSTR bszVoice,    // Voice setting for Command
   long bEnabled,    // Enabled setting for Command
   long bVisible,    // Visible setting for Command
   long dwRefID,     // reference Command for insertion
   long dBefore,     // insertion position flag
   long * pdwID      // address for variable for Command ID
);
```

<span data-ttu-id="06266-105">在 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中插入 [**Command**](/windows/desktop/lwef/the-command-object)物件。</span><span class="sxs-lookup"><span data-stu-id="06266-105">Inserts a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="06266-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="06266-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="06266-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span><span class="sxs-lookup"><span data-stu-id="06266-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="06266-108">指定針對 [**命令**](/windows/desktop/lwef/the-command-object)顯示之 [**標題**](caption-property.md)文字值的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="06266-108">A BSTR that specifies the value of the [**Caption**](caption-property.md) text displayed for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> <dt>

<span data-ttu-id="06266-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span><span class="sxs-lookup"><span data-stu-id="06266-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="06266-110">指定 [**命令**](/windows/desktop/lwef/the-command-object)之 [**語音**](voice-property.md)文字設定值的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="06266-110">A BSTR that specifies the value of the [**Voice**](voice-property.md) text setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> <dt>

<span data-ttu-id="06266-111"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="06266-111"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="06266-112">指定 [**命令**](/windows/desktop/lwef/the-command-object)[**已啟用**](enabled-property.md)設定的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="06266-112">A Boolean expression that specifies the [**Enabled**](enabled-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="06266-113">如果參數為 **True**，則會啟用並選取 **命令** ;如果 **為 False**，則表示 **命令** 已停用。</span><span class="sxs-lookup"><span data-stu-id="06266-113">If the parameter is **True**, the **Command** is enabled and can be selected; if **False**, the **Command** is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="06266-114"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="06266-114"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="06266-115">指定 [**命令**](/windows/desktop/lwef/the-command-object)之 [**可見**](visible-property.md)設定的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="06266-115">A Boolean expression that specifies the [**Visible**](visible-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="06266-116">如果參數為 **True**，則在字元的快顯功能表中會顯示 **命令** (如果 [**Caption**](caption-property.md) 屬性也設定為) 。</span><span class="sxs-lookup"><span data-stu-id="06266-116">If the parameter is **True**, the **Command** will be visible in the character's pop-up menu (if the [**Caption**](caption-property.md) property is also set).</span></span>

</dd> <dt>

<span data-ttu-id="06266-117"><span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*</span><span class="sxs-lookup"><span data-stu-id="06266-117"><span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*</span></span>
</dt> <dd>

<span data-ttu-id="06266-118">用來作為新 **命令** 之相對插入參考的 [**命令**](/windows/desktop/lwef/the-command-object)識別碼。</span><span class="sxs-lookup"><span data-stu-id="06266-118">The ID of a [**Command**](/windows/desktop/lwef/the-command-object) used as a reference for the relative insertion of the new **Command**.</span></span>

</dd> <dt>

<span data-ttu-id="06266-119"><span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*</span><span class="sxs-lookup"><span data-stu-id="06266-119"><span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*</span></span>
</dt> <dd>

<span data-ttu-id="06266-120">指定要放置 [**命令**](/windows/desktop/lwef/the-command-object)之位置的布林運算式。</span><span class="sxs-lookup"><span data-stu-id="06266-120">A Boolean expression that specifies where to place the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="06266-121">如果此參數為 **True**，則會在參考的 **命令** 之前插入新的 **命令**;如果 **為 False**，則新的 **命令** 會放在參考的 **命令** 之後。</span><span class="sxs-lookup"><span data-stu-id="06266-121">If this parameter is **True**, the new **Command** is inserted before the referenced **Command**; if **False**, the new **Command** is placed after the referenced **Command**.</span></span>

</dd> <dt>

<span data-ttu-id="06266-122"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span><span class="sxs-lookup"><span data-stu-id="06266-122"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span></span> 
</dt> <dd>

<span data-ttu-id="06266-123">接收所插入 [**命令**](/windows/desktop/lwef/the-command-object)之識別碼的變數位址。</span><span class="sxs-lookup"><span data-stu-id="06266-123">Address of a variable that receives the ID for the inserted [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="06266-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06266-124">See Also</span></span>

<span data-ttu-id="06266-125">[**IAgentCommands：： Add**](iagentcommands--add.md)、 [**IAgentCommands：： Remove**](iagentcommands--remove.md)、 [**IAgentCommands：： RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="06266-125">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 