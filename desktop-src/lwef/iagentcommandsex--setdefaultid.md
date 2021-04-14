---
title: IAgentCommandsEx SetDefaultID
description: IAgentCommandsEx SetDefaultID
ms.assetid: 056ec518-bf0b-403f-adc6-9b53b0c044a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37754eb61df7879511a03dde705936d36f905376
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375120"
---
# <a name="iagentcommandsexsetdefaultid"></a><span data-ttu-id="193b0-103">IAgentCommandsEx::SetDefaultID</span><span class="sxs-lookup"><span data-stu-id="193b0-103">IAgentCommandsEx::SetDefaultID</span></span>

<span data-ttu-id="193b0-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="193b0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetDefaultID(
   long dwID,  // default command's ID
);
```

<span data-ttu-id="193b0-105">設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合中預設命令的識別碼。</span><span class="sxs-lookup"><span data-stu-id="193b0-105">Sets the ID of the default command in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="193b0-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="193b0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="193b0-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span><span class="sxs-lookup"><span data-stu-id="193b0-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span></span>
</dt> <dd>

<span data-ttu-id="193b0-108">要設定為預設值之 [**命令**](/windows/desktop/lwef/the-command-object) 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="193b0-108">The ID for the [**Command**](/windows/desktop/lwef/the-command-object) to be set as the default.</span></span>

</dd> </dl>

<span data-ttu-id="193b0-109">這個屬性會設定 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中的預設 [**命令**](/windows/desktop/lwef/the-command-object)物件集。</span><span class="sxs-lookup"><span data-stu-id="193b0-109">This property sets the default [**Command**](/windows/desktop/lwef/the-command-object) object set in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="193b0-110">在字元的快顯功能表中，預設的命令為粗體。</span><span class="sxs-lookup"><span data-stu-id="193b0-110">The default command is bold in the character's pop-up menu.</span></span> <span data-ttu-id="193b0-111">不過，設定預設的命令不會實際變更命令處理或按兩下事件。</span><span class="sxs-lookup"><span data-stu-id="193b0-111">However, setting the default command does not actually change command handling or double-click events.</span></span>

<span data-ttu-id="193b0-112">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="193b0-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="193b0-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="193b0-113">See Also</span></span>

[<span data-ttu-id="193b0-114">**IAgentCommandsEx::GetDefaultID**</span><span class="sxs-lookup"><span data-stu-id="193b0-114">**IAgentCommandsEx::GetDefaultID**</span></span>](iagentcommandsex--getdefaultid.md)


 

 