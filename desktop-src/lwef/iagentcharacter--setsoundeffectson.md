---
title: IAgentCharacter SetSoundEffectsOn
description: IAgentCharacter SetSoundEffectsOn
ms.assetid: 141dd9a8-5fd8-42c6-880a-856c61cb8940
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a454a6ebeecc763cb7e5a964bb1f2897df6c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965809"
---
# <a name="iagentcharactersetsoundeffectson"></a><span data-ttu-id="8b698-103">IAgentCharacter::SetSoundEffectsOn</span><span class="sxs-lookup"><span data-stu-id="8b698-103">IAgentCharacter::SetSoundEffectsOn</span></span>

<span data-ttu-id="8b698-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="8b698-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSoundEffectsOn(
   long bOn  // character sound effects setting 
);
```

<span data-ttu-id="8b698-105">決定是否播放字元的音效效果。</span><span class="sxs-lookup"><span data-stu-id="8b698-105">Determines whether the character's sound effects are played.</span></span>

-   <span data-ttu-id="8b698-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="8b698-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8b698-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*邦*</span><span class="sxs-lookup"><span data-stu-id="8b698-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*</span></span>
</dt> <dd>

<span data-ttu-id="8b698-108">聲音效果設定。</span><span class="sxs-lookup"><span data-stu-id="8b698-108">Sound effects setting.</span></span> <span data-ttu-id="8b698-109">如果此參數為 **True**，動畫播放時會播放動畫的音效效果;如果 **為 False**，則不播放音效效果。</span><span class="sxs-lookup"><span data-stu-id="8b698-109">If this parameter is **True**, the sound effects for animations are played when the animation plays; if **False**, sound effects are not played.</span></span>

</dd> </dl>

<span data-ttu-id="8b698-110">這項設定會決定當您播放相關聯的動畫時，是否播放編譯為字元一部分的音效效果。</span><span class="sxs-lookup"><span data-stu-id="8b698-110">This setting determines whether sound effects compiled as a part of the character are played when you play an associated animation.</span></span> <span data-ttu-id="8b698-111">這個屬性的設定會套用到字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="8b698-111">This property's setting applies to all clients of the character.</span></span> <span data-ttu-id="8b698-112">這項設定也會受限於使用者在 [**IAgentAudioOutputProperties：： GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)中的全域音效效果設定。</span><span class="sxs-lookup"><span data-stu-id="8b698-112">The setting is also subject to the user's global sound effects setting in [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8b698-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b698-113">See Also</span></span>

<span data-ttu-id="8b698-114">[**IAgentCharacter：： GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md)、 [ **IAgentAudioOutputProperties：： GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span><span class="sxs-lookup"><span data-stu-id="8b698-114">[**IAgentCharacter::GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span></span>


 

 




