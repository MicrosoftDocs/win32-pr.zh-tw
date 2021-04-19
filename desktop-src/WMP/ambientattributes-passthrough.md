---
title: AmbientAttributes
description: 傳遞屬性會指定或抓取值，指出控制項是否會將所有滑鼠事件傳遞至其下的控制項。
ms.assetid: 907ae233-3421-4e80-84be-64db4a3ab654
keywords:
- AmbientAttributes 傳遞 Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.passThrough
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b786aeefc182caab904c644dfd00ab4e76fec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987030"
---
# <a name="ambientattributespassthrough"></a>AmbientAttributes

**傳遞** 屬性會指定或抓取值，指出控制項是否會將所有滑鼠事件傳遞至其下的控制項。

``` syntax
        elementID.passThrough
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **布林值**。



| 值 | 描述                                            |
|-------|--------------------------------------------------------|
| true  | 控制權會將事件傳遞至其下的控制項。 |
| false | 預設值。 控制項不會透過傳遞事件。         |



 

## <a name="remarks"></a>備註

例如，如果文字控制項位於按鈕控制項上方，只提供標籤，這個屬性就很有用。 在此情況下，必須將文字控制項的按一下動作傳遞至按鈕控制項。

**VIEW**、子 **視圖** 和 **播放清單** 元素不支援 **傳遞** 屬性。 如果 *影片* 是 **影片** 專案，它將無法使用。[**無視窗**] 會設定為 false，而效果元素 *則會* 設定為 [**效果**]。**視窗** 設定為 true。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> </dl>

 

 





