---
title: AmbientAttributes. AlphaBlend
description: AlphaBlend 屬性會指定或抓取 Alpha 混合任何視圖、子視圖或 UI widget 的值。
ms.assetid: a6c47d32-a497-4bfa-8fa3-ef94e267d94b
keywords:
- AmbientAttributes. AlphaBlend Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlend
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b7170931c8fc266fdc335076dbc6dc687795f9bb432518b62a39d1f610b601
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391708"
---
# <a name="ambientattributesalphablend"></a>AmbientAttributes. AlphaBlend

**AlphaBlend** 屬性會指定或抓取 Alpha 混合任何 **視圖**、子 **視圖** 或 UI widget 的值。

``` syntax
        elementID.alphaBlend
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **號碼** (**long**) ，其值範圍從 0 (不透明度) 255 (完全不透明度) 和預設值255。

## <a name="remarks"></a>備註

這個屬性可讓元素根據不透明度設定的數量，以半透明的形式出現。 不透明度越少，就越透明地顯示元素。 面板中的每個專案都可以有不同的不透明度值，但 **BUTTONGROUP** 控制項中的按鈕元素除外。 當 [ **AlphaBlend** ] 設定為 [ **VIEW**] 時，將會設定整個外觀的不透明度。 如果 [**無視窗**] 設定為 [false]) ，Alpha blend 將無法用於視窗型控制項，包括 **播放清單**、**效果**、 **LISTBOX**、 **POPUP**、**編輯方塊** 和 **VIDEO** (。 當 [ **AlphaBlend** ] 設定為 [ **VIEW**] 時，整個外觀就會變成透明。 **AlphaBlend** 不支援數個元素所使用的 **transparencyColor** 屬性。

當您使用 **AlphaBlend** 搭配未指定 **backgroundColor** 的 **TEXT** 元素時，將會使用黑色的背景色彩。 如果前景色彩也是黑色 (這是 *文字* 的預設值。**foregroundColor**) ，您的文字可能會變成無法讀取。 若要避免這種情況，請一律指定 **backgroundColor** 屬性，或將 **foregroundColor** 設定為黑色以外的色彩。

> [!Note]  
> Windows 98 不支援這個屬性。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**環境屬性**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.AlphaBlendTo**](ambientattributes-alphablendto.md)
</dt> <dt>

[**TEXT 元素**](text-element.md)
</dt> <dt>

[**BackgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**ForegroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





