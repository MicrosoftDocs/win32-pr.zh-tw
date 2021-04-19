---
title: 關於 MediaCollection 和 Media 物件
description: 關於 MediaCollection 和 Media 物件
ms.assetid: e3260efd-44cc-4b4e-9f48-3441631bfa4f
keywords:
- Windows Media Player，MediaCollection 物件
- Windows Media Player 物件模型，MediaCollection 物件
- 物件模型，MediaCollection 物件
- Windows Media Player ActiveX 控制項，MediaCollection 物件
- ActiveX 控制項，MediaCollection 物件
- Windows Media Player 行動 ActiveX 控制項，MediaCollection 物件
- Windows Media Player Mobile，MediaCollection 物件
- MediaCollection 物件
- Windows Media Player，媒體物件
- Windows Media Player 物件模型，媒體物件
- 物件模型，媒體物件
- Windows Media Player ActiveX 控制項、媒體物件
- ActiveX 控制項、媒體物件
- Windows Media Player 的行動 ActiveX 控制項、媒體物件
- Windows Media Player Mobile，Media 物件
- 媒體物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe902fd9ed046e0197fb5c8c2d995d26befafe29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106976323"
---
# <a name="about-the-mediacollection-and-media-objects"></a>關於 MediaCollection 和 Media 物件

**MediaCollection** 和 **media** 物件會管理媒體集合，以定義 Windows Media Player 可以存取的數位媒體檔案的位置。 您可以從 **Player** 物件的 **MediaCollection** 屬性取得 **MediaCollection** 物件。 **MediaCollection** 屬性會傳回 **mediaCollection** 物件。 您只能在建立 **MediaCollection** 物件之後，存取其屬性。 例如，若要將 **Media** 物件新增 () 的歌曲，請使用下列程式碼：


```C++
player.mediacollection.add('laure.wma');

```



您已將 laure 檔案新增至媒體集合。

您可以使用 **播放** 程式的 **currentMedia** 屬性來取得目前的 **媒體** 物件。 例如，此程式碼會取得目前 **媒體** 物件的 **duration** 屬性：


```C++
myduration = player.currentmedia.duration;

```



有許多方法可取得 **媒體** 物件，讓您可以存取其屬性。 例如，如果您想要存取目前媒體的 **duration** 屬性，則可以使用下列每一行程式碼。

若要取得目前播放媒體的持續時間：


```C++
player.currentMedia.duration;

```



若要取得播放清單中目前媒體的持續時間：


```C++
player.controls.currentItem.duration;

```



若要取得播放清單中第三個媒體專案的持續時間：


```C++
player.currentPlaylist.item(2).duration;

```



若要取得「爵士樂」類型中第三個媒體專案的持續時間：


```C++
player.mediaCollection.getByGenre("jazz").item(2).duration;

```



若要取得第二個播放清單中第三個媒體專案的持續時間：


```C++
player.playlistCollection.getAll.item(1).item(2).duration; 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**媒體物件**](media-object.md)
</dt> <dt>

[**MediaCollection 物件**](mediacollection-object.md)
</dt> <dt>

[**指令碼語言的播放程式物件模型**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




