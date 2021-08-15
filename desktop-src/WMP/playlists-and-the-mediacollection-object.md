---
title: 播放清單和 MediaCollection 物件
description: 播放清單和 MediaCollection 物件
ms.assetid: 3c98ceed-2545-4774-998b-c1db0d172a81
keywords:
- Windows Media Player，播放清單
- Windows Media Player 物件模型，播放清單
- 物件模型，播放清單
- Windows Media Player行動裝置、播放清單
- Windows Media Player ActiveX 控制項、播放清單
- Windows Media Player行動 ActiveX 控制項、播放清單
- ActiveX 控制項，播放清單
- 播放清單，MediaCollection 物件
- 中繼檔播放清單，MediaCollection 物件
- Windows媒體中繼檔播放清單，MediaCollection 物件
- MediaCollection 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b1a0bba2e966e51523dc24965c2f2a066767b059f26a08fde9ee5856a1694df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334451"
---
# <a name="playlists-and-the-mediacollection-object"></a>播放清單和 MediaCollection 物件

**MediaCollection** 物件可讓您存取各種特殊的播放清單，並包含從中繼檔建立新播放清單的方法。

下列方法會取出特殊的播放清單：

-   **getAll**
-   **getByAlbum**
-   **getByAttribute**
-   **getByAuthor**
-   **getByGenre**
-   **getByName**

顧名思義，這些方法會取出包含媒體櫃中符合特定準則之所有媒體專案的播放清單。

請小心不要混淆 *MediaCollection*。具有 *PlaylistCollection* 的 **getByName** 方法。**getByName** 方法。 **MediaCollection** 方法會傳回包含所有具有指定名稱之媒體專案的 **播放清單** 物件。 **PlaylistCollection** 方法會傳回 **PlaylistArray** 物件，其中包含所有具有指定名稱的播放清單。

您可以使用 *MediaCollection*。**新增** 方法，以將播放清單以及媒體專案新增至程式庫。 若要加入播放清單，請將路徑傳遞給定義播放清單的中繼檔。 方法一律會傳回 **媒體** 物件。 您無法在 **媒體** 與 **播放清單** 物件之間轉換。 若要使用您新增的播放清單，請取得與 **媒體** 物件同名的 **播放清單** 物件。

下列 c # 範例示範如何使用 **MediaCollection** 依類型取得媒體。**getByAttribute** 方法。 此程式碼會抓取與指定類型相關聯之所有屬性的名稱，以及這些屬性的讀/寫或唯讀狀態。 它會產生單一檔案，其中包含音訊、影片、廣播、播放清單、其他、音樂和相片類型的屬性清單。


```C++
string strOutFile = "AttribList.txt";    // Name of the output file
...
StreamWriter sw = new StreamWriter(strOutFile, true);

sw.Write(getMediaCollectionNames("Audio"));
sw.Write(getMediaCollectionNames("Video"));
sw.Write(getMediaCollectionNames("Radio"));
sw.Write(getMediaCollectionNames("Playlist"));
sw.Write(getMediaCollectionNames("Other"));
sw.Write(getMediaCollectionNames("Music"));
sw.Write(getMediaCollectionNames("Photo"));
sw.Close();
...
// The getMediaCollection method retrieves the names of
// all attributes for a specified type.
private string getMediaCollectionNames(string sSchema)
{
IWMPPlaylist playlist;
IWMPMedia media;
string strResult = "";    // Cumulative list of attributes
string strAttrName = "";  // Attribute name
string strReadWrite = ""; // Read/Write status of attribute
int iAttrCount = 0;       // Count of playlist attributes

// Retrieve a playlist corresponding to the requested type.
playlist = Player.mediaCollection.getByAttribute("MediaType", sSchema);

// Initialize the result string
strResult += "\n" + sSchema.ToString() + " Schema: \n";

// Retrieve the attributes for the playlist
if (playlist.count != 0)
{
    media = playlist.get_Item(0);
    iAttrCount = media.attributeCount;
    for (int i = 0; i < iAttrCount; i++)
    {
        strAttrName = media.getAttributeName(i);
        strResult += "   " + strAttrName  +"\n";
        if (media.isReadOnlyItem(strAttrName))
            strReadWrite = "Read Only";
        else
            strReadWrite = "Read/Write";
        strResult += "         " + strReadWrite + "\n";
    }
}

return strResult;
}

```



下列 c # 範例示範如何從中繼檔將播放清單新增至程式庫。


```C++
// Add a playlist as a media item
IWMPMedia Media = Player.mediaCollection.add("c:\\testPlayList.asx");

```



靜態播放清單包含特定媒體專案。 自動播放清單會在每次開啟程式庫時搜尋程式庫，而且可能會在不同時間包含不同的媒體專案。 您可以使用 *MediaCollection*，將靜態和自動播放清單新增至程式庫。**add** 方法。 您也可以使用 *PlaylistCollection* 來新增靜態播放清單。**importPlaylist** 方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**管理播放清單**](managing-playlists.md)
</dt> <dt>

[**MediaCollection 物件**](mediacollection-object.md)
</dt> <dt>

[**播放清單物件**](playlist-object.md)
</dt> <dt>

[**PlaylistCollection 物件**](playlistcollection-object.md)
</dt> <dt>

[**播放清單和 PlaylistCollection 物件**](playlists-and-the-playlistcollection-object.md)
</dt> <dt>

[**靜態和自動播放清單**](static-and-auto-playlists.md)
</dt> </dl>

 

 




