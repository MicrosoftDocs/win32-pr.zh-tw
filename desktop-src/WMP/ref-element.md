---
title: REF 元素
description: REF 元素會指定數位媒體內容的 URL。
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- REF 元素 Windows Media Player
topic_type:
- apiref
api_name:
- REF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 739ac61007e619055c28732c5c5aa763e84054fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995280"
---
# <a name="ref-element"></a>REF 元素

**REF** 元素會指定數位媒體內容的 URL。

``` syntax
<REF
   HREF = "URL"
>
</REF>
```

## <a name="attributes"></a>屬性

需要) **HREF** (

Windows Media Player 所支援的任何媒體內容的 URL。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| 父元素 | **進入**                                                                        |
| 子元素  | **DURATION**、 **ENDMARKER**、 **PREVIEWDURATION**、 **STARTMARKER**、 **STARTTIME** |



 

## <a name="remarks"></a>備註

這個元素會指定一段媒體內容的 URL。 URL 可以使用 Windows Media Player 所支援的任何通訊協定，指向任何支援的媒體類型。

支援的媒體類型包括仍為 .gif 和 .jpg 影像的影像，以及副檔名為 .gif 的 Flash 檔案。 這些媒體類型適用于將廣告內容包含在播放清單中。 使用迴圈中播放的影像檔案和 Flash 檔案，您也必須在 **REF** 元素中包含 **DURATION** 元素，以指定顯示媒體專案的時間量。 如果您想要在播放播放清單中的下一個專案時，繼續顯示影像，請在 **Entry 專案** 中包含 **PARAM** 元素、將其 **name** 屬性設定為 ShowWhileBuffering，然後將其 **value** 屬性設為 true。

若要參考 CD 或 DVD 上允許的內容，請提供 wmpcd 和 wmpdvd 通訊協定。 例如，將 **HREF** 屬性設定為 "wmpdvd://f/5/3" 將會播放 dvd 上的第3章，但只有在已撰寫 dvd 才能允許時。

如果使用功能變數名稱伺服器 (DNS) 名稱（而非 IP 位址）指定位址，則開啟媒體專案時，從防火牆後方開啟數位媒體的應用程式將會有較佳的效能。

此元素最常見的用法是用於 URL 變換。 如果 Windows Media Player 無法開啟 **REF** 元素中定義的媒體片段，它會嘗試下一個 **REF** 元素中的 URL。 一旦 Windows Media Player 從一個 **專案專案** 範圍內定義的 URL 開啟媒體內容，它就會忽略該 **entry 專案** 內的後續 **REF** 標記。 內容完成播放之後，Windows Media Player 移至下一個 **專案專案** （如果有的話）。

-   **重要** 一旦 Windows Media Player 建立與所參考內容片段的連接，它就會忽略該 **專案** 中的所有其他 **REF** 元素，不論連接是正常或異常地終止。

如果參考的媒體專案是影像檔案，則必須使用 **DURATION** 元素來指定影像的顯示時間。

**注意**

嘗試播放包含第一個框架音效的 Flash 媒體可能會產生非預期的結果。 您應該撰寫 Flash 內容，以在第二個畫面格開始時播放音效。

## <a name="examples"></a>範例


```XML
<ASX VERSION="3.0">
   <ENTRY>
   <TITLE>Example Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/selection1.asf" />
      <REF HREF="mms://sample.microsoft.com/mirror/selection1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**支援的通訊協定和檔案類型**](supported-protocols-and-file-types.md)
</dt> <dt>

[**Windows Media 中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media 中繼檔參考**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





