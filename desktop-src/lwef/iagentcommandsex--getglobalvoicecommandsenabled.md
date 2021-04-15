---
title: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
ms.assetid: 9c8fa978-a02b-4dfc-8cf7-e066c5b75122
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7275bfe28190e06782cb2564dbf4868dd2c096
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375157"
---
# <a name="iagentcommandsexgetglobalvoicecommandsenabled"></a><span data-ttu-id="ff4fc-103">IAgentCommandsEx::GetGlobalVoiceCommandsEnabled</span><span class="sxs-lookup"><span data-stu-id="ff4fc-103">IAgentCommandsEx::GetGlobalVoiceCommandsEnabled</span></span>

<span data-ttu-id="ff4fc-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="ff4fc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetGlobalVoiceCommandsEnabled(
   long * pbEnabled  // address of the global voice command setting
);
```

<span data-ttu-id="ff4fc-105">抓取是否已啟用代理程式全域命令的語音文法。</span><span class="sxs-lookup"><span data-stu-id="ff4fc-105">Retrieves whether the voice grammar for Agent's global commands is enabled.</span></span>

-   <span data-ttu-id="ff4fc-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="ff4fc-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ff4fc-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="ff4fc-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="ff4fc-108">如果已啟用代理程式 global 命令的語音文法，則為收到 **True** 的位址，如果停用，則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="ff4fc-108">The address that receives **True** if the voice grammar for Agent's global commands is enabled, **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="ff4fc-109">Microsoft 代理程式會自動新增語音參數 (文法) 來開啟和關閉 [語音命令] 視窗，以及顯示和隱藏字元。</span><span class="sxs-lookup"><span data-stu-id="ff4fc-109">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="ff4fc-110">當此方法傳回 **False** 時，文法中不會包含這些命令的任何語音參數，以及其他用戶端 [**命令**](/windows/desktop/lwef/the-command-object)物件之 [**標題**](caption-property.md)的語音參數。</span><span class="sxs-lookup"><span data-stu-id="ff4fc-110">When this method returns **False**, any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other clients' [**Command**](/windows/desktop/lwef/the-command-object) objects are not included in the grammar.</span></span> <span data-ttu-id="ff4fc-111">這可讓您從用戶端目前的活動文法中排除這些。</span><span class="sxs-lookup"><span data-stu-id="ff4fc-111">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="ff4fc-112">不過，此設定不會反映在字元的快顯功能表中包含這些命令。</span><span class="sxs-lookup"><span data-stu-id="ff4fc-112">However, this setting does not reflect the inclusion of these commands in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff4fc-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff4fc-113">See Also</span></span>

[<span data-ttu-id="ff4fc-114">**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**</span><span class="sxs-lookup"><span data-stu-id="ff4fc-114">**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**</span></span>](iagentcommandsex--setglobalvoicecommandsenabled.md)


 

 