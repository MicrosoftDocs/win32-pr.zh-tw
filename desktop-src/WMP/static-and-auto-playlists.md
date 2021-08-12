---
title: 靜態和自動播放清單
description: 靜態和自動播放清單
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Windows Media Player，播放清單
- Windows Media Player 物件模型，播放清單
- 物件模型，播放清單
- Windows Media Player行動裝置、播放清單
- Windows Media Player ActiveX 控制項、播放清單
- Windows Media Player行動 ActiveX 控制項、播放清單
- ActiveX 控制項，播放清單
- 播放清單、靜態
- 中繼檔播放清單，靜態
- Windows媒體中繼檔播放清單，靜態
- 靜態播放清單
- 自動播放清單
- 播放清單、自動
- 中繼檔播放清單，自動
- Windows媒體中繼檔播放清單，自動
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645b3bd9ca9ddeebcce9fd6cbb905caa54717e87876be6e449ebd4d3ab64a11a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568780"
---
# <a name="static-and-auto-playlists"></a>靜態和自動播放清單

有兩種類型的播放清單：

-   包含特定媒體專案的靜態播放清單
-   自動播放清單，會在每次開啟程式庫時搜尋程式庫，而且可能會在不同的時間包含不同的媒體專案。 自動播放清單是資料庫查詢的結果。

若要從中繼檔匯入靜態播放清單，請先呼叫 *Player*。**[]** 根據中繼檔中的資料建立 **播放清單** 物件，然後將該物件傳遞至 *PlaylistCollection*。**importPlaylist** ，將播放清單新增至程式庫。

若要從中繼檔匯入自動播放清單，請使用 *MediaCollection*。**加入**。 如需詳細資訊，請參閱 [播放清單和 MediaCollection 物件](playlists-and-the-mediacollection-object.md)。

若要從自動播放清單中繼檔匯入靜態播放清單，請使用 *Player*。**[]** 和 *PlaylistCollection*。如先前所述 **importPlaylist** 。 自動播放清單會執行一次，而且會根據該執行的結果來建立靜態播放清單。

使用者透過網際網路存取的網頁不支援使用自動播放清單來查詢使用者的程式庫。

下列 c # 範例程式碼示範如何將自動播放清單中繼檔匯入為靜態播放清單。 若要執行此範例，請使用程式庫使用者介面建立自動播放清單，然後在此程式碼中包含自動播放清單中繼檔的正確路徑。


```C++
private void addStaticPlaylist()
{
    IWMPPlaylist pList;

    pList = Player.newPlaylist("NewImportedList", "\\\\myServer\\myPath\\artistcollection.wpl");
    if (pList.count == 0)
        MessageBox.Show("The specified playlist is empty.");
    else
        Player.playlistCollection.importPlaylist(pList);
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**管理播放清單**](managing-playlists.md)
</dt> </dl>

 

 




