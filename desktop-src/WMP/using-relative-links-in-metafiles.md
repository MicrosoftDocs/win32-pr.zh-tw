---
title: 使用中繼檔中的相對連結
description: 使用中繼檔中的相對連結
ms.assetid: 8f6c40fc-e025-43d5-a43a-c162f28bbd71
keywords:
- Windows Media 中繼檔播放清單，相對連結
- 播放清單、相對連結
- 中繼檔播放清單、相對連結
- 中繼檔、相對連結
- Windows Media 中繼檔，相對連結
- relative links (相對連結)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9fe000ec071b0e54b9c6699a8a560ee4a26051
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839727"
---
# <a name="using-relative-links-in-metafiles"></a>使用中繼檔中的相對連結

相對連結是 Windows Media 中繼檔的完整支援功能。 您可以使用中繼檔中的相對連結，就像在 HTML 檔案中使用一樣。 使用相對連結可讓您建立可移植的中繼檔，也就是說，您可以將整個目錄結構複製或移動到另一部伺服器，而不需要更新用來作為橫幅的圖形檔案路徑或 **MOREINFO** 專案的 **HREF** 屬性 (如果它們參考與儲存的中繼檔) 相同的 web 伺服器上的檔案。 相對連結可在任何支援它們的應用程式中運作，因為未包含在專案之 **HREF** 屬性中的 url 部分，會包含在要求該 url 的應用程式傳送至伺服器的 url 中。 這表示通訊協定 (例如 HTTPs://) 、伺服器名稱，以及包含相對連結的檔案所在的虛擬目錄，全都包含在傳送至伺服器的 URL 中。 如果您使用相對連結連結到的媒體檔案或 URL 與中繼檔不位於相同的伺服器上，相對連結就會無效。

> [!Note]  
> 只有在使用獨立 Windows Media Player 中開啟之中繼檔的連結時，相關連結上的這項資訊才是正確的。 當您使用內嵌的 Windows Media Player 控制項時，所有連結都會相對於裝載控制項的頁面，除非使用 **ASX** 元素的 **基底** 子項目來重新導向相對路徑。

 

中繼檔中的所有相對連結都必須是串流媒體的完全相對，而不是相對於磁片磁碟機。 當 URL 的開頭為 " \\ " 字元時，連結會相對於磁片磁碟機。 Windows Media Player 嘗試在開啟中繼檔的磁片磁碟機上開啟連結的檔案，通常是 web 伺服器。 由於 web 伺服器使用虛擬目錄，Windows Media Player 嘗試在開啟中繼檔的 web 伺服器上，于虛擬目錄的子目錄中尋找指定的資料流程或媒體檔案。 使用者無法存取伺服器目錄。 本章節中的範例說明如何使用完整的相對連結。

當您在單一電腦上使用中繼檔時，可以使用磁片磁碟機相對連結，而中繼檔播放清單中連結的所有媒體檔案都存在於該電腦的儲存裝置上。 不過，您無法以這種方式串流媒體。

當您使用另一個中繼檔的連結來允許相對連結時，依 Windows Media Player 顯示的名稱會是原始中繼檔中的標題。

相對連結無法用於串流處理媒體伺服器的 Url，因為使用不同的通訊協定來存取串流媒體內容。

在下列範例播放清單中，第一個 **ENTRYREF** 包含另一個播放清單的 URL，相對. 地板蠟。


```XML
<ASX>
    <ENTRYREF HREF="https://example.microsoft.com/metafiles/relative.wax"/>
</ASX>

```



下列範例是地板蠟檔案，其中包含相對連結。


```XML
<ASX version = "3.0">
    <BANNER HREF = "graphics/logo1.jpg">
        <MOREINFO HREF = "category1/category1.htm" />
    </BANNER>
    <ENTRY>
        <REF HREF = "mms://samples.microsoft.com/myfile.wma" />
    </ENTRY>
</ASX>

```



包含播放清單地板蠟參考的 URL 可以存在於使用者可存取的中繼檔播放清單中。 若要成功處理 URL，必須有一個名為 "example.microsoft.com" 的 web 伺服器。 該網頁伺服器必須有定義為「中繼檔」的虛擬目錄。 參照的播放清單地板蠟必須存在於虛擬目錄 "中繼檔" 中名為 "example.microsoft.com" 的 web 伺服器上。

如果要成功存取和播放播放清單中的參考媒體檔案，必須有一個名為 "Graphics" 的目錄，這是伺服器的虛擬目錄 "中繼檔" 的子目錄。 **橫幅** 元素中所參考的圖形檔案 Logo1.jpg 必須是名為 graphics 的子目錄。

同樣地，名為 Category1.htm 的檔必須位於名為 Category1 的子目錄中。 名為 Category1 的目錄必須以子目錄形式存在於 web 伺服器 example.microsoft.com 上的虛擬目錄「中繼檔」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立中繼檔播放清單**](creating-metafile-playlists.md)
</dt> <dt>

[**中繼檔播放清單**](metafile-playlists.md)
</dt> <dt>

[**Windows Media 中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media 中繼檔指南**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




