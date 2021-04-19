---
title: IAgentCharacter GetSoundEffectsOn
description: IAgentCharacter GetSoundEffectsOn
ms.assetid: 11bc074e-7654-4a78-920e-acd56db52c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a40f18a4fb8e7778c116c54391a7dc50e5267af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106988021"
---
# <a name="iagentcharactergetsoundeffectson"></a><span data-ttu-id="88928-103">IAgentCharacter::GetSoundEffectsOn</span><span class="sxs-lookup"><span data-stu-id="88928-103">IAgentCharacter::GetSoundEffectsOn</span></span>

<span data-ttu-id="88928-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="88928-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSoundEffectsOn(
   long * pbOn  // address of variable for sound effects setting 
);
```

<span data-ttu-id="88928-105">抓取是否啟用字元的音效效果設定。</span><span class="sxs-lookup"><span data-stu-id="88928-105">Retrieves whether the character's sound effects setting is enabled.</span></span>

-   <span data-ttu-id="88928-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="88928-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="88928-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span><span class="sxs-lookup"><span data-stu-id="88928-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span></span>
</dt> <dd>

<span data-ttu-id="88928-108">如果已啟用字元的音效效果設定，就會收到 **True** 的變數位址，如果停用，則 **為 False** 。</span><span class="sxs-lookup"><span data-stu-id="88928-108">Address of a variable that receives **True** if the character's sound effects setting is enabled, **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="88928-109">字元的音效效果設定會決定當您播放相關聯的動畫時，是否播放編譯為字元一部分的音效效果。</span><span class="sxs-lookup"><span data-stu-id="88928-109">The character's sound effects setting determines whether sound effects compiled as a part of the character are played when you play an associated animation.</span></span> <span data-ttu-id="88928-110">此設定受限於使用者在 [**IAgentAudioOutputProperties：： GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)中的全域音效效果設定。</span><span class="sxs-lookup"><span data-stu-id="88928-110">The setting is subject to the user's global sound effects setting in [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="88928-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88928-111">See Also</span></span>

<span data-ttu-id="88928-112">[**IAgentCharacter：： SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md)、 [ **IAgentAudioOutputProperties：： GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span><span class="sxs-lookup"><span data-stu-id="88928-112">[**IAgentCharacter::SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md), [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span></span>


 

 




