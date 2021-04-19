---
title: EQUALIZERSETTINGS.speakerSize
description: SpeakerSize 屬性會指定或抓取目前說話者大小的索引編號。
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- EQUALIZERSETTINGS. speakerSize Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26dc49af55e96d3ef8de4e8a4567b3a4296ca214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000780"
---
# <a name="equalizersettingsspeakersize"></a>EQUALIZERSETTINGS.speakerSize

**SpeakerSize** 屬性會指定或抓取目前說話者大小的索引編號。

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a>可能的值

這個屬性是包含下列其中一個值 (long) 的讀取/寫入 **號碼** 。



| 值 | 描述                              |
|-------|------------------------------------------|
| 0     | 目前的喇叭是耳機。     |
| 1     | 目前的喇叭是正常的大小。 |
| 2     | 目前的喇叭很大。          |



 

## <a name="remarks"></a>備註

您可以使用 **currentSpeakerName** 屬性來取出喇叭大小的易記名稱。

如果 **enhancedAudio** 設定為 false，則會忽略這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EQUALIZERSETTINGS 元素**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.currentSpeakerName**](equalizersettings-currentspeakername.md)
</dt> <dt>

[**EQUALIZERSETTINGS.enhancedAudio**](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





