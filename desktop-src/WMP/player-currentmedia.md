---
title: CurrentMedia
description: CurrentMedia 屬性會指定或抓取目前的媒體物件。
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- CurrentMedia Windows Media Player
topic_type:
- apiref
api_name:
- Player.currentMedia
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df5e8cd2032d772cbd781d0b45794e86cc19eff7c730a6a963778d54a6f283d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054396"
---
# <a name="playercurrentmedia"></a>CurrentMedia

**CurrentMedia** 屬性會指定或抓取目前的媒體物件。

## <a name="syntax"></a>Syntax

*玩家* 。**currentMedia**

## <a name="possible-values"></a>可能的值

此屬性是讀取/寫入媒體物件。

## <a name="remarks"></a>備註

如果 *設定*，則為。**autoStart** 屬性為 true，每當您設定 **currentMedia** 時，就會自動開始播放。

這個屬性會採用媒體物件，您可以使用 *播放清單* 來取得該物件。**專案**。 若要使用檔案名載入 **媒體** 專案，請設定 URL 屬性，或使用 **newMedia**。

## <a name="examples"></a>範例

下列 JScript 範例會抓取媒體櫃中的第一個媒體專案。 然後，它會使用 **currentMedia** 使取出的媒體專案成為目前的媒體專案，然後顯示目前媒體專案的名稱。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Retrieve the first media item from the library.
var firstMedia = Player.mediaCollection.getAll().item(0);

// Make the retrieved media item the current media item.
Player.currentMedia = firstMedia;

// Display the name of the current media item.
document.write("Found first media item. Name = " + Player.currentMedia.name);
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

[**Player 物件**](player-object.md)
</dt> <dt>

[**NewMedia**](player-newmedia.md)
</dt> <dt>

[**播放清單。專案**](playlist-item.md)
</dt> <dt>

[**設定 autoStart**](settings-autostart.md)
</dt> </dl>

 

 





