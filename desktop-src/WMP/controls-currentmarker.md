---
title: CurrentMarker
description: CurrentMarker 屬性會指定或抓取目前的標記編號。
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- CurrentMarker Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentMarker
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aae8af226b62550b3faae9389385d321bf10aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995366"
---
# <a name="controlscurrentmarker"></a>CurrentMarker

**CurrentMarker** 屬性會指定或抓取目前的標記編號。

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入 **號碼** (**長**) ，預設值為零。

## <a name="remarks"></a>備註

設定 **currentMarker** 會導致播放從指定的標記開始。 在嘗試設定 **currentMarker** 之前，請先判斷檔案是否有標記以及使用 **markerCount** 有多少標記。 如果檔案沒有標記，請將 **currentMarker** 設定為任何值，但不會產生錯誤。 將 **currentMarker** 設定為大於 **markerCount** 的數位也會導致錯誤。

**CurrentMarker** 屬性一律會傳回目前的或最後一個標記，這表示實際的檔案位置可以是目前標記或下一個標記之前的位置。 標記從1開始編號，因此，如果檔案有標記，您可以將 **currentMarker** 設定為零，將檔案位置變更為零。

直到目前的媒體專案設定 (使用 *Player* 為止。**URL** 或 *播放機*。**currentMedia**) ， **currentMarker** 會傳回零。

## <a name="examples"></a>範例

下列 JScript 範例會使用 **currentMarker** ，從對應至 HTML SELECT 元素 **selectedIndex** 屬性的標記開始播放影片。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<SELECT ID = "markers"  NAME = "markers"  LANGUAGE = "JScript"

    /* Seek to the marker number that corresponds to the SELECT element
       selectedIndex value when the list selection changes. */
    onChange = "Player.controls.currentMarker = markers.selectedIndex + 1;
">

    /* Fill the SELECT element with the marker identifiers. */
    <OPTION SELECTED>Sunrise
    <OPTION>Car chase 
    <OPTION>Happy ending
</SELECT>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Controls 物件**](controls-object.md)
</dt> <dt>

[**MarkerCount**](media-markercount.md)
</dt> <dt>

[**CurrentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





