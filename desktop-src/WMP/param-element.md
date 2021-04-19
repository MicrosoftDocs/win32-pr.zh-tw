---
title: " (WMP SDK) 的 PARAM 元素"
description: PARAM 元素會定義與播放清單或播放清單元素相關聯的自訂參數。
ms.assetid: d905a42a-ac89-4c99-94ca-b3b7060ebbdc
keywords:
- PARAM 元素 Windows Media Player
topic_type:
- apiref
api_name:
- PARAM Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7879f9dc9a8cf31afee5a3f1684af5cba33a9e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979564"
---
# <a name="param-element"></a>PARAM 元素

**PARAM** 元素會定義與播放清單或播放清單元素相關聯的自訂參數。

``` syntax
<PARAM
   NAME = "parameter name"
   VALUE = "parameter value"
/>
```

## <a name="parameters"></a>參數

參數也可以與顯示相關聯，而不是個別的剪輯，方法是將這個專案直接放在 **.asx** 標記之後。 這些專案是由其名稱和開頭為零的索引值所參考。

> [!Note]  
> 此 **ASX** 元素僅適用于 Windows Media Player 6.01 版和更新版本。 Microsoft Internet Explorer 5 的標準安裝包含相容的 Windows Media Player 版本。

 

## <a name="attributes"></a>屬性

**名稱**

用來存取參數值的名稱。 名稱可以是任何有效的字串。 已定義下列字串。



| String                          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowShuffle                    | **VALUE** 屬性會指定中繼檔播放清單是否允許 Windows Media Player 隨機播放的功能，以隨機順序播放專案。 **VALUE** 屬性可以設定為 "Yes" 或 "No"。 預設值為 "No"。                                                                                                                                                                                                                                                                                                                                                                  |
| CanPause                        | **VALUE** 屬性會指定使用者是否可以暫停播放。 **VALUE** 屬性可以設定為 "Yes" 或 "No"。 預設值為 [是]。                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CanSeek                         | **VALUE** 屬性會指定使用者是否可以使用搜尋列、向前快轉或快速反轉，來變更目前的播放位置。 **VALUE** 屬性可以設定為 "Yes" 或 "No"。 預設值為 [是]。                                                                                                                                                                                                                                                                                                                                                                    |
| CanSkipBack                     | **VALUE** 屬性會指定使用者是否可以按一下 [**上一步**]，跳到上一個播放清單專案。 **VALUE** 屬性可以設定為 "Yes" 或 "No"。 預設值為 [是]。                                                                                                                                                                                                                                                                                                                                                                                         |
| CanSkipForward                  | **值** 屬性指定使用者是否可以按一下 **[下一步]**，跳到下一個播放清單專案。 **VALUE** 屬性可以設定為 "Yes" 或 "No"。 預設值為 [是]。                                                                                                                                                                                                                                                                                                                                                                                                  |
| CPRadioID                       | **VALUE** 屬性會指定由類型1線上商店提供的收音機摘要識別碼。 也就是說， **VALUE** 屬性必須等於線上商店目錄中其中一個收音機摘要的 RadioID 欄位。 父元素是 **ASX** 元素。                                                                                                                                                                                                                                                                                                                                   |
| 編碼                        | **VALUE** 屬性會設定為 "utf-8"，表示中繼檔是 UNICODE (utf-8) 編碼的檔案。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| HtmlFlink                       | **值** 屬性是類型1線上商店所提供的字串。 Windows Media Player 將字串傳遞至 [IWMPContentPartner：： GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) 方法，該方法是由線上商店的外掛程式所執行。 **GetItemInfo** 方法會傳回要在播放程式的 [**現正播放**] 窗格中顯示的網頁 URL。 網頁可以存取 **外部** 物件所公開的所有方法，以鍵入1個存放區。 如需這些方法的清單，請參閱 [類型1線上商店的外部物件](external-object-for-type-1-online-stores.md)。 |
| HTMLView                        | **值** 屬性指定 URL，此 URL 會根據父項目為 **ASX** 元素或 **entry 專案**，在播放清單或目前專案的完整模式播放程式的 [**立即播放**] 窗格中顯示。 Windows Media Player 控制項不支援 HTMLView。                                                                                                                                                                                                                                                                               |
| 記錄：*FieldName* \[ ：*NameSpace*\] | **Value** 屬性會指定指定的記錄欄位將設定為的值。 **NAME** 屬性的：*命名空間* 部分是選擇性的。                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Prebuffer                       | **VALUE** 屬性會指定下一個播放清單專案是否會在目前專案的結尾之前開始緩衝處理，這樣可讓您順暢地轉換。 **VALUE** 屬性可以設定為 "true" 或 "false"。                                                                                                                                                                                                                                                                                                                                                                                 |
| ShowWhileBuffering              | **VALUE** 屬性會指定目前 **專案專案** 所參考的影像檔，是否會在下次播放播放清單專案時，繼續顯示超過指定的時間長度。 **VALUE** 屬性可以設定為 "true" 或 "false"。                                                                                                                                                                                                                                                                                                                                         |



 

**VALUE**

與此參數相關聯的值。 可以是數值或字串值。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素           |
|-----------------|--------------------|
| 父元素 | **ASX**， **進入** |
| 子元素  | 無               |



 

## <a name="remarks"></a>備註

此元素可讓使用者在包含它的 **ENTRY 專案** 內，放置每個剪輯的其他相關資訊。 若要取出播放清單 **專案** 中指定的中繼資料資訊，請使用 *媒體*。**getItemInfo** 方法。 *媒體*。**getItemInfo** 方法會在指定參數名稱的情況下，取得 **value** 屬性的值。 舊版 Windows Media Player 會使用 **GetMediaParameter** 方法來取得播放清單 **專案** 中指定的中繼資料資訊，並使用指定的參數名稱和專案的索引編號。

參數也可以與顯示相關聯，而不是個別的剪輯，方法是將這個專案直接放在 **.asx** 標記之後。 這些專案是由其名稱和開頭為零的索引值所參考。

**注意**

此 **ASX** 元素僅適用于 Windows Media Player 6.01 版和更新版本。 Microsoft Internet Explorer 5 的標準安裝包含相容的 Windows Media Player 版本。

## <a name="examples"></a>範例


```XML
<ASX VERSION="3.0">
   <TITLE>Example Media Player Show</TITLE>
   <PARAM NAME="Director" VALUE="Jane D." />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/media.asf" />
      <PARAM NAME="Location" VALUE="North America" />
      <PARAM NAME="Release Date" VALUE="March 1998" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/more_media.asf" />
      <PARAM NAME="Location" VALUE="Japan">
      <PARAM NAME="Release Date" VALUE="December 1996" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本，預先定義的名稱屬性需要 Windows Media Player 9 系列或更新版本，預先定義的名稱屬性需要 Windows Media Player 10 或更新版本 CanPause、CanSeek、CanSkipBack 和 CanSkipForward<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**顯示 Windows Media Player 中的網頁**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**記錄資料流程資料**](logging-stream-data.md)
</dt> <dt>

[**Windows Media 中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media 中繼檔參考**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





