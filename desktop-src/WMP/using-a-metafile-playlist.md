---
title: 使用中繼檔播放清單
description: 使用中繼檔播放清單
ms.assetid: e6cbdb76-4405-409e-93c3-38a3baa7c231
keywords:
- Windows Media 中繼檔播放清單，使用
- 中繼檔播放清單，使用
- 播放清單，使用
- Windows Media 中繼檔播放清單，關於
- 中繼檔播放清單，關於
- 播放清單，關於
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5f1832c0c739874fbbd4db219f2c622fc2debfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672767"
---
# <a name="using-a-metafile-playlist"></a>使用中繼檔播放清單

由於您無法直接從網頁連結到串流媒體伺服器，因此您可以使用中繼檔播放清單。 中繼檔播放清單包含 Windows Media Player 所需的資訊，而且會儲存在 web 伺服器上。 然後，您可以從 Web 檔連結到中繼檔播放清單。 開啟中繼檔播放清單時，會將控制項傳輸至 Windows Media Player，以處理檔案、連線至串流處理媒體伺服器，並播放指定的內容。

瀏覽器會先將中繼檔播放清單下載到使用者的快取目錄。 因為中繼檔播放清單很小，所以這是非常快速的步驟。 使用者的電腦接著會在其 [檔案關聯] 資料表中找到與 Windows Media Player 的中繼檔播放清單關聯。 Windows Media Player 會開啟並解釋中繼檔播放清單中的腳本，其中包含串流內容的 URL，還有其他專案。 Windows Media Player 會使用 URL 來找出內容並起始資料流程。 中繼檔播放清單腳本接著會控制串流體驗。

因為中繼檔播放清單會透過與 ASXMIME 類型相關聯的協助程式應用程式運作， (application/mplayer2 或 video/x--------) -------- 本檔中顯示的範例適用于 Microsoft Internet Explorer 4.0 和更新版本，以及 Microsoft Win32®和 Apple Macintosh 平臺上的 Netscape Navigator 4.0 和更新版本。 在所有範例中，您都必須確定參考的任何數位媒體檔案都具有有效的環境路徑和檔案名。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Windows Media 中繼檔指南**](windows-media-metafile-guide.md)
</dt> <dt>

[**Windows Media 中繼檔參考**](windows-media-metafile-reference.md)
</dt> <dt>

[**Windows Media 中繼檔總覽**](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




