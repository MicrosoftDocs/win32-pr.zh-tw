---
title: ENTRY 元素
description: ENTRY 元素會指定要轉譯為剪輯的 Windows Media 檔案。
ms.assetid: 7fd16aff-2eed-4f95-92b3-b48a9d785e7c
keywords:
- ENTRY 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ENTRY Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13da18c72022c916f91bcffe7382f673ba3d4fa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984880"
---
# <a name="entry-element"></a>ENTRY 元素

**ENTRY** 元素會指定要轉譯為剪輯的 Windows Media 檔案。

``` syntax
<ENTRY
   CLIENTSKIP = "YES" | "NO"
   SKIPIFREF = "YES" | "NO"
>
</ENTRY>
```

## <a name="attributes"></a>屬性

**CLIENTSKIP**

值，指出使用者是否可以向前跳過剪輯。

可能的值如下。



| 值 | 描述                                   |
|-------|-----------------------------------------------|
| YES   | 預設值。 使用者可以跳過剪輯之後的向前跳過。 |
| 否    | 使用者無法向前跳過剪輯。       |



 

**SKIPIFREF**

值，指出當 **ENTRY 專案** 透過使用 **ENTRYREF** 元素包含在第二個中繼檔中時，Windows Media Player 是否應略過此剪輯。

可能的值如下。



| 值 | 描述                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| YES   | 如果透過 **ENTRYREF** 元素參考，Windows Media Player 將會忽略此專案。 |
| 否    | 預設值。 Windows Media Player 不會忽略此專案。                                   |



 

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素                                                                                                                                                                                     |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 父元素 | **ASX**、 **事件**、 **重複**                                                                                                                                                               |
| 子元素  | **ABSTRACT**、 **AUTHOR**、 **橫幅**、 **BASE**、 **著作權**、 **DURATION**、 **ENDMARKER**、 **MOREINFO**、 **PARAM**、 **PREVIEWDURATION**、 **REF**、 **STARTMARKER**、 **STARTTIME**、 **TITLE** |



 

## <a name="remarks"></a>備註

此元素是 Windows Media 中繼檔中的基礎結構。 **ENTRY 專案** 和其相關聯的屬性會定義單一邏輯內容片段的中繼資訊，稱為「剪輯」。 **專案專案** 範圍內的子專案會定義 Windows Media Player 的媒體內容以開啟 (**REF**) 、Windows Media Player 會顯示為文字的剪輯相關資訊 (**作者**、**著作權**、**標題**) ，以及其他與剪輯相關的設定。 **REF** 子項目會連結要針對父項目 **專案** 進行資料流程處理的內容。 雖然腳本不會中斷，但在沒有 **REF** 子系的情況下，**專案** 沒有意義。

如果 [ **CLIENTSKIP** ] 屬性的值為 [否]，使用者就無法向前跳過 **專案專案** 所定義的內容片段。 如果子系 **REF** 元素參考另一個中繼檔，則無法使用。 應該使用 **ENTRYREF** 元素參考嵌套的中繼檔。

**SKIPIFREF** 屬性僅適用于透過使用 **ENTRYREF** 專案所包含在第二個中繼檔中的 **專案專案**。 **ENTRYREF** 元素會參考另一個中繼檔，以便在目前的檔案中包含邏輯。 如果所參考之中繼檔中 **專案專案** 的 **SKIPIFREF** 屬性值為 YES，Windows Media Player 會忽略此提取專案，並移至下一個 **專案** 專案（如果有的話）。 下一個 **專案** 專案可以是原始檔案中的下一個專案，或是 **ENTRYREF** 元素所參考之中繼檔中的下一個專案。

## <a name="examples"></a>範例


```XML
<ASX VERSION="3.0">
   <TITLE>Example Windows Media Player Show</TITLE>
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://example.microsoft.com/media.asf" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://example.microsoft.com/more_media.asf" />
   </ENTRY>
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

 

 





