---
title: SoundEffects 屬性
description: SoundEffects 屬性
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca45d373d39d479c62149a131f2a6678e5ecdf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106993712"
---
# <a name="soundeffects-property"></a>SoundEffects 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回布林值，指出是否 ( 音效效果。將會播放設定為字元動作一部分的 WAV) 檔案。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 * * *。AudioOutput.SoundEffects**



| 值     | 描述                          |
|-----------|--------------------------------------|
| **True**  | 已啟用字元音效效果。 |
| **False** | 字元音效效果已停用。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

這個屬性會在 [代理程式] 屬性工作表的 [輸出] 頁面上反映 [播放字元音效效果] 選項， ([Advanced Character Options]) 。 當 **SoundEffects** 屬性傳回 **True** 時，將會播放包含在字元定義中的音效效果。 若 **為 False**，將不會播放音效效果。 屬性設定會影響所有字元，而且是唯讀的;只有使用者可以設定此屬性值。

## <a name="see-also"></a>另請參閱

[**AgentPropertyChange 事件**](agentpropertychange-event.md)


 

 




