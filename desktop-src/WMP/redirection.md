---
title: 重新導向
description: 重新導向
ms.assetid: c8e3b43f-c11a-4ca7-b85c-038f0bfc3eb3
keywords:
- Windows Media 中繼檔播放清單，重新導向
- 播放清單，重新導向
- 中繼檔播放清單，重新導向
- Windows Media Player，重新導向
- 重新導向
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf1bb4d690c8aa6808e009a45a7bff1d6efada72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300164"
---
# <a name="redirection"></a>重新導向

播放清單會將瀏覽器重新導向至 Windows Media Player，以播放指定的媒體串流或媒體檔案。 最基本的中繼檔播放清單只包含媒體檔案 (URL) 的統一資源定位器。

若要建立基本的中繼檔播放清單，請開啟您慣用的文字編輯器（例如 Microsoft 記事本），然後輸入下列範例程式碼。


```XML
<ASX version="3.0">
   <ENTRY>
      <REF HREF="PathToYourFile"/>
   </ENTRY>
</ASX>

```



使用下表中的語法取代 Windows Media 檔案的有效路徑。



| 內容來源                                                                                 | Syntax                                    |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| 內容是 Windows Media 伺服器上的檔案                                                       | mms://ServerName/Path/FileName.wma        |
| 內容是從 Windows Media 站存取的廣播多播                    | https://WebServerName/Stations/kxyz.nsc    |
| 內容是從 Windows Media 伺服器上的發行端點存取的廣播單播 | mms://ServerName/PublishingPointAlias     |
| 內容是 web 伺服器上的檔案                                                                 | https://WebServerName/Path/Filename.wma    |
| 內容是本機硬碟上的檔案                                                            | file://c： \\ 路徑 \\ 檔案名 .wma             |
| 內容是網路共用上的檔案                                                              | file:// \\ \\ ServerName \\ 路徑 \\ 檔案名 .wma |
| 內容是 Windows Media 伺服器上的檔案                                                       | mms://ServerName/Path/FileName.wmv        |



 

使用 [[副檔名] 中所](file-name-extensions.md)述的檔案名和副檔名來儲存您所建立的檔案。 在 Windows 檔案總管中按兩下它。 Windows Media Player 應開啟並開始串流處理內容。 您可以將檔案連同網頁一起儲存至 web 伺服器，並使用 **HREF** 元素連結到該檔案，或使用 Windows Media Player **物件** 標記將它內嵌在網頁中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**中繼檔播放清單**](metafile-playlists.md)
</dt> <dt>

[**使用中繼檔播放清單**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Media 中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media 中繼檔指南**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




