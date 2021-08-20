---
title: 影片。縮放
description: Zoom 屬性指定調整影片的百分比。
ms.assetid: 71c0e5a6-f7c4-46cf-a180-083d2926ba20
keywords:
- VIDEO. zoom Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.zoom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd49e9d2381fd0f86531a2d99fc9aa13a38e7f97699e5c048457dc983ad18af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117931381"
---
# <a name="videozoom"></a>影片。縮放

**Zoom** 屬性指定調整影片的百分比。

``` syntax
        elementID.zoom
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **號碼** (**長**) 範圍從1到可由影片控制項的寬度和高度容納的大小上限。 預設值為100。

## <a name="remarks"></a>備註

這個屬性不能與 **全螢幕** 屬性一起使用。

如果指定了 **寬度** 和 **高度** ，而所產生的影片視窗大於播放的影片，則可以藉由相應增加到視窗所容納的大小上限來放大影片。 如果未指定 **寬度** 和 **高度** ，則 **縮放** 範圍會限制為100或更小的值。

如果 **shrinkToFit** 屬性為 false，則影片會在縮放時變更比例，以符合可用空間。 如果 **shrinkToFit** 為 true，影片將會縮小以符合最嚴格的維度，同時保留其原始比例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**影片元素**](video-element.md)
</dt> <dt>

[**全螢幕影片**](video-fullscreen.md)
</dt> <dt>

[**ShrinkToFit**](video-shrinktofit.md)
</dt> </dl>

 

 





