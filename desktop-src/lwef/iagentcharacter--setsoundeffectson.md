---
title: IAgentCharacter SetSoundEffectsOn
description: IAgentCharacter SetSoundEffectsOn
ms.assetid: 141dd9a8-5fd8-42c6-880a-856c61cb8940
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71abb6adebf09182d4329202e77355e7dc365899291995e97eca66305a00ab94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725018"
---
# <a name="iagentcharactersetsoundeffectson"></a>IAgentCharacter::SetSoundEffectsOn

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT SetSoundEffectsOn(
   long bOn  // character sound effects setting 
);
```

決定是否播放字元的音效效果。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*邦*
</dt> <dd>

聲音效果設定。 如果此參數為 **True**，動畫播放時會播放動畫的音效效果;如果 **為 False**，則不播放音效效果。

</dd> </dl>

這項設定會決定當您播放相關聯的動畫時，是否播放編譯為字元一部分的音效效果。 這個屬性的設定會套用到字元的所有用戶端。 這項設定也會受限於使用者在 [**IAgentAudioOutputProperties：： GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)中的全域音效效果設定。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md)、 [ **IAgentAudioOutputProperties：： GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




