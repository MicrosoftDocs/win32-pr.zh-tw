---
title: 全螢幕影片
description: 全螢幕屬性會指定或抓取值，指出影片是否以全螢幕模式顯示。
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- VIDEO. 全螢幕 Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8150843ab14148d398b11cba82aa52711621c15962976ca37d5332a6ae58f24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465689"
---
# <a name="videofullscreen"></a>全螢幕影片

**全** 螢幕屬性會指定或抓取值，指出影片是否以全螢幕模式顯示。

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                                          |
|-------|------------------------------------------------------|
| true  | 影片會以全螢幕模式顯示。                  |
| false | 預設值。 影片不會以全螢幕模式顯示。 |



 

## <a name="remarks"></a>備註

在載入檔案之後，才可以在執行時間指定此屬性。 因此，它必須在腳本事件處理常式內設定。 [Escape] 按鈕可用來返回一般的觀賞。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**影片元素**](video-element.md)
</dt> <dt>

[**MaintainAspectRatio**](video-maintainaspectratio.md)
</dt> <dt>

[**ShrinkToFit**](video-shrinktofit.md)
</dt> <dt>

[**StretchToFit**](video-stretchtofit.md)
</dt> </dl>

 

 





