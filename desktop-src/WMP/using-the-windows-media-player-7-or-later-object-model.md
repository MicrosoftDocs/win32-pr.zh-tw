---
title: 使用 Windows Media Player 7 或更新版本的物件模型
description: 使用 Windows Media Player 7 或更新版本的物件模型
ms.assetid: e2dbe2c1-23be-499b-b754-b7e87486ecd6
keywords:
- Windows Media Player，物件模型
- Windows Media Player 物件模型7版或更新版本
- 物件模型7版或更新版本
- Windows Media Player ActiveX 控制項7版或更新版本
- ActiveX 控制項，7版或更新版本
- Windows Media Player 的行動 ActiveX 控制項7版或更新版本
- Windows Media Player 行動裝置，物件模型
- 第7版或更新版本的遷移指南
- Windows Media Player 的版本，物件模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eb4d3d09b38e381d0cddeb25ee7cb5d7de3cb2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301232"
---
# <a name="using-the-windows-media-player-7-or-later-object-model"></a>使用 Windows Media Player 7 或更新版本的物件模型

您可能使用 Windows Media Player 6.4 ActiveX 控制項物件模型執行的大部分工作都需要新的方法。 在許多情況下，屬性、方法和事件的名稱在 Windows Media Player 7 或更新版本的物件模型中已經變更。 比方說，若要在6.4 版物件模型中指定檔案路徑，您可以設定 **Player6 檔案名** 屬性：


```C++
WMP64.FileName = "https://www.microsoft.com/somefile.wmv";

```



使用 Windows Media Player 7 或更新版本的物件模型時，您必須設定 **Media Player. URL** 屬性：


```C++
WMP9.URL = "https://www.microsoft.com/somefile.wmv";

```



或者，使用10個物件模型，您可以從程式庫取得 **媒體** 物件，然後設定 **currentMedia** 屬性：


```C++
// Get the first media object in the media collection.
var MyMediaItem = WMP9.mediaCollection.getAll().item(0)

// Make the MyMediaItem object the current media.
WMP9.currentMedia = MyMediaItem;

```



Windows Media Player 7 或更新版本物件模型中的大部分功能都是透過物件階層進行存取。 如上一個範例所示，您可以使用 **mediaCollection** 物件的 **getAll** 方法來取得 **播放清單** 物件，該方法是透過根 **播放機** 物件來存取。 然後，您可以使用 **播放清單** 物件的 **item** 方法，從 **播放清單** 物件取得特定 **媒體** 物件。 有五個額外的方法可透過傳回 **播放清單** 物件的 **mediaCollection** 物件存取;每個方法都可讓您根據特定條件（例如內容類型或專輯）來取得物件。

Windows Media Player 7 或更新版本的 ActiveX 控制項物件模型的階層式結構，可提供更多邏輯方法來組織可供您使用的屬性、方法和事件。 Player 控制項的所有功能都包含在 **controls** 物件中，而 player 網路連接的所有功能都包含在 **network** 物件中，依此類推。 例如，若要使用6.4 版物件模型開始播放內容，您可以使用 **Player6** 方法：


```C++
WMP64.Play();

```



使用 Windows Media Player 7 或更新版本的物件模型時，您必須使用 **Controls** 物件來存取 **Play** 方法：


```C++
WMP9.controls.play();

```



不過，物件模型的深度可能會導致很長的腳本語句：


```C++
WMP9.currentPlaylist.appendItem(WMP9.mediaCollection.getByName("MySong").item(0));

```



使用個別的命名物件，可讓您更簡單且更容易閱讀的語句（如先前的語句）。 下列範例會使用不同的物件變數，以語法取代上述的程式碼語句：


```C++
// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Get a playlist from the media collection that contains
// one media item named "MySong".
var temp = WMP9.mediaCollection.getByName("MySong");

// Get the individual media item from the temp playlist.
var song = temp.item(0);

// Append the media item to the current playlist.
pl.appendItem(song);

```



這種編碼樣式需要更多程式碼，但更容易遵循，尤其是新增的批註。 還有另一項優點： **currentPlaylist** 物件會儲存在變數 pl 中，方便重複使用。

在 Windows Media Player 7 或更新版本的物件模型中，許多屬性、方法和事件都會設定或抓取不同的值，或傳回不同類型或數位的值，相較于6.4 版物件模型中的對應功能。 例如，當 **Player6 openState** 抓取2時，該值會對應至 Visual Basic 常數 **nsLoadingNSC**，這表示播放程式正在載入副檔名為 .nsc 的工作站檔案。 但是，當 Windows Media Player 7 或更新版本的物件模型屬性 **播放機 openState** 抓取2時，該值會對應至狀態 PlaylistLocating，這表示 Windows Media Player 正在嘗試尋找播放清單。 此外， **Player6. openState** 屬性可以抓取七個不同的值，而 Windows Media Player 7 或更新版本的 **Player. openState** 屬性可以取出22個不同的值。 修改程式碼以使用不同的物件模型版本時，請務必參考 Windows Media Player SDK 之腳本區段的物件模型參考。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Player 物件模型**](about-the-player-object-model.md)
</dt> <dt>

[**腳本的物件模型參考**](object-model-reference-for-scripting.md)
</dt> <dt>

[**物件模型遷移指南**](object-model-migration-guide.md)
</dt> </dl>

 

 




