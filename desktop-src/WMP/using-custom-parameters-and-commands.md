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
# <a name="using-custom-parameters-and-commands"></a>使用自訂參數和命令

您可以使用 **PARAM** 元素，建立自訂參數以傳遞中繼檔播放清單中的額外中繼資料。 使用 **PARAM** 元素的 **NAME** 屬性來定義自訂參數名稱。 您可以使用 **VALUE** 屬性來定義指名自訂參數的值。

使用 **媒體** 和 **播放清單** 物件的 **getItemInfo** 方法來取出 **參數** 中繼資料。 如需使用這些方法來取出中繼資料的範例，請參閱 **播放清單** 物件的 [attributeCount](playlist-attributecount.md)方法。

下列範例中繼檔播放清單顯示如何使用 **PARAM** 元素來定義自訂參數。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用中繼檔播放清單**](using-metafile-playlists.md)
</dt> </dl>

 

 




