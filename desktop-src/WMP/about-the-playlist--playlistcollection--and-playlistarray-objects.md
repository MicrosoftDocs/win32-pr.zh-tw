---
title: 關於播放清單、PlaylistCollection 和 PlaylistArray 物件
description: 關於播放清單、PlaylistCollection 和 PlaylistArray 物件
ms.assetid: 19867944-c836-4b7e-ada3-f696905e6327
keywords:
- Windows Media Player，播放清單物件
- Windows Media Player 物件模型、播放清單物件
- 物件模型、播放清單物件
- Windows Media Player ActiveX 控制項、播放清單物件
- ActiveX 控制項、播放清單物件
- Windows Media Player 行動 ActiveX 控制項、播放清單物件
- Windows Media Player Mobile，播放清單物件
- 播放清單物件
- Windows Media Player，PlaylistCollection 物件
- Windows Media Player 物件模型，PlaylistCollection 物件
- 物件模型，PlaylistCollection 物件
- Windows Media Player ActiveX 控制項，PlaylistCollection 物件
- ActiveX 控制項，PlaylistCollection 物件
- Windows Media Player 行動 ActiveX 控制項，PlaylistCollection 物件
- Windows Media Player Mobile，PlaylistCollection 物件
- PlaylistCollection 物件
- Windows Media Player，PlaylistArray 物件
- Windows Media Player 物件模型，PlaylistArray 物件
- 物件模型，PlaylistArray 物件
- Windows Media Player ActiveX 控制項，PlaylistArray 物件
- ActiveX 控制項，PlaylistArray 物件
- Windows Media Player 行動 ActiveX 控制項，PlaylistArray 物件
- Windows Media Player Mobile，PlaylistArray 物件
- PlaylistArray 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee9d24f4f5decc28a369e44910990ff41b99e9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106984505"
---
# <a name="about-the-playlist-playlistcollection-and-playlistarray-objects"></a>關於播放清單、PlaylistCollection 和 PlaylistArray 物件

**播放清單**、 **PlaylistCollection** 和 **PlaylistArray** 物件會管理 Windows Media Player 可用來指定播放內容之順序的播放清單。 您可以從 **Player** 物件的 **PlaylistCollection** 屬性取得 **PlaylistCollection** 物件。 **PlaylistCollection** 屬性會傳回 **playlistCollection** 物件。 您只能在建立 **PlaylistCollection** 物件之後，存取其屬性。 例如，若要建立新的播放清單，您必須先取得 **PlaylistCollection** 物件，然後在該物件上使用方法。


```C++
player.playlistcollection.newplaylist('myplaylist');
```



您可以使用 **currentPlaylist** 屬性來取得目前的播放清單。 例如，若要取得目前播放清單的名稱，請使用下列程式碼：


```C++
myname = player.currentplaylist.name;
```



**PlaylistArray** 物件是由 **PlaylistCollection** 物件的 **getAll** 和 **getByName** 方法所傳回。 例如，若要取得播放清單的數目，請使用下列程式碼：


```C++
howmany = player.playlistcollection.getAll().count;
```



若要依名稱取得已知播放清單，請使用下列程式碼：


```C++
if (player.playlistcollection.getbyname('myplaylist').count == 1) {
    pl = player.playlistcollection.getbyname('myplaylist').item(0);
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**指令碼語言的播放程式物件模型**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**播放清單物件**](playlist-object.md)
</dt> <dt>

[**PlaylistArray 物件**](playlistarray-object.md)
</dt> <dt>

[**PlaylistCollection 物件**](playlistcollection-object.md)
</dt> </dl>

 

 




