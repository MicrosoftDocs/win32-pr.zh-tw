---
title: ASX 元素
description: ASX 元素會將檔案定義為中繼檔。
ms.assetid: 130220a0-959c-4c13-aa7d-06b6bbebc9cc
keywords:
- ASX 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ASX Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b77cb6c379319c97377b2a3953a9f8fd86b65938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983155"
---
# <a name="asx-element"></a>ASX 元素

**ASX** 元素會將檔案定義為中繼檔。

``` syntax
<ASX
   VERSION = "number"
   PREVIEWMODE = "YES" | "NO"
   BANNERBAR = "AUTO" | "FIXED"
>
</ASX>
```

## <a name="attributes"></a>屬性

`VERSION` (必要)

十進位數，代表中繼檔的語法版本號碼。 設定為3或3.0。

**PREVIEWMODE** (選用) 

值，指出在播放第一個剪輯之前 Windows Media Player 是否進入預覽模式。

必須是下列其中一個值。



| 值 | 描述                                                                                        |
|-------|----------------------------------------------------------------------------------------------------|
| YES   | Windows Media Player 在播放第一個剪輯之前進入預覽模式。                            |
| 否    | 預設值。 在播放第一個剪輯之前，Windows Media Player 不會進入預覽模式。 |



 

**BANNERBAR** (選用) 

值，指出 Windows Media Player 是否保留橫幅圖形的空間。

必須是下列其中一個值。



| 值 | 描述                                                                                                                                |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| AUTO  | 預設值。 Windows Media Player 只有在內容包含一段內容時，才會保留橫幅列的空間。                       |
| FIXED | Windows Media Player 會針對每個播放的內容保留一個固定的空間，而不論是否有相關聯的橫幅。 |



 

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素                                                                                                                                                               |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 父元素 | 無。 **ASX** 元素必須是每個中繼檔中的第一個元素。                                                                                                 |
| 子元素  | **ABSTRACT**、 **AUTHOR**、 **橫幅**、 **BASE**、 **著作權**、 **ENTRY**、 **ENTRYREF**、 **EVENT**、 **MOREINFO**、 **PREVIEWDURATION**、 **PARAM**、 **REPEAT**、 **TITLE** |



 

## <a name="remarks"></a>備註

中繼檔播放清單的前四個字元必須是 "<ASX"。 在 **ASX** 元素範圍內定義的其他元素（例如 **標題** 和 **作者**）會與 Windows Media Player 所顯示的顯示資訊相關聯。

針對 Windows Media Player，語法版本號碼為3.0。 Windows Media Player 支援所有舊版的中繼檔語法。 **VERSION** 屬性可接受的值包括3.0 和 3 (，但) 不含小數點。

如果 **PREVIEWMODE** 屬性的值為 YES，Windows Media Player 在播放第一個剪輯之前立即進入預覽模式。 當 Windows Media Player 進入預覽模式時，它會預覽中繼檔中所參考的每個剪輯。 **PREVIEWDURATION** 元素決定每個預覽的持續時間。

**BANNERBAR** 屬性會定義 Windows Media Player 是否保留橫幅圖形的空間。 橫幅是媒體內容播放時，顯示在影片顯示區域中的圖形。  (使用 **橫幅** 專案將橫幅新增至內容。 ) 如果 **BANNERBAR** 的值是固定的，Windows Media Player 會針對媒體內容的每個部分保留橫幅空間，不論媒體內容是否有橫幅。 如果媒體內容沒有相關聯的橫幅，保留給一個的空間會是黑色。 如果 [ **BANNERBAR** ] 屬性的值為 [自動]，Windows Media Player 只有當媒體內容包含時，才會保留橫幅的空間。

如果您建立具有多個剪輯的中繼檔 (專案或 **ENTRYREF** **專案**) ，並將 [ **BANNERBAR** ] 屬性的值設定為 [自動]，Windows Media Player 可能會調整大小以允許一個剪輯的橫幅圖形出現空間，然後在下一個剪輯未包含橫幅圖形時再調整大小。 如果您想要讓視窗的大小維持相同的 (但) 的影片大小變更時，請使用 **BANNERBAR** 屬性的固定值。

針對橫幅圖形所保留的空間為32圖元高、194圖元寬。 保留的空間會出現在影片區域下方任何轉譯的影片內容和6圖元上方，讓6圖元的視頻區域框線具有空格。 保留的橫幅空間會以水準方式置中。

Windows Media Player 會以橫幅空間最左邊的圖元開始呈現圖形。 如果圖形填滿整個空間，則會以水準方式顯示。 否則將會有尾端的空格。 請注意，不論 **BANNERBAR** 屬性的值為何，Windows Media Player 的最小寬度一律會比影片剪輯的大小更寬。

## <a name="examples"></a>範例


```XML
<ASX VERSION="3.0" PREVIEWMODE="YES" BANNERBAR="auto"  >
   <ENTRY HREF="https://sample.microsoft.com/sample1.ASX" />
</ASX>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------|
| 版本<br/> | Windows Media Player 70 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Windows Media 中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media 中繼檔參考**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





