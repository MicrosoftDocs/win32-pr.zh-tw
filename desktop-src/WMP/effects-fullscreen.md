---
title: 效果。全螢幕
description: 全螢幕屬性會指定或抓取值，指出目前的視覺效果是否以全螢幕顯示。 這個屬性只能在執行時間設定。
ms.assetid: 319b46a4-b6c2-4dda-8285-f12af6836b25
keywords:
- 效果。全螢幕 Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c66ebb39c94135a28f90e4538116b663c2714d80413653ba945766e395d6af3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935270"
---
# <a name="effectsfullscreen"></a>效果。全螢幕

**全** 螢幕屬性會指定或抓取值，指出目前的視覺效果是否以全螢幕顯示。 這個屬性只能在執行時間設定。

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                                          |
|-------|------------------------------------------------------|
| true  | 視覺效果會以全螢幕顯示。              |
| false | 預設值。 視覺效果不會顯示全螢幕。 |



 

## <a name="remarks"></a>備註

只有當媒體現正播放或暫停時，視覺效果才能進入全螢幕模式。 如果 *播放機*。**currentMedia** 是影片，必須有影片外掛程式。 如果是音訊，則必須有支援全螢幕顯示的視覺化外掛程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**效果元素**](effects-element.md)
</dt> </dl>

 

 





