---
title: 存取媒體
description: 存取媒體
ms.assetid: 18ea844d-98c9-4168-9af2-161dda52f6bd
keywords:
- Windows媒體中繼檔播放清單，存取媒體
- 播放清單，存取媒體
- 中繼檔播放清單，存取媒體
- Windows媒體中繼檔播放清單，媒體存取
- 播放清單，媒體存取
- 中繼檔播放清單，媒體存取
- Windows媒體中繼檔播放清單，控制播放
- 播放清單，控制播放
- 中繼檔播放清單，控制播放
- Windows媒體中繼檔播放清單，設定持續時間
- 播放清單，設定持續時間
- 中繼檔播放清單，設定持續時間
- Windows Media Player，存取媒體
- Windows Media Player，媒體存取
- Windows Media Player，控制播放
- Windows Media Player，設定持續時間
- 存取媒體
- 媒體存取
- 控制播放
- 設定持續時間
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c1a0846be4e8b9b62e424ce24d1b1800bc361c6a28f52a323c6bfa8511ae040b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956398"
---
# <a name="accessing-media"></a>存取媒體

使用播放清單來指定及控制 Windows Media Player 播放的串流媒體或媒體檔案。

您可以使用 **ENTRY 專案** 來指定單一媒體元件 (媒體檔案或即時資料流) 和任何子項目 (例如影像、 **MOREINFO** 連結和 **抽象** 文字) 。 使用 **ENTRYREF** 元素來指定播放清單。 播放清單可包含一或多個 **專案** 或 **ENTRYREF** 元素。 Windows Media Player 會從第一個專案開始，然後依序播放每個專案，直到清單完成為止，以執行播放清單。

**專案專案** 可以指向任何 Windows Media Player 可以播放的媒體類型。 這不僅包括 .wma、.wmv、.asf 和 .avi 檔案，還可以命名一些但即時資料流。 藉由使用一系列的專案或 **ENTRYREF** **專案** 來參考媒體內容，您可以使用播放清單來傳送由多個來源組成的單一資料流程。 參考的資料流程會依序播放，並由檢視器視為一個連續串流。 例如，播放清單可以包含兩個 **ENTRY** 元素：標準簡介從 Windows 媒體檔案副檔名為 .wma，以及即時 Windows 媒體串流。

> [!Note]  
> 播放清單不能包含媒體檔案的連結，這些媒體檔案的內容是使用不同版本的數位 Rights Management (DRM) 所建立。 在中繼檔播放清單中，如果有包含 drm 第1版內容的媒體檔案連結，以及以較新 drm 版本建立的媒體檔案的連結，Windows Media Player 只會播放 drm 第1版的內容。

 

## <a name="controlling-playback"></a>控制播放

使用播放清單來控制是否只播放播放的媒體剪輯，以及播放剪輯的哪些部分和操作方式。 您可以使用播放清單來定義要進行迴圈或重複的一組剪輯、設定播放的持續時間，以及指派開始時間和每個專案的開始和結束標記。 **STARTTIME**、 **STARTMARKER** 和 **ENDMARKER** 元素會與媒體檔案中的標記一起使用。

例如，下列播放清單會在一個 **專案** 中使用廣告橫幅和相關聯的 **MOREINFO** 連結，並參考 **STARTMARKER** 和 **ENDMARKER**。


```XML
<ASX version ="3.0">
<Title>Windows Media Example</Title>
<Abstract>Windows Media Technologies</Abstract>
<MoreInfo href = "https://www.proseware.com"/>
    <!--This is the first Entry -->
    <Entry>
        <Title>This is the ad</Title>
        <Author>Ad Department</Author>
        <Copyright>2000</Copyright>
        <Abstract>This is a description of the ad.</Abstract>
        <MoreInfo href = "https://www.proseware.com/"/>
        <Ref href="ad.wma"/>
        <Banner href ="purchase.gif">
           <Abstract>Click here to go to our website.</Abstract>
           <MoreInfo href = "https://www.litwareinc.com/" />
        </Banner>
     </Entry>        
    <!-- This is the second Entry -->
    <!-- The Windows Media file plays from Segment2 to Segment3 -->
    <Entry>
        <Title>Playlist Clip Number Two</Title>
        <Author>Windows Media</Author>
        <Copyright>2000</Copyright>
        <Ref href="show.wma"/>
        <StartMarker Name = "Segment2" />
        <EndMarker Name = "Segment3" />
    </Entry>
</ASX>

```



## <a name="setting-duration"></a>設定持續時間

您可以使用 **DURATION** 元素來指定播放剪輯或一組剪輯的時間長度。 您也可以搭配 **PREVIEWDURATION** 元素使用 **ASX** 元素的 **PREVIEWMODE** 屬性，以指定播放剪輯或一組剪輯的時間長度。 將 **PREVIEWMODE** 屬性設定為 [是]，即可使用 **PREVIEWDURATION** 元素指定播放相關剪輯的時間長度。 **PREVIEWDURATION** 和 **DURATION** 元素有相同的行為。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**中繼檔播放清單**](metafile-playlists.md)
</dt> <dt>

[**使用中繼檔播放清單**](using-metafile-playlists.md)
</dt> <dt>

[**Windows媒體中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows媒體中繼檔指南**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




