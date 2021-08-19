---
title: 播放清單。 attributeCount
description: AttributeCount 屬性會捕獲與播放清單相關聯的屬性數目。
ms.assetid: 92063131-0118-4458-9122-0539628a9821
keywords:
- 播放清單. attributeCount Windows Media Player
topic_type:
- apiref
api_name:
- Playlist.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63616096dbfc3989a93d3dc8010dd0ed1f256ccd9e9bf2cc7b3c825c88a63d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054296"
---
# <a name="playlistattributecount"></a>播放清單。 attributeCount

**AttributeCount** 屬性會捕獲與播放清單相關聯的屬性數目。

## <a name="syntax"></a>Syntax

*玩家*。*currentPlaylist*。**attributeCount**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

由於播放清單可以來自許多不同的來源，因此可以有數個不同的屬性集。 這個方法會抓取可用屬性的總數，讓 **播放清單** 物件的其他方法可以存取它們。

若要取得這個屬性的值，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player[屬性參考](attribute-reference.md)。

## <a name="examples"></a>範例

下列 JScript 範例說明如何使用 **播放清單** 和 **媒體** 物件的各種屬性和方法。


```JScript
function onLoad() {
    var display;
    var pl = player.currentPlaylist;

    pl.setItemInfo("custom playlist attribute", "changed");
    pl.item(0).setItemInfo("new custom attribute", "5");

    display = pl.attributeCount + " Playlist Attributes:\r\r";

    for (var i = 0; i < pl.attributeCount; ++i) {
        display = display + pl.attributeName(i) + ": ";
        display = display + pl.getItemInfo(pl.attributeName(i)) + "\r";
    }

    for (var j = 0; j < pl.count; ++j) {
        display = display + "\rTrack " + j + "\r"
        display = display + pl.item(j).attributeCount + " Attributes:\r\r";

        for (var k = 0; k < pl.item(j).attributeCount; ++k) {
            var it = pl.item(j);  // Media object
            display = display + it.getAttributeName(k) + ": ";
            display = display + it.getItemInfo(it.getAttributeName(k)) + "\r";
        }
    }

    myText.value = display;
}

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單物件**](playlist-object.md)
</dt> <dt>

[**播放清單。 attributeName**](playlist-attributename.md)
</dt> <dt>

[**播放清單。 getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**播放清單。 setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





