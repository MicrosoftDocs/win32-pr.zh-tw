---
title: Media. duration
description: Duration 屬性會取出目前媒體專案的持續時間（以秒為單位）。
ms.assetid: d7d36858-812d-471b-84ce-fe2ab96b86b3
keywords:
- Media. duration Windows Media Player
topic_type:
- apiref
api_name:
- Media.duration
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e89eab1ffbb8c9f3d48c3f61eb6d831af66b4931ed1d858658eed3fc21d08183
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118798"
---
# <a name="mediaduration"></a>Media. duration

**Duration** 屬性會取出目前媒體專案的持續時間（以秒為單位）。

## <a name="syntax"></a>Syntax

*玩家*。*currentMedia*。**持續時間**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 (**雙**) 的 **數位**。

## <a name="remarks"></a>備註

如果這個屬性與 media 專案一起使用，而不是 *播放* 程式中指定的媒體專案。**currentMedia**，它可能不包含有效的值。

若要取得不在使用者程式庫中的檔案持續時間，您必須等候 Windows Media Player 開啟檔案;亦即，目前的 OpenState 必須等於 MediaOpen。 您可以藉由處理 *播放* 程式來確認這一點。**OpenStateChange** 事件，或定期檢查 *Player* 的值。**openState**。

若為播放清單，當個別媒體專案開啟時，可以抓取每個媒體專案的持續時間，而不是開啟播放清單時的。

若要取得這個屬性的值，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

下列 JScript 範例會使用 *媒體*。顯示目前媒體專案剩餘時間的 **持續** 時間。 名為 RemTime 的 HTML DIV 元素會顯示資訊。 HTML 計時器會每秒更新 DIV 元素中的文字。

下列 JScript 程式碼會啟動計時器：


```JScript
// Execute the update() function at one-second intervals.
idTmr = window.setInterval("update()",1000);
```



下列 JScript 程式碼會停止計時器：


```JScript
window.clearInterval(idTmr);
```



使用 *播放*。具有 **switch** 語句的 **PlayStateChange** 事件，以判斷何時要啟動和停止計時器。

每次計時器呼叫 update 函數時，都會執行下列 JScript 程式碼：


```JScript
// Store the current position of the current media item.
var TimeNow = Player.controls.currentPosition;

// Display the time remaining information.
RemTime.innerHTML = "Seconds remaining: ";

// Subtract the current position from the duration of the current media.
// Use the Math.floor method to round the result down to the nearest integer.
RemTime.innerHTML += Math.floor(Player.currentMedia.duration - TimeNow);
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

[**PlayStateChange 事件**](player-player-playstatechange.md)
</dt> <dt>

[**設定. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**設定. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





