---
title: IAgentCharacter GetTTSSpeed
description: IAgentCharacter GetTTSSpeed
ms.assetid: 25526ef7-581f-489c-a299-bd3b5ac9ea61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 551074e1647cffc88e0b5f9f530cea931cd21ff9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372691"
---
# <a name="iagentcharactergetttsspeed"></a><span data-ttu-id="e4b18-103">IAgentCharacter::GetTTSSpeed</span><span class="sxs-lookup"><span data-stu-id="e4b18-103">IAgentCharacter::GetTTSSpeed</span></span>

<span data-ttu-id="e4b18-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="e4b18-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

<span data-ttu-id="e4b18-105">抓取字元的 TTS 輸出速度設定。</span><span class="sxs-lookup"><span data-stu-id="e4b18-105">Retrieves the character's TTS output speed setting.</span></span>

-   <span data-ttu-id="e4b18-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="e4b18-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e4b18-107"><span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*</span><span class="sxs-lookup"><span data-stu-id="e4b18-107"><span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="e4b18-108">每分鐘接收字元輸出速度的變數位址（以單字為單位）。</span><span class="sxs-lookup"><span data-stu-id="e4b18-108">Address of a variable that receives the output speed of the character in words per minute.</span></span>

</dd> </dl>

<span data-ttu-id="e4b18-109">雖然您的應用程式無法寫入此值，但您可以將速度標記包含在輸出文字中，以暫時加速特定語句的輸出。</span><span class="sxs-lookup"><span data-stu-id="e4b18-109">Although your application cannot write this value, you can include speed tags in your output text that will temporarily speed up the output for a particular utterance.</span></span>

<span data-ttu-id="e4b18-110">這個屬性會傳回字元的目前說話輸出速度設定。</span><span class="sxs-lookup"><span data-stu-id="e4b18-110">This property returns the current speaking output speed setting for the character.</span></span> <span data-ttu-id="e4b18-111">針對使用 TTS 輸出的字元，屬性會傳回字元的實際 TTS 輸出。</span><span class="sxs-lookup"><span data-stu-id="e4b18-111">For characters using TTS output, the property returns the actual TTS output for the character.</span></span> <span data-ttu-id="e4b18-112">如果未啟用 TTS 或字元不支援 TTS 輸出，此設定會反映輸出速度的使用者設定。</span><span class="sxs-lookup"><span data-stu-id="e4b18-112">If TTS is not enabled or the character does not support TTS output, the setting reflects the user setting for output speed.</span></span>

 

 




