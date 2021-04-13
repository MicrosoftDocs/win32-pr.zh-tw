---
title: IAgentCharacter SetIdleOn
description: IAgentCharacter SetIdleOn
ms.assetid: 397d223a-0970-4535-ad46-2923df6b9975
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98db30c9c440ed0564b98977d33e15e390cf57d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372686"
---
# <a name="iagentcharactersetidleon"></a><span data-ttu-id="4032c-103">IAgentCharacter::SetIdleOn</span><span class="sxs-lookup"><span data-stu-id="4032c-103">IAgentCharacter::SetIdleOn</span></span>

<span data-ttu-id="4032c-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="4032c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetIdleOn(
   long bOn  // idle processing flag
);
```

<span data-ttu-id="4032c-105">為字元設定自動閒置處理。</span><span class="sxs-lookup"><span data-stu-id="4032c-105">Sets automatic idle processing for a character.</span></span>

-   <span data-ttu-id="4032c-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="4032c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4032c-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*邦*</span><span class="sxs-lookup"><span data-stu-id="4032c-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*</span></span>
</dt> <dd>

<span data-ttu-id="4032c-108">閒置處理旗標。</span><span class="sxs-lookup"><span data-stu-id="4032c-108">Idle processing flag.</span></span> <span data-ttu-id="4032c-109">如果此參數為 **True**，Microsoft 代理程式會自動播放 **閒置** 狀態動畫。</span><span class="sxs-lookup"><span data-stu-id="4032c-109">If this parameter is **True**, the Microsoft Agent automatically plays **Idling** state animations.</span></span>

</dd> </dl>

<span data-ttu-id="4032c-110">伺服器會自動設定最後一個動畫播放某個字元之後的時間。</span><span class="sxs-lookup"><span data-stu-id="4032c-110">The server automatically sets a time out after the last animation played for a character.</span></span> <span data-ttu-id="4032c-111">當此計時器的間隔完成時，伺服器會開始 **閒置** 狀態的字元，並定期播放其相關聯的 **閒置** 動畫。</span><span class="sxs-lookup"><span data-stu-id="4032c-111">When this timer's interval is complete, the server begins the **Idling** states for a character, playing its associated **Idling** animations at regular intervals.</span></span> <span data-ttu-id="4032c-112">如果您想要自行管理 **閒置** 狀態動畫，請將屬性設定為 **False**。</span><span class="sxs-lookup"><span data-stu-id="4032c-112">If you want to manage the **Idling** state animations yourself, set the property to **False**.</span></span> <span data-ttu-id="4032c-113">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="4032c-113">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="4032c-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4032c-114">See Also</span></span>

[<span data-ttu-id="4032c-115">**IAgentCharacter::GetIdleOn**</span><span class="sxs-lookup"><span data-stu-id="4032c-115">**IAgentCharacter::GetIdleOn**</span></span>](iagentcharacter--getidleon.md)


 

 




