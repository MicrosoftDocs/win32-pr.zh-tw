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
# <a name="retrieving-metadata"></a>擷取中繼資料

當播放顯示或剪輯時，您的腳本可以使用 Windows Media Player **媒體** 和 **播放清單** 物件的 **getItemInfo** 方法，來取得中繼資料（例如標題和作者）。 您可以使用 **播放清單** 物件方法，以及從專案範圍使用 **媒體** 物件方法，從 ASX 範圍取得中繼資料。

例如，若要在下列檔案中取出 AUTHOR、ABSTRACT 和 PARAM 的值，請使用 **播放清單** 物件的 **getItemInfo** 方法。 此方法需要屬性名稱。 藉由提供索引編號給 **attributeName** 屬性，即可取得屬性名稱。 您可以使用 **attributeCount** 屬性來取得 **播放清單** 物件的可用索引。

## <a name="example-code"></a>範例程式碼


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



若要在 REF、TITLE、著作權和 PARAM 的專案範圍中取出目前 **媒體** 物件的值 ( "三" ) ，請使用 **Player** 物件的 **currentMedia** 屬性。 使用 **媒體** 物件的 **attributeCount** 屬性，來判斷指定之 **媒體** 物件的可用屬性數目。 使用 **getItemInfoByAtom** 方法的索引編號來取出屬性值。 使用具有 **媒體** 物件之 **getAttributeName** 方法的索引編號來判斷可用屬性的名稱，然後使用 **getItemInfo** 方法的結果。

如需使用 Windows Media Player 物件方法來取得中繼資料的範例，請參閱 [attributeCount](playlist-attributecount.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立中繼檔播放清單**](creating-metafile-playlists.md)
</dt> <dt>

[**中繼檔播放清單**](metafile-playlists.md)
</dt> <dt>

[**Windows Media 中繼檔指南**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




