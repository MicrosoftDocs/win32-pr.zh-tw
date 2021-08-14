---
title: CUSTOMSLIDER.positionImage
description: PositionImage 屬性會指定或抓取用來判斷影像檔案中所要顯示之位置影像的影像地圖。
ms.assetid: 7e99dc21-ebba-438a-a983-190dbe429578
keywords:
- CUSTOMSLIDER. positionImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.positionImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 727601ceb7ed078e40a284ab291f2e182a4270682b5f1db104515e31d3dbe2ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749987"
---
# <a name="customsliderpositionimage"></a>CUSTOMSLIDER.positionImage

**PositionImage** 屬性會指定或抓取用來判斷影像檔案中所要顯示之位置影像的影像地圖。

``` syntax
        elementID.positionImage
```

## <a name="possible-values"></a>可能的值

這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。

## <a name="remarks"></a>備註

這個屬性是必要的，而且必須指定。

不會顯示 **positionImage** 。 相反地，它會作為對應，以定義所顯示影像的可按區域。 顯示的影像是影像檔案的其中一個子影像，代表滑杆的實際狀態。 **PositionImage** 包含一些相當於這些子影像數目的灰色比例區域。 子映射必須與 **positionImage** 具有相同的維度，否則自訂滑杆將無法正常運作。

任何不是灰色縮放的區域都將無法按。 可點按的區域應設定為色彩值，這些值會從黑色到白色的灰色尺規範圍平均，而且第一個區域是純黑色，而最後一個區域是純白色。 每個後續區域的色彩值，應以等於255除以區域總數減一的值遞增，四捨五入為最接近的整數。

例如，如果有六個區域，則遞增量會是 51 (255 除以 5) ，而六個灰色小數位數值為0、51、102、153、204和255。 六個區域的十六進位色彩值接著會是 \# 000000、 \# 333333、 \# 666666、 \# 999999、 \# CCCCCC 和 \# FFFFFF。

如此一來，區域會有以灰色縮放色彩值為依據的序列，而此順序會對應至影像檔案中的子影像順序。 按一下其中一個區域時，會顯示對應的子影像，並據此更新自訂滑杆的 **值** 。

支援的影像檔案類型為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。

## <a name="examples"></a>範例

以下是自訂滑杆 **positionImage** 的範例。 對應的影像會顯示在 [ **影像** ] 屬性的 [範例] 區段中。

![範例 positionimage 圖形](images/dialmap.png)

下列程式碼說明如何使用 **CUSTOMSLIDER** 屬性。


```XML
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >

    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    >
      <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition;"
      />
    </PLAYER>

    <SLIDER
      id = "myslider"
      min = "0"
      max = "wmpprop:player.currentMedia.duration"
      onmouseup = "player.controls.currentPosition = myslider.value; "
      tooltip = "current position"
      height = "10"
      width = "180"
      top = "150"
      left = "88"
      backgroundColor = "red"
      foregroundColor = "blue"
      thumbImage = "thumb.bmp"
    />

    <CUSTOMSLIDER
      top = "120"
      left = "23"
      min = "0"
      max = "100"
      borderSize = "10"
      toolTip = "volume control"
      image = "dial.bmp"
      transparencyColor = "#00FFFF"
      positionImage = "dialmap.bmp"
      enabled = "true"
      value = "wmpprop:player.settings.volume"
      value_onchange = "player.settings.volume = value"
    />

    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "100"
    />

    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    > 

      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />

      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />

    </BUTTONGROUP>

  </VIEW>
</THEME>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CUSTOMSLIDER 元素**](customslider-element.md)
</dt> <dt>

[**CUSTOMSLIDER 影像**](customslider-image.md)
</dt> </dl>

 

 





