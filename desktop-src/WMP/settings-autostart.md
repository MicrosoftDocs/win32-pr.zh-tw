---
title: 設定。 autoStart
description: AutoStart 屬性會指定或抓取值，指出目前的媒體專案是否會自動開始播放。
ms.assetid: 553f8534-9e3e-4fdc-bfc1-551939969289
keywords:
- 設定： autoStart Windows Media Player
topic_type:
- apiref
api_name:
- Settings.autoStart
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d08b8f84f4a0b51225ed5692a25fa41cab809ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985988"
---
# <a name="settingsautostart"></a>設定。 autoStart

**AutoStart** 屬性會指定或抓取值，指出目前的媒體專案是否會自動開始播放。

## <a name="syntax"></a>Syntax

設定： autoStart

## <a name="possible-values"></a>可能的值

這個屬性是讀取/寫入 **布林值**。



| 值 | 描述                                                         |
|-------|---------------------------------------------------------------------|
| true  | 預設值。 媒體專案會自動開始播放 (請參閱備註) 。 |
| false | 媒體專案不會自動開始播放。                |



 

## <a name="remarks"></a>備註

如果 **自動啟動** 設定為 true，則會在 *播放* 程式時開始播放媒體專案。**URL**、 *播放機*。**currentPlaylist** 或 *播放機*。已設定 **currentMedia** 。 否則，它將不會開始播放，直到 *控制項* 為止。會呼叫 **play** 方法。

由於 Windows Media Player 完整模式的 **autoStart** 屬性可以由外來事件全域設定 (例如載入 CD) ，因此沒有適用于外觀和遠端播放機控制項的可靠預設值。 這是因為在這兩種情況下都會使用完整模式播放機的播放引擎。

您應該在設定 *Player* 之前，立即將 **autoStart** 設定為 false。**URL**、*播放機*。**currentPlaylist** 或 *播放機*。如果您想要確保媒體專案不會立即開始播放，請在 [外觀] 和 [遠端 Windows Media Player] 控制項中 **currentMedia** 。 此外，除非您在指定媒體專案之前立即將 **autostart** 設定為 true，否則您不應該依賴此設定來替代使用 *控制項*。**play** 方法。

## <a name="examples"></a>範例

下列範例會建立 HTML CHECKBOX 元素，讓使用者可以指定播放程式控制項是否自動播放目前的媒體專案。 使用 ID = "Player" 建立 **player** 物件。


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX" ID = AS
              onClick = "
    /* Use the CHECKBOX state to specify the value 
       of the autoStart property. */
    Player.settings.autoStart = AS.checked;
"> 

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CurrentMedia**](player-currentmedia.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Settings 物件**](settings-object.md)
</dt> </dl>

 

 





