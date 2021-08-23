---
title: 滑杆. foregroundProgress
description: ForegroundProgress 屬性會指定或抓取前景進度列的目前位置（以滑杆區域的百分比表示）。
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- ForegroundProgress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e48819a2b3245fc8a72d29e9a30135cc37702417ca498c88b8be01578b74988
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646338"
---
# <a name="sliderforegroundprogress"></a>滑杆. foregroundProgress

**ForegroundProgress** 屬性會指定或抓取前景進度列的目前位置（以滑杆區域的百分比表示）。

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a>可能的值

這個屬性是 (**浮點數**) 範圍從0到100的讀取/寫入 **號碼**。

## <a name="remarks"></a>備註

這個屬性主要是用來追蹤媒體檔案的下載進度，同時使用 **value** 屬性來追蹤檔案目前的播放位置。 滑杆捲動方塊的位置會限制為前景進度的區域。 這可讓您只在下載檔案的可用部分內進行互動式搜尋。

若要使用此功能， **useForegroundProgress** 屬性必須設定為 true。

## <a name="examples"></a>範例


```C++
<SLIDER
  id="seek"
  backgroundColor="blue"
  foregroundColor="red"
  thumbImage="seekthumb.bmp"
  min="0"
  max="wmpprop:player.currentMedia.duration"
  value="wmpprop:player.controls.currentPosition"
  useForegroundProgress="true"
  foregroundProgress="wmpprop:player.network.downloadProgress"
  ondragend="player.controls.currentposition=value"
/>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**滑杆元素**](slider-element.md)
</dt> <dt>

[**滑杆。最小值**](slider-min.md)
</dt> <dt>

[**滑杆。最大值**](slider-max.md)
</dt> <dt>

[**滑杆. useForegroundProgress**](slider-useforegroundprogress.md)
</dt> <dt>

[**滑杆。值**](slider-value.md)
</dt> </dl>

 

 





