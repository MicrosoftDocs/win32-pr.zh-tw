---
title: 在 Firefox 所顯示的網頁中使用腳本
description: 在 Firefox 所顯示的網頁中使用腳本
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player ActiveX 控制項、網頁
- Windows Media Player 的行動 ActiveX 控制項、網頁
- ActiveX 控制項，網頁
- Windows Media Player ActiveX 控制項，腳本範例
- Windows Media Player Mobile ActiveX 控制項，腳本範例
- ActiveX 控制項，腳本範例
- 內嵌、網頁
- 網頁內嵌、腳本範例
- Windows Media Player，Firefox
- Windows Media Player 物件模型，Firefox
- 物件模型，Firefox
- Windows Media Player Mobile、Firefox
- Windows Media Player ActiveX 控制項，Firefox
- Windows Media Player Mobile ActiveX 控制項，Firefox
- ActiveX 控制項、Firefox
- Firefox，腳本範例
- 網頁內嵌、Firefox
- 網頁內嵌的腳本範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8629f87f954d12602999f76483fdd36ab279290
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2019
ms.locfileid: "106967856"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a>在 Firefox 所顯示的網頁中使用腳本

當使用者與頁面互動時，網頁上的腳本可以使用 Player 物件模型來控制播放機。 例如，下列輸入專案具有可設定播放程式音量的腳本。


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



Windows Media Player 物件模型中的許多物件都受到 Internet Explorer 和 Firefox 外掛程式的支援。 不過，Firefox 外掛程式不支援某些物件。 下表列出 Player 物件模型中的所有物件，並顯示 Firefox 外掛程式支援的物件。



| Object                                              | Firefox 支援 |
|-----------------------------------------------------|-----------------|
| [光碟](cdrom-object.md)                           | 不可以              |
| [CdromCollection](cdromcollection-object.md)       | 不可以              |
| [ClosedCaption](closedcaption-object.md)           | 是             |
| [控制項](controls-object.md)                     | 不可以              |
| [Dvd](dvd-object.md)                               | 不可以              |
| [錯誤](error-object.md)                           | 是             |
| [ErrorItem](erroritem-object.md)                   | 是             |
| [媒體](media-object.md)                           | 是             |
| [MediaCollection](mediacollection-object.md)       | 不可以              |
| [MetadataPicture](metadatapicture-object.md)       | 不可以              |
| [MetadataText](metadatatext-object.md)             | 不可以              |
| [Network](network-object.md)                       | 是             |
| [球員](player-object.md)                         | 是             |
| [PlayerApplication](playerapplication-object.md)   | 不可以              |
| [播放 清單](playlist-object.md)                     | 是             |
| [PlaylistArray](playlistarray-object.md)           | 不可以              |
| [PlaylistCollection](playlistcollection-object.md) | 不可以              |
| [查詢](query-object.md)                           | 不可以              |
| [設定](settings-object.md)                     | 是             |
| [StringCollection](stringcollection-object.md)     | 不可以              |



 

Firefox 外掛程式支援 **player** 物件，但是 **player** 物件的某些屬性會在 Firefox 瀏覽器中傳回 **Null** 。 例如， **Player** 物件的 [cdromCollection](player-cdromcollection.md)屬性會傳回 **Null** ，因為 Firefox 外掛程式不支援 **Cdrom** 物件。 同樣地，在 Firefox 瀏覽器中， **Player** 物件的 [dvd](player-dvd.md)、 [mediaCollection](player-mediacollection.md)、 [playerApplication](player-playerapplication.md)和 [playlistCollection](player-playlistcollection.md)屬性會傳回 **Null** 。

**PluginVersionInfo** 屬性受到 Firefox 外掛程式的支援，但不受 Internet Explorer。 這個屬性會傳回 Firefox 外掛程式的版本。

Firefox 外掛程式支援 **媒體** 物件，包括 [getItemInfoByType](media-getiteminfobytype.md) 屬性。 不過，在 Firefox 瀏覽器中， **getItemInfoByType** 屬性不支援 **MetadataText** 和 **MetadataPicture** 傳回型別。

Firefox 外掛程式除了[setMode](settings-setmode.md)方法和[requestMediaAccessRights](settings-requestmediaaccessrights.md)屬性之外，還支援[Settings](settings-object.md)物件。 在 Firefox 瀏覽器中， **requestMediaAccessRight** 屬性一律會傳回 false。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**搭配 Firefox 使用 Windows Media Player 控制項**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




