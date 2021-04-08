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
# <a name="playlist-attributes"></a><span data-ttu-id="2f086-114">播放清單屬性</span><span class="sxs-lookup"><span data-stu-id="2f086-114">Playlist Attributes</span></span>

<span data-ttu-id="2f086-115">播放清單有稱為屬性的中繼資料資訊，就像媒體專案具有屬性一樣。</span><span class="sxs-lookup"><span data-stu-id="2f086-115">Playlists have metadata information called attributes, just as media items have attributes.</span></span> <span data-ttu-id="2f086-116">您可以取出播放清單屬性的名稱和值，並將它們顯示在使用者介面中，或者您的程式碼可以根據屬性的值採取動作。</span><span class="sxs-lookup"><span data-stu-id="2f086-116">You can retrieve the names and values of playlist attributes and display them in your user interface, or your code can take actions based on the value of an attribute.</span></span>

<span data-ttu-id="2f086-117">播放清單是在以 XML 格式組織的檔案中定義，而檔案中的特定元素則是定義播放清單屬性。</span><span class="sxs-lookup"><span data-stu-id="2f086-117">Playlists are defined in files organized in an XML format, and particular elements in the file define playlist attributes.</span></span> <span data-ttu-id="2f086-118">某些屬性元素是已知的;中繼檔的作者也可以定義任意屬性。</span><span class="sxs-lookup"><span data-stu-id="2f086-118">Some attribute elements are well-known; the author of the metafile can also define arbitrary attributes.</span></span> <span data-ttu-id="2f086-119">如需有關播放清單檔案中 attribute 元素的詳細資訊，請參閱抓取 [中繼資料](retrieving-metadata.md)。</span><span class="sxs-lookup"><span data-stu-id="2f086-119">For more information about attribute elements in playlist files, see [Retrieving Metadata](retrieving-metadata.md).</span></span>

<span data-ttu-id="2f086-120">程式庫可能會提供額外的播放清單屬性，例如 **SourceURL** 或 **UserLastPlayedTime**。</span><span class="sxs-lookup"><span data-stu-id="2f086-120">The library may provide additional playlist attributes, such as **SourceURL** or **UserLastPlayedTime**.</span></span> <span data-ttu-id="2f086-121">如需程式庫播放清單屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="2f086-121">For more information about the library playlist attributes, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="2f086-122">*播放清單*。**attributeCount** 屬性會捕獲與播放清單相關聯的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="2f086-122">The *Playlist*.**attributeCount** property retrieves the number of attributes associated with the playlist.</span></span> <span data-ttu-id="2f086-123">*播放清單*。**attributeName** 屬性會根據屬性的索引和 *播放清單* 來抓取屬性的名稱。**getItemInfo** 方法會根據屬性的名稱來抓取屬性的值。</span><span class="sxs-lookup"><span data-stu-id="2f086-123">The *Playlist*.**attributeName** property retrieves the name of an attribute based on its index, and the *Playlist*.**getItemInfo** method retrieves the value of an attribute based on its name.</span></span>

<span data-ttu-id="2f086-124">您可以使用 *播放清單* 修改目前播放清單的屬性值。**setItemInfo** 方法。</span><span class="sxs-lookup"><span data-stu-id="2f086-124">You can modify the value of an attribute of the current playlist with the *Playlist*.**setItemInfo** method.</span></span>

<span data-ttu-id="2f086-125">**SetItemInfo** 方法的特殊用途是使用 **SortAttribute** 屬性來排序播放清單中的專案。</span><span class="sxs-lookup"><span data-stu-id="2f086-125">A special use of the **setItemInfo** method is to sort the items in the playlist, using the **SortAttribute** attribute.</span></span> <span data-ttu-id="2f086-126">下列 c # 範例會依 **UserLastPlayedTime** 屬性的值來排序播放清單。</span><span class="sxs-lookup"><span data-stu-id="2f086-126">The following C# example sorts a playlist by the values of the **UserLastPlayedTime** attribute.</span></span> <span data-ttu-id="2f086-127">變數 *播放* 清單是 **播放清單** 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="2f086-127">The variable *Playlist* is a reference to a **Playlist** object.</span></span>


```C++
Playlist.setItemInfo("SortAttribute", "UserLastPlayedTime");

```



<span data-ttu-id="2f086-128">在本主題中， **Player** 物件是以下列方式定義：</span><span class="sxs-lookup"><span data-stu-id="2f086-128">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="2f086-129">下列 c # 範例程式碼示範如何取出播放清單屬性。</span><span class="sxs-lookup"><span data-stu-id="2f086-129">The following C# example code demonstrates retrieving playlist attributes.</span></span> <span data-ttu-id="2f086-130">第一個函式 ShowPlaylists 會以可用播放清單的名稱填入 ListBox 控制項。</span><span class="sxs-lookup"><span data-stu-id="2f086-130">The first function, ShowPlaylists, populates a ListBox control with the names of the available playlists.</span></span> <span data-ttu-id="2f086-131">第二個部分是清單方塊事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="2f086-131">The second part is the list box event handler.</span></span> <span data-ttu-id="2f086-132">當使用者按一下播放清單名稱時，此程式碼會抓取該播放清單的屬性，並在第二個清單方塊中顯示這些屬性。</span><span class="sxs-lookup"><span data-stu-id="2f086-132">When the user clicks a playlist name, this code retrieves the attributes for that playlist and displays those attributes in a second list box.</span></span>


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



<span data-ttu-id="2f086-133">每次使用者選取播放清單名稱時，都會呼叫 ListBox 控制項的 SelectedIndexChanged 事件。</span><span class="sxs-lookup"><span data-stu-id="2f086-133">The SelectedIndexChanged event for the ListBox control is called each time the user selects a playlist name.</span></span> <span data-ttu-id="2f086-134">下列事件處理常式會填滿第二個清單方塊，其中包含與使用者選取專案對應的屬性名稱和值。</span><span class="sxs-lookup"><span data-stu-id="2f086-134">The following event handler fills a second list box with the attribute names and values corresponding to the user's selection.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2f086-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f086-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f086-136">**管理播放清單**</span><span class="sxs-lookup"><span data-stu-id="2f086-136">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="2f086-137">**媒體專案屬性**</span><span class="sxs-lookup"><span data-stu-id="2f086-137">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="2f086-138">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="2f086-138">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




