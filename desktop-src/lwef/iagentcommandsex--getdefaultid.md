---
title: IAgentCommandsEx GetDefaultID
description: IAgentCommandsEx GetDefaultID
ms.assetid: 14079ae0-ad2c-4f38-9371-9914f8402e49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4380eca62a65758979a94fb23511348b11acdf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375313"
---
# <a name="iagentcommandsexgetdefaultid"></a><span data-ttu-id="f3fa0-103">IAgentCommandsEx::GetDefaultID</span><span class="sxs-lookup"><span data-stu-id="f3fa0-103">IAgentCommandsEx::GetDefaultID</span></span>

<span data-ttu-id="f3fa0-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="f3fa0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetDefaultID(
   long * pdwID  // address of default command's ID
);
```

<span data-ttu-id="f3fa0-105">抓取 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合中預設命令的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3fa0-105">Retrieves the ID of the default command in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="f3fa0-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="f3fa0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f3fa0-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span><span class="sxs-lookup"><span data-stu-id="f3fa0-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span></span>
</dt> <dd>

<span data-ttu-id="f3fa0-108">接收 [**命令**](/windows/desktop/lwef/the-command-object) 集之識別碼作為預設值的變數位址。</span><span class="sxs-lookup"><span data-stu-id="f3fa0-108">Address of a variable that receives the ID of the [**Command**](/windows/desktop/lwef/the-command-object) set as the default.</span></span>

</dd> </dl>

<span data-ttu-id="f3fa0-109">這個屬性會傳回 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中目前的預設 [**命令**](/windows/desktop/lwef/the-command-object)物件。</span><span class="sxs-lookup"><span data-stu-id="f3fa0-109">This property returns the current default [**Command**](/windows/desktop/lwef/the-command-object) object in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="f3fa0-110">在字元的快顯功能表中，預設的命令為粗體。</span><span class="sxs-lookup"><span data-stu-id="f3fa0-110">The default command is bold in the character's pop-up menu.</span></span> <span data-ttu-id="f3fa0-111">不過，設定預設的命令不會變更命令處理或按兩下事件。</span><span class="sxs-lookup"><span data-stu-id="f3fa0-111">However, setting the default command does not change command handling or double-click events.</span></span>

<span data-ttu-id="f3fa0-112">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="f3fa0-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="f3fa0-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3fa0-113">See Also</span></span>

[<span data-ttu-id="f3fa0-114">**IAgentCommandsEx::SetDefaultID**</span><span class="sxs-lookup"><span data-stu-id="f3fa0-114">**IAgentCommandsEx::SetDefaultID**</span></span>](iagentcommandsex--setdefaultid.md)


 

 