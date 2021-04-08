---
title: 使用自訂參數和命令
description: 使用自訂參數和命令
ms.assetid: 6b0bfd19-1672-41e3-9b7f-c8d541168c0e
keywords:
- Windows Media 中繼檔播放清單，自訂參數
- 播放清單，自訂參數
- 中繼檔播放清單，自訂參數
- Windows Media 中繼檔播放清單，自訂命令
- 播放清單，自訂命令
- 中繼檔播放清單，自訂命令
- Windows Media 中繼檔播放清單，參數
- 播放清單，參數
- 中繼檔播放清單，參數
- 自訂參數
- 自訂命令
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59f577fa4f3af71799b163389f85987d8723e045
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840211"
---
# <a name="using-custom-parameters-and-commands"></a><span data-ttu-id="3dbaf-114">使用自訂參數和命令</span><span class="sxs-lookup"><span data-stu-id="3dbaf-114">Using Custom Parameters and Commands</span></span>

<span data-ttu-id="3dbaf-115">您可以使用 **PARAM** 元素，建立自訂參數以傳遞中繼檔播放清單中的額外中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3dbaf-115">You can create custom parameters to pass additional metadata in a metafile playlist by using the **PARAM** element.</span></span> <span data-ttu-id="3dbaf-116">使用 **PARAM** 元素的 **NAME** 屬性來定義自訂參數名稱。</span><span class="sxs-lookup"><span data-stu-id="3dbaf-116">Use the **NAME** attribute of the **PARAM** element to define the custom parameter name.</span></span> <span data-ttu-id="3dbaf-117">您可以使用 **VALUE** 屬性來定義指名自訂參數的值。</span><span class="sxs-lookup"><span data-stu-id="3dbaf-117">Use the **VALUE** attribute to define the value for the named custom parameter.</span></span>

<span data-ttu-id="3dbaf-118">使用 **媒體** 和 **播放清單** 物件的 **getItemInfo** 方法來取出 **參數** 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3dbaf-118">Retrieve **PARAM** metadata by using the **getItemInfo** methods of the **Media** and **Playlist** objects.</span></span> <span data-ttu-id="3dbaf-119">如需使用這些方法來取出中繼資料的範例，請參閱 **播放清單** 物件的 [attributeCount](playlist-attributecount.md)方法。</span><span class="sxs-lookup"><span data-stu-id="3dbaf-119">For an example using these methods to retrieve metadata, see the [attributeCount](playlist-attributecount.md) method of the **Playlist** object.</span></span>

<span data-ttu-id="3dbaf-120">下列範例中繼檔播放清單顯示如何使用 **PARAM** 元素來定義自訂參數。</span><span class="sxs-lookup"><span data-stu-id="3dbaf-120">The following example metafile playlist shows the use of the **PARAM** element to define custom parameters.</span></span>


```XML
<ASX version="3.0" BANNERBAR="auto" >
    <TITLE>Example Media Player Show</TITLE>
    <PARAM NAME="Director" VALUE="Jane D." />

    <ENTRY>
        <TITLE>Example Clip</TITLE>
        <REF HREF="https://www.proseware.com/media.wma" />
        <PARAM NAME="Title" VALUE="Example Clip" />
        <PARAM NAME="Location" VALUE="North America" />
        <PARAM NAME="Release Date" VALUE="March 1998" />
    </ENTRY>

    <ENTRY>
        <TITLE>Another Clip</TITLE>
        <REF HREF="https://www.proseware.com/more_media.wma" />
        <PARAM NAME="Title" VALUE="Another Clip" />
        <PARAM NAME="Location" VALUE="Japan" />
        <PARAM NAME="Release Date" VALUE="December 2000" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="3dbaf-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="3dbaf-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dbaf-122">**使用中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="3dbaf-122">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




