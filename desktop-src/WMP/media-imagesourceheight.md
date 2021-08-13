---
title: ImageSourceHeight
description: ImageSourceHeight 屬性會抓取目前媒體專案的高度（以圖元為單位）。
ms.assetid: fa98ec62-4c58-46ab-98f3-8017096d46d8
keywords:
- ImageSourceHeight Windows Media Player
topic_type:
- apiref
api_name:
- Media.imageSourceHeight
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c399efa33d542de14c0753f5812298de83024c8856ea00a1e1fda002cd33c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390096"
---
# <a name="mediaimagesourceheight"></a>ImageSourceHeight

**ImageSourceHeight** 屬性會抓取目前媒體專案的高度（以圖元為單位）。

## <a name="syntax"></a>Syntax

*玩家*。*currentMedia*。**imageSourceHeight**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

如果媒體專案不是目前的，則這個屬性會傳回零。

若要取得這個屬性的值，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列 JScript 範例 *會使用 imageSourceHeight* 來顯示目前媒體專案的影像大小（以圖元為單位）。 這項資訊會列印到名為 VideoSize 的 HTML TEXTAREA 元素。 使用 ID = "player" 建立 **player** 物件。


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Store the height and width of the new media item.
   var Height = Player.currentMedia.imageSourceHeight;
   var Width =  Player.currentMedia.imageSourceWidth;

   // Erase the information in the text area.
   VideoSize.value = "";

   // Test whether an image is visible.
   if (Height != 0 && Width != 0)

      // Display the image size information.
      VideoSize.value = Width + " x " + Height;
}
</SCRIPT>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**CurrentMedia**](player-currentmedia.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





