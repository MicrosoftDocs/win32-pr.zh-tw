---
title: 管理媒體專案
description: 管理媒體專案
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Windows Media Player，程式庫
- Windows Media Player 物件模型，程式庫
- 物件模型，程式庫
- Windows Media Player 行動裝置、物件模型的程式庫
- Windows Media Player ActiveX 控制項，物件模型的程式庫
- Windows Media Player 的行動 ActiveX 控制項、物件模型的程式庫
- ActiveX 控制項，物件模型的程式庫
- Windows Media Player 程式庫，管理媒體專案
- 媒體櫃，管理媒體專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b8003de49de9b7e4e51aabeffa222fb649ddef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092317"
---
# <a name="managing-media-items"></a>管理媒體專案

**媒體** 物件代表一個媒體專案。 它具有可用來抓取資訊並向使用者顯示資訊的屬性和方法，或根據您抓取的值採取不同的動作。

**媒體** 物件的大部分工作都牽涉到與媒體專案內容相關的中繼資料（稱為屬性）。 主題 [媒體專案屬性](media-item-attributes.md) 說明如何讀取和變更屬性值。 除了本主題之外，請參閱 Microsoft 網站上的 [Windows Media 中繼資料使用指導方針](/previous-versions/ms867702(v=msdn.10)) ，以取得有關屬性及其用途的詳細資訊。

**媒體** 物件具有直接取出部分屬性的屬性和方法，例如專案的名稱或持續時間。 針對影片專案，您可以抓取影像的高度和寬度，也可以根據標記的名稱或索引來取得標記資訊。 您也可以判斷特定媒體專案是否包含在特定的播放清單中。

## <a name="retrieving-a-media-object"></a>取出媒體物件

您可以使用 *播放* 程式來快速存取目前的媒體專案。**currentMedia** 屬性。

在本主題中， **Player** 物件是以下列方式定義：


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



下列 c # 範例會捕獲代表目前專案的 **媒體** 物件。


```C++
IWMPMedia media;
media = Player.currentMedia;

```



您可以使用 *播放* 程式，從數位媒體檔案建立新的媒體專案。**newMedia** 方法。 您將 URL 路徑傳遞至數位媒體檔案，它會傳回新 **媒體** 物件的參考。 方法不會直接將新的物件加入至程式庫。 不過，您可以將物件傳遞至 *播放清單*。**appendItem** 方法或 *播放清單*。**insertItem** 方法。

下列 c # 範例會根據隨 Windows Media Player SDK 一併安裝的其中一個數位媒體範例，建立 **媒體** 物件。


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> 您必須在字串中包含兩個反斜線 (\) 字元 (或在 c # ) 中使用 @ 字元，以代表一個實際的反斜線字元。 這是因為 c # 會使用單一反斜線字元來定義 escape 序列。

 

您可以使用 *MediaCollection*，從數位媒體檔案建立新的媒體專案，並將其新增至程式庫。**add** 方法。 就像 *玩家* 一樣。**newMedia** 方法， **add** 方法會採用數位媒體檔案的路徑。

下列 c # 範例會根據其中一個 SDK 範例檔案建立 **媒體** 物件，並將該物件新增至程式庫。


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



您可以使用 *播放清單* 來取出代表播放清單中媒體專案的 **媒體** 物件。**item** 方法。 下列 c # 範例會從目前的播放清單抓取第六個媒體專案。


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CurrentItem**](controls-currentitem.md)
</dt> <dt>

[**管理播放清單**](managing-playlists.md)
</dt> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**MediaCollection 新增**](mediacollection-add.md)
</dt> <dt>

[**CurrentMedia**](player-currentmedia.md)
</dt> <dt>

[**NewMedia**](player-newmedia.md)
</dt> <dt>

[**播放清單。專案**](playlist-item.md)
</dt> <dt>

[**使用程式庫**](working-with-the-library.md)
</dt> </dl>

 

 




