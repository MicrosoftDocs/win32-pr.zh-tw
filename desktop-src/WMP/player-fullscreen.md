---
title: Media Player. 全螢幕
description: 全螢幕屬性會指定或抓取值，指出是否以全螢幕模式播放影片內容。
ms.assetid: 43eeeddd-13a6-44d8-9cff-a60e976fc189
keywords:
- Media Player. 全螢幕 Windows Media Player
topic_type:
- apiref
api_name:
- Player.fullScreen
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3f71b4100c359effd95f79c574a52b5a5bae28c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995191"
---
# <a name="playerfullscreen"></a>Media Player. 全螢幕

**全** 螢幕屬性會指定或抓取值，指出是否以全螢幕模式播放影片內容。

## <a name="syntax"></a>Syntax

*玩家* 。**全螢幕**

## <a name="possible-values"></a>可能的值

這個屬性是讀取/寫入 **布林值**。



| 值 | 描述                                                    |
|-------|----------------------------------------------------------------|
| true  | 影片內容會以全螢幕模式播放。              |
| false | 預設值。 影片內容不會以全螢幕模式播放。 |



 

## <a name="remarks"></a>備註

若要在內嵌 Windows Media Player 控制項時讓全螢幕模式正常運作，影片顯示區域必須具有至少一個圖元的高度和寬度。 如果 **uiMode** 設定為「迷你」或「完整」，則控制項本身的高度必須是65或更大，才能容納除了使用者介面之外的影片顯示區域。

如果 **uiMode** 設為「隱藏」，則將這個屬性設定為 true 會引發錯誤，而且不會影響控制項的行為。

在全螢幕播放期間，Windows Media Player 會在 **enableCoNtextMenu** 等於 False 且 **uiMode** 等於 "none" 時隱藏滑鼠游標。

如果 **uiMode** 設為「完整」或「迷你」，Windows Media Player 在滑鼠游標移動時，以全螢幕模式顯示傳輸控制項。 在不移動滑鼠的短暫間隔之後，就會隱藏傳輸控制項。 如果 **uiMode** 設為 "none"，就不會在全螢幕模式中顯示任何控制項。

**注意**

以全螢幕模式顯示傳輸控制項需要 Windows XP 作業系統。

如果傳輸控制項未以全螢幕模式顯示，則 Windows Media Player 會在播放停止時自動離開全螢幕模式。

**注意**

務必通知使用者如何從全螢幕模式中返回。

## <a name="examples"></a>範例

下列範例會建立使用 *Player* 的 HTML 輸入按鈕。將內嵌播放機物件切換至全螢幕模式的 **全** 螢幕。 使用 ID = "Player" 建立 **player** 物件。


```
<INPUT type = button 
       value = "Full Screen" 
       name = FSBUTTON
       onclick = "
               /* Check to be sure the player is playing. */
               if (Player.playState == 3) 
                  Player.fullScreen = 'true';
               ">
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





