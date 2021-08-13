---
title: SourceURL
description: SourceURL 屬性會抓取媒體專案的 URL。
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- SourceURL Windows Media Player
topic_type:
- apiref
api_name:
- Media.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e2f99aeb64a73bcf36e2cbd472aedfa8f509a5073e70792e7b47343a1b37d60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415948"
---
# <a name="mediasourceurl"></a>SourceURL

**SourceURL** 屬性會抓取媒體專案的 URL。

## <a name="syntax"></a>Syntax

*玩家*。*currentMedia*. sourceURL

## <a name="possible-values"></a>可能的值

這個屬性是唯讀 **字串**。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *媒體*。**sourceURL** 以取得範例播放清單中第一個媒體專案的 URL;媒體專案的 URL 接著會指派給 player 物件 **url** 屬性。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Store the sample playlist object in a variable. 
var pl = Player.playlistCollection.getByName("Sample Playlist").item(0);

// Store the first media item from the sample playlist.
var media = pl.item(0);

// Change the URL property of the player to the URL of the media item.
Player.URL = media.sourceURL;

// Play the media item.
Player.controls.play();

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**媒體物件**](media-object.md)
</dt> </dl>

 

 





