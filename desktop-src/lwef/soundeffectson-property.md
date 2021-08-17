---
title: SoundEffectsOn 屬性
description: SoundEffectsOn 屬性
ms.assetid: 478c4748-5ca1-4237-958a-17f0a476c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664a9f3ce4e76d7f42cc6fb15e737bea302730bb03ea414e968336ee147772cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975708"
---
# <a name="soundeffectson-property"></a>SoundEffectsOn 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定是否為您的字元啟用音效效果。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式*。**( "**_CharacterID_*_" ) 的字元。SoundEffectsOn_* \[  =  *布林值*\]



| 部分      | 描述                                                                                                                                                        |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | 指定是否啟用音效效果的布林運算式。 **True** 啟用音效效果。<br/> **False** 音效效果已停用。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

這個屬性會決定當動畫播放時，是否會播放包含在字元動畫中的音效效果。 這個屬性的設定會套用到字元的所有用戶端。

## <a name="see-also"></a>另請參閱

[**SoundEffects 屬性**](soundeffects-property.md)


 

 





