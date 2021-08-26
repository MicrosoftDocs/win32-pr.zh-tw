---
title: 基本播放清單
description: 基本播放清單
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
keywords:
- Windows媒體中繼檔播放清單、播放清單範例
- 播放清單、播放清單範例
- 中繼檔播放清單，播放清單範例
- Windows媒體中繼檔播放清單，範例播放清單
- 播放清單、範例播放清單
- 中繼檔播放清單，範例播放清單
- Windows媒體中繼檔播放清單、範例播放清單
- 播放清單、範例播放清單
- 中繼檔播放清單，範例播放清單
- Windows媒體中繼檔播放清單，程式碼範例
- 播放清單，程式碼範例
- 中繼檔播放清單，程式碼範例
- Windows媒體中繼檔播放清單，基本播放清單範例
- 播放清單、基本播放清單範例
- 中繼檔播放清單，基本播放清單範例
- Windows Media Player，播放清單範例
- Windows Media Player，範例播放清單
- Windows Media Player，範例播放清單
- Windows Media Player，基本播放清單範例
- 播放清單範例
- 範例播放清單
- 範例播放清單
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c8284acfe86cb204293902c0fb8664e74b12f3d2cc176d762f1aff079faac0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004578"
---
# <a name="a-basic-playlist"></a>基本播放清單

下列播放清單範例顯示一組基本的播放清單元素。 撰寫您自己的程式碼時，您必須將所有 Url 和檔案名變更為有效的檔案名，而您的 Windows Media Player 可以存取這些名稱。

**程式碼範例**


```XML
<ASX version = "3.0">
<TITLE>Basic Playlist Demo</TITLE>
    <ENTRY>
        <TITLE>An Entry in a basic playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <REF HREF = "mms://proseware.com/path/Yourfile.wma" />
    </ENTRY>
</ASX>

```



下表提供在範例程式碼中使用每個元素的詳細資料。



| 折線圖                                                                                            | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<ASX version = "3.0">                                                                     | [ASX](asx-element.md)元素會識別用戶端 (Windows Media Player) 這是 Windows 媒體中繼檔播放清單。 **Version** 屬性會指定中繼檔元素的版本號碼。                                                                                                                                                                                                                                                                                                                                           |
| \<TITLE>基本播放清單示範\</TITLE>                                                  | [Title](title-element--metafile.md)元素會識別播放清單的整體標題。 Windows Media Player 會將此中繼資料顯示為 [顯示標題]。                                                                                                                                                                                                                                                                                                                                                                                               |
| \<ENTRY>                                                                                   | 開始 [輸入](entry-element.md) 元素。 **ENTRY** 元素是在播放清單中定義特定剪輯的方式                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<TITLE>基本播放清單中的專案\</TITLE>                                         | 識別播放清單剪輯的標題。 它與先前的 **TITLE** 元素不同，因為這個專案是在 **專案專案** 內進行嵌套。 Windows Media Player 會將此中繼資料顯示為剪輯標題。                                                                                                                                                                                                                                                                                                                                         |
| \<AUTHOR>Microsoft Corporation\</AUTHOR>                                              | [Author](author-element.md)元素會識別 media 剪輯的作者。 Windows Media Player 會將此中繼資料顯示為剪輯 **作者**。                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<!-- This is a comment. Change the following path to point to your Windows media file --> | 註解。 只有在程式碼被查看，而且格式與 **XML** 批註相同時，才會顯示 [批註](comments.md)。                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \<REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | 媒體檔案的實際指標。 [REF](ref-element.md)元素會將該行識別為媒體內容的指標，而 **HREF** 屬性則是媒體檔案的 URL。 在此情況下，URL 會使用 MMS 通訊協定，因此會指向 Windows 媒體伺服器。媒體伺服器上的媒體檔案通常不會與您的 HTML 檔案保存在相同的位置。<br/> 請注意，使用類似 XML 的元素 "/>"，而不是 " &lt; /REF &gt; "。 因為這個元素沒有子專案，所以它會自行關閉。<br/> |
| \</ENTRY>                                                                                  | 指定 **ENTRY** 元素的結尾。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \</ASX>                                                                                    | 指定播放清單的結尾。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立中繼檔播放清單**](creating-metafile-playlists.md)
</dt> <dt>

[**範例播放清單**](example-playlists.md)
</dt> <dt>

[**中繼檔播放清單**](metafile-playlists.md)
</dt> <dt>

[**Windows媒體中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows媒體中繼檔指南**](windows-media-metafile-guide.md)
</dt> </dl>

 

 





