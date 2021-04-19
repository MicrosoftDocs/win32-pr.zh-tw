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
# <a name="iagentcharactersetsoundeffectson"></a>IAgentCharacter::SetSoundEffectsOn

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

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


 

 




