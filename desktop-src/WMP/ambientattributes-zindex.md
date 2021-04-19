---
title: AmbientAttributes. zIndex
description: ZIndex 屬性會指定或抓取控制項的呈現順序。
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- AmbientAttributes. zIndex Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52480cc387c0a9e5e45c4b8e8fd2dae4199dbd16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996439"
---
# <a name="ambientattributeszindex"></a>AmbientAttributes. zIndex

**ZIndex** 屬性會指定或抓取控制項的呈現順序。

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **號碼** (**長**) ，預設值為零。 範圍是帶正負號長整數的範圍。

## <a name="remarks"></a>備註

**視圖****或子視圖的** 背景點陣圖具有固定的 z 索引（零）。 如果您希望控制項位於背景後方， **zIndex** 必須設定為負數。

**視圖****或子視圖的** z 索引是絕對索引，而控制項的 z 索引是相對於包含它的視圖 **或子****視圖** 的 z 索引。

**瀏覽器** 和 **播放清單** 元素不支援 **zIndex** 屬性。 如果 *影片* 是 **影片** 專案，它將無法使用。[**無視窗**] 會設定為 false，而效果元素 **則會** 設定為 [**效果**]。**視窗** 設定為 true。

**BUTTONELEMENT** 元素會使用其 **BUTTONGROUP** 的 **zIndex** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> </dl>

 

 





