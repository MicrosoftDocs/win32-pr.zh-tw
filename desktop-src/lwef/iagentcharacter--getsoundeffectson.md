---
title: IAgentCharacter GetSoundEffectsOn
description: IAgentCharacter GetSoundEffectsOn
ms.assetid: 11bc074e-7654-4a78-920e-acd56db52c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f7133e41e4c291200feaf8fdb8ab3919cdb622ca927c155fc0941202fd555a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848638"
---
# <a name="iagentcharactergetsoundeffectson"></a>IAgentCharacter::GetSoundEffectsOn

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetSoundEffectsOn(
   long * pbOn  // address of variable for sound effects setting 
);
```

抓取是否啟用字元的音效效果設定。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*
</dt> <dd>

如果已啟用字元的音效效果設定，就會收到 **True** 的變數位址，如果停用，則 **為 False** 。

</dd> </dl>

字元的音效效果設定會決定當您播放相關聯的動畫時，是否播放編譯為字元一部分的音效效果。 此設定受限於使用者在 [**IAgentAudioOutputProperties：： GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)中的全域音效效果設定。

## <a name="see-also"></a>另請參閱

[**IAgentCharacter：： SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md)、 [ **IAgentAudioOutputProperties：： GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




