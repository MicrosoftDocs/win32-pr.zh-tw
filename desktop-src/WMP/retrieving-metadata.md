---
title: 擷取中繼資料
description: 擷取中繼資料
ms.assetid: f634118a-0a62-4407-8be1-a907347de55b
keywords:
- Windows Media 中繼檔播放清單，正在抓取中繼資料
- 播放清單，正在抓取中繼資料
- 中繼檔播放清單，正在抓取中繼資料
- Windows Media 中繼檔播放清單，中繼資料抓取
- 播放清單，中繼資料抓取
- 中繼檔播放清單，中繼資料抓取
- 中繼資料，正在抓取
- 擷取中繼資料
- Windows Media Player，正在抓取中繼資料
- Windows Media Player，中繼資料抓取
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c9855ec1dc95a52429561e91aa82abdac088523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932354"
---
# <a name="retrieving-metadata"></a><span data-ttu-id="02a45-113">擷取中繼資料</span><span class="sxs-lookup"><span data-stu-id="02a45-113">Retrieving Metadata</span></span>

<span data-ttu-id="02a45-114">當播放顯示或剪輯時，您的腳本可以使用 Windows Media Player **媒體** 和 **播放清單** 物件的 **getItemInfo** 方法，來取得中繼資料（例如標題和作者）。</span><span class="sxs-lookup"><span data-stu-id="02a45-114">While a show or clip is playing, your script can retrieve metadata, such as title and author, by using the **getItemInfo** methods of the Windows Media Player **Media** and **Playlist** objects.</span></span> <span data-ttu-id="02a45-115">您可以使用 **播放清單** 物件方法，以及從專案範圍使用 **媒體** 物件方法，從 ASX 範圍取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="02a45-115">You can retrieve metadata from the ASX scope using **Playlist** object methods and from the ENTRY scope using **Media** object methods.</span></span>

<span data-ttu-id="02a45-116">例如，若要在下列檔案中取出 AUTHOR、ABSTRACT 和 PARAM 的值，請使用 **播放清單** 物件的 **getItemInfo** 方法。</span><span class="sxs-lookup"><span data-stu-id="02a45-116">For example, to retrieve the values for AUTHOR, ABSTRACT and PARAM in the following file, use the **getItemInfo** method of the **Playlist** object.</span></span> <span data-ttu-id="02a45-117">此方法需要屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="02a45-117">The attribute name is required for this method.</span></span> <span data-ttu-id="02a45-118">藉由提供索引編號給 **attributeName** 屬性，即可取得屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="02a45-118">Attribute names can be obtained by providing the index number to the **attributeName** property.</span></span> <span data-ttu-id="02a45-119">您可以使用 **attributeCount** 屬性來取得 **播放清單** 物件的可用索引。</span><span class="sxs-lookup"><span data-stu-id="02a45-119">The available indexes for a **Playlist** object can be obtained using the **attributeCount** property.</span></span>

## <a name="example-code"></a><span data-ttu-id="02a45-120">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="02a45-120">Example Code</span></span>


```XML

    <ASX version="3.0">
        <AUTHOR>My Talking File</AUTHOR>
        <ABSTRACT>Talking File Album</ABSTRACT>
        <PARAM name="one" value="111"/>
        <ENTRY>
            <REF href="Artists_Only.wma"/>
            <TITLE>Artists Only</TITLE>
            <COPYRIGHT>2000</COPYRIGHT>
            <PARAM name="three" value="333"/>
        </ENTRY>
        <PARAM name="two" value="222"/>
    </ASX>
    

```



<span data-ttu-id="02a45-121">若要在 REF、TITLE、著作權和 PARAM 的專案範圍中取出目前 **媒體** 物件的值 ( "三" ) ，請使用 **Player** 物件的 **currentMedia** 屬性。</span><span class="sxs-lookup"><span data-stu-id="02a45-121">To retrieve the values of the current **Media** object in the ENTRY scope for REF,TITLE,COPYRIGHT, and PARAM ("three"), use the **currentMedia** property of the **Player** object.</span></span> <span data-ttu-id="02a45-122">使用 **媒體** 物件的 **attributeCount** 屬性，來判斷指定之 **媒體** 物件的可用屬性數目。</span><span class="sxs-lookup"><span data-stu-id="02a45-122">Use the **attributeCount** property of the **Media** object to determine the number of attributes available for the specified **Media** object.</span></span> <span data-ttu-id="02a45-123">使用 **getItemInfoByAtom** 方法的索引編號來取出屬性值。</span><span class="sxs-lookup"><span data-stu-id="02a45-123">Use index numbers with the **getItemInfoByAtom** method to retrieve attribute values.</span></span> <span data-ttu-id="02a45-124">使用具有 **媒體** 物件之 **getAttributeName** 方法的索引編號來判斷可用屬性的名稱，然後使用 **getItemInfo** 方法的結果。</span><span class="sxs-lookup"><span data-stu-id="02a45-124">Use index numbers with the **getAttributeName** method of the **Media** object to determine the names of the available attributes, and then use the results with the **getItemInfo** method.</span></span>

<span data-ttu-id="02a45-125">如需使用 Windows Media Player 物件方法來取得中繼資料的範例，請參閱 [attributeCount](playlist-attributecount.md)。</span><span class="sxs-lookup"><span data-stu-id="02a45-125">For an example of using Windows Media Player object methods to retrieve metadata, see [Playlist.attributeCount](playlist-attributecount.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02a45-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="02a45-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02a45-127">**建立中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="02a45-127">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="02a45-128">**中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="02a45-128">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="02a45-129">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="02a45-129">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




