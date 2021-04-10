---
title: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
ms.assetid: f456b1d3-60aa-4b90-90d0-6c695947fa8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87a576a36d3df4b3ddf0ca71f5709a712a3c9e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092692"
---
# <a name="iagentcommandsexsetglobalvoicecommandsenabled"></a><span data-ttu-id="2384b-103">IAgentCommandsEx::SetGlobalVoiceCommandsEnabled</span><span class="sxs-lookup"><span data-stu-id="2384b-103">IAgentCommandsEx::SetGlobalVoiceCommandsEnabled</span></span>

<span data-ttu-id="2384b-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="2384b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetGlobalVoiceCommandsEnabled(
 long bEnable  // Enabled setting for Agent's global voice commands
);
```

<span data-ttu-id="2384b-105">為 Microsoft 代理程式的全域命令的語音文法設定 [**Enabled**](enabled-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="2384b-105">Sets the [**Enabled**](enabled-property.md) property for the voice grammar of Microsoft Agent's global commands.</span></span>

-   <span data-ttu-id="2384b-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="2384b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2384b-107"><span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*</span><span class="sxs-lookup"><span data-stu-id="2384b-107"><span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*</span></span>
</dt> <dd>

<span data-ttu-id="2384b-108">布林值，設定是否啟用代理程式全域命令的語音文法。</span><span class="sxs-lookup"><span data-stu-id="2384b-108">A Boolean value that sets whether the voice grammar of Agent's global commands is enabled.</span></span> <span data-ttu-id="2384b-109">**True** 可啟用語音文法; **False** 會停用它。</span><span class="sxs-lookup"><span data-stu-id="2384b-109">**True** enables the voice grammar; **False** disables it.</span></span>

</dd> </dl>

<span data-ttu-id="2384b-110">Microsoft 代理程式會自動新增語音參數 (文法) 來開啟和關閉 [語音命令] 視窗，以及顯示和隱藏字元。</span><span class="sxs-lookup"><span data-stu-id="2384b-110">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="2384b-111">當設定為 **False** 時，Agent 會停用這些命令的任何語音參數，以及其他用戶端 [**命令**](/windows/desktop/lwef/the-command-object)物件之 [**標題**](caption-property.md)的語音參數。</span><span class="sxs-lookup"><span data-stu-id="2384b-111">When set to **False**, Agent disables any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other client's [**Command**](/windows/desktop/lwef/the-command-object) objects.</span></span> <span data-ttu-id="2384b-112">這可讓您從用戶端目前的活動文法中排除這些。</span><span class="sxs-lookup"><span data-stu-id="2384b-112">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="2384b-113">不過，因為這可能會封鎖其他用戶端的語音存取，所以在處理使用者的語音輸入之後，請將此屬性重設為 **True** 。</span><span class="sxs-lookup"><span data-stu-id="2384b-113">However, because this potentially blocks voice access to other clients, reset this property to **True** after processing the user's voice input.</span></span>

<span data-ttu-id="2384b-114">停用此屬性並不會影響該字元的快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="2384b-114">Disabling the property does not affect the character's pop-up menu.</span></span> <span data-ttu-id="2384b-115">伺服器所加入的全域命令仍會出現。</span><span class="sxs-lookup"><span data-stu-id="2384b-115">The global commands added by the server will still appear.</span></span> <span data-ttu-id="2384b-116">您無法從快顯功能表中移除它們。</span><span class="sxs-lookup"><span data-stu-id="2384b-116">You cannot remove them from the pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="2384b-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2384b-117">See Also</span></span>

[<span data-ttu-id="2384b-118">**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**</span><span class="sxs-lookup"><span data-stu-id="2384b-118">**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**</span></span>](iagentcommandsex--getglobalvoicecommandsenabled.md)


 

 