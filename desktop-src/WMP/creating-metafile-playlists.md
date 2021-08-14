---
title: 建立中繼檔播放清單
description: 建立中繼檔播放清單
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Windows媒體中繼檔播放清單，建立
- 播放清單，建立
- 中繼檔播放清單，建立
- 建立 Windows 媒體中繼檔播放清單
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 765d8ab507c2ce502f1cad021696b0fc2ecfd110da8dfa95ccc84a43a8987561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750465"
---
# <a name="creating-metafile-playlists"></a>建立中繼檔播放清單

您可以使用任何文字編輯器（例如 Microsoft 記事本）來建立播放清單。 開啟您的文字編輯器。 輸入您想要執行的腳本專案。 完成輸入記事本之後，請以適當的檔案名和副檔名儲存檔案。 如需擴充功能的詳細資訊，請參閱 [中繼檔延伸指導方針](metafile-extension-guidelines.md)。 檔案名通常是 Windows 媒體檔案或資料流程的名稱，後面接著地板蠟、. 300k.wvx 或 .asx 的副檔名。 例如，如果您的媒體內容是副檔名為 .wma 的 Windows 媒體音訊檔案，則在命名播放清單時，請使用地板蠟副檔名。 播放清單不能包含文字處理器的任何格式設定代碼，例如 Microsoft Word。 若要確定播放清單中未包含任何格式設定代碼，請將檔案儲存為純文字或 ASCII 檔。

> [!Note]  
> 元素和屬性不區分大小寫。 播放清單中用來定義元素或屬性的文字可以是大寫或小寫，或是兩者的混合。

 

如果專案沒有任何子項目 (修改或包含在另一個專案) 中的專案，就可以在開頭標記的結尾處使用單一斜線字元 (/) ，而不是在 ' > ' 之前，用來取代結束記號。 專案的子項目必須出現在該元素的開頭和結束記號之間;否則這些專案不是該專案的子專案，而且會被忽略，或在播放清單的語法中造成錯誤。

播放清單的前四個字元必須是 " &lt; ASX"。 當所有播放清單中的地板蠟、. 300k.wvx 或 .asx 時，都使用了 **ASX** 元素。 每個播放清單必須只有一個 **ASX** 元素。 這個元素會將檔案識別為 Windows 媒體中繼檔播放清單。 它不會指定播放清單的類型。

**ASX** 元素有三個可能的屬性：

**VERSION**

**VERSION** 屬性是必要的，而且必須緊接在 **ASX** 元素之後，例如 "<asx VERSION =" 3.0 " &gt; "。 目前的版本號碼為3.0。 Windows Media Player 支援所有先前的版本。 **VERSION** 屬性可接受的值包括3.0 和 3 (，但) 不含小數點。

**PREVIEWMODE**

**PREVIEWMODE** 屬性是選擇性的。 它提供另一種機制來指定呈現剪輯的時間長度。 如果 [ **PREVIEWMODE** ] 屬性的值為 [是]，Windows Media Player 將會針對元素 **PREVIEWDURATION** 所指定的持續時間轉譯每個剪輯。 每個剪輯都可以指定 **PREVIEWDURATION** 。

**BANNERBAR**

選擇性的 **BANNERBAR** 屬性會定義 Windows Media Player 控制項是否保留橫幅圖形的空間。  (使用 **橫幅** 元素來指定要顯示的圖形。 ) 如果 **BANNERBAR** 的值是固定的，Windows Media Player 會保留顯示和每個剪輯的橫幅空間，無論中繼檔播放清單是否指定顯示或剪輯的橫幅。 這會將 Windows Media Player 視窗的大小保持不變，但不論是在影片大小變更) ，不論是否有橫幅圖形都不存在也 (一樣。 如果顯示或剪輯沒有相關聯的橫幅，保留給一個的空間會是黑色。 如果 [ **BANNERBAR** ] 屬性的值為 [自動]，Windows Media Player 只有在顯示或剪輯包含時，才會保留橫幅的空間。


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



如需有關 **asx** 元素之三個屬性的詳細資訊，請參閱 [asx 元素](asx-element.md)的參考專案。

**ASX** 元素包含 **專案** 子項目，可定義要存取之媒體檔案的相關資訊。 每個 **ENTRY 專案** 都必須包含 **REF** 元素，以指定要進行資料流程處理之媒體檔案的路徑。 **ASX** 元素中必須至少有一個 **專案** 或 **ENTRYREF** 元素。

在 **ASX** 元素範圍內定義的其他元素（例如 **標題** 和 **作者**）會與 Windows Media Player 所顯示的中繼資料相關聯。

最簡單的播放清單是藉由將具有單一 **REF** 專案的多個 **專案專案** 新增至中繼檔來建立。 中繼檔播放清單中的每個 **ENTRY 專案** 都會依照其出現的順序轉譯，如同使用者手動開啟每個剪輯一樣。

範例程式碼


```XML
<ASX version = "3.0">
<!--A simple playlist with entries to be played in sequence.-->
    <Title>The Show Title</Title>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title1.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title2.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title3.wma" />
    </Entry>
</ASX>

```



在 Windows 檔案總管中按兩下播放清單來確定播放清單是否正常運作。 Windows Media Player 應開啟並開始串流處理媒體內容。 確認播放清單正常運作之後，請將它連同網頁一起儲存到您的 web 伺服器，並透過 **HREF** 元素連結，或使用 Windows Media Player **物件** 專案將它內嵌在網頁中。

下列各節包含詳細資訊：

-   [嵌套中繼檔](nesting-metafiles.md)
-   [使用 ASP 頁面動態建立 Windows 媒體中繼檔播放清單](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**橫幅元素**](banner-element.md)
</dt> <dt>

[**範例播放清單**](example-playlists.md)
</dt> <dt>

[**Windows媒體中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows媒體中繼檔指南**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




