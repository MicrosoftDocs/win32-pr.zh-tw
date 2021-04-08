---
title: 播放清單屬性
description: 播放清單屬性
ms.assetid: 2f2224ad-a1de-4f88-9166-8c00137a3695
keywords:
- Windows Media Player，播放清單
- Windows Media Player 物件模型，播放清單
- 物件模型，播放清單
- Windows Media Player 行動裝置、播放清單
- Windows Media Player ActiveX 控制項，播放清單
- Windows Media Player 的行動 ActiveX 控制項、播放清單
- ActiveX 控制項，播放清單
- 播放清單、屬性
- 中繼檔播放清單，屬性
- Windows Media 中繼檔播放清單，屬性
- 屬性、播放清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669d3203fdb703099a7089e2165f31fd5bb326bb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932084"
---
# <a name="playlist-attributes"></a>播放清單屬性

播放清單有稱為屬性的中繼資料資訊，就像媒體專案具有屬性一樣。 您可以取出播放清單屬性的名稱和值，並將它們顯示在使用者介面中，或者您的程式碼可以根據屬性的值採取動作。

播放清單是在以 XML 格式組織的檔案中定義，而檔案中的特定元素則是定義播放清單屬性。 某些屬性元素是已知的;中繼檔的作者也可以定義任意屬性。 如需有關播放清單檔案中 attribute 元素的詳細資訊，請參閱抓取 [中繼資料](retrieving-metadata.md)。

程式庫可能會提供額外的播放清單屬性，例如 **SourceURL** 或 **UserLastPlayedTime**。 如需程式庫播放清單屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。

*播放清單*。**attributeCount** 屬性會捕獲與播放清單相關聯的屬性數目。 *播放清單*。**attributeName** 屬性會根據屬性的索引和 *播放清單* 來抓取屬性的名稱。**getItemInfo** 方法會根據屬性的名稱來抓取屬性的值。

您可以使用 *播放清單* 修改目前播放清單的屬性值。**setItemInfo** 方法。

**SetItemInfo** 方法的特殊用途是使用 **SortAttribute** 屬性來排序播放清單中的專案。 下列 c # 範例會依 **UserLastPlayedTime** 屬性的值來排序播放清單。 變數 *播放* 清單是 **播放清單** 物件的參考。


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



在本主題中， **Player** 物件是以下列方式定義：


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



下列 c # 範例程式碼示範如何取出播放清單屬性。 第一個函式 ShowPlaylists 會以可用播放清單的名稱填入 ListBox 控制項。 第二個部分是清單方塊事件處理常式。 當使用者按一下播放清單名稱時，此程式碼會抓取該播放清單的屬性，並在第二個清單方塊中顯示這些屬性。


```C++
// Member variables
IWMPPlaylistCollection PlaylistColl;
IWMPPlaylistArray PlaylistArray;

private void ShowPlaylists()
{
    // Retrieve the playlist collection
    PlaylistColl = Player.playlistCollection;
    // Store the collection in a playlist array
    PlaylistArray = PlaylistColl.getAll();

    // Retrieve the count of elements
    iCount = PlaylistArray.count;

    // Update the list box with the playlist names.
    lstPlaylist.BeginUpdate();
    for (int i=0; i<iCount; i++)
    {
        lstPlaylist.Items.Add(PlaylistArray.Item(i).name);
    }
    lstPlaylist.EndUpdate();

    // Set the selected index to zero
    lstPlaylist.SelectedIndex = 0;
}

```



每次使用者選取播放清單名稱時，都會呼叫 ListBox 控制項的 SelectedIndexChanged 事件。 下列事件處理常式會填滿第二個清單方塊，其中包含與使用者選取專案對應的屬性名稱和值。


```C++
private void lstPlaylist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    IWMPPlaylist Playlist = PlaylistArray.Item(lstPlaylist.SelectedIndex);
    string strAttr="";
    string strItemNames="";
    int iAttribCount=0;

    iAttribCount = Playlist.attribCount;
    for (j=0; j<iAttribCount; j++)
    {
        strAttr=Playlist.get_attributeName(j) + " -- ";
        strAttr+=Playlist.getItemInfo(Playlist.get_attributeName(j));
        lstOutput.Items.Add(strAttr);
    }
}

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**管理播放清單**](managing-playlists.md)
</dt> <dt>

[**媒體專案屬性**](media-item-attributes.md)
</dt> <dt>

[**播放清單物件**](playlist-object.md)
</dt> </dl>

 

 




