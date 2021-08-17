---
title: MOREINFO 元素
description: MOREINFO 元素會指定與顯示、剪輯或橫幅相關聯之網站、電子郵件地址或指令碼命令的 URL。
ms.assetid: b817ef1d-4ca0-45f4-942b-695eaf537110
keywords:
- MOREINFO 元素 Windows Media Player
topic_type:
- apiref
api_name:
- MOREINFO Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 925783b6bd48fbc8b944d7b8fd2a2b94a9954c7036114145b99b015b90cbb6d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134951"
---
# <a name="moreinfo-element"></a>MOREINFO 元素

**MOREINFO** 元素會指定與顯示、剪輯或橫幅相關聯之網站、電子郵件地址或指令碼命令的 URL。

``` syntax
<MOREINFO
   HREF = "URL"
   TARGET = "Frame"
/>
```

## <a name="attributes"></a>屬性

需要) **HREF** (

網站、電子郵件地址或指令碼命令的 URL。

**目標**

值，定義瀏覽器將在其中開啟 **HREF** 屬性所定義之頁面的框架或視窗。

這可以是包含視窗名稱的字串，或下列其中一個值。



| 值    | 描述                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| \_空白  | 檔會在新的瀏覽器視窗中載入。                                                                              |
| \_自我   | 檔載入的框架與包含 Windows Media Player 控制項的目前檔相同。                |
| \_父母 | 檔會在目前框架的直屬父框架中載入，如果沒有父框架，則會載入目前的畫面格。 |
| \_top    | 檔會在完整的瀏覽器視窗中載入，取代所有其他的畫面格或檔。                                  |



 

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素                       |
|-----------------|--------------------------------|
| 父元素 | **ASX**、 **ENTRY**、 **橫幅** |
| 子元素  | 無                           |



 

## <a name="remarks"></a>備註

這個元素會指定網站、電子郵件地址 **或指令碼命令的 URL。使用者可以按一下與 MOREINFO 元素相關聯的圖形或文字，以存取 URL 的目標** 。 詳細資料取決於 **MOREINFO** 元素的父元素：

-   如果 **MOREINFO** 專案是 **ASX** 元素的子系，則使用者可以按一下 [顯示標題] 來存取 URL。
-   如果 **MOREINFO** **專案是專案專案** 的子系，則使用者可以按一下剪輯標題來存取 URL。
-   如果 **MOREINFO** 專案是 **橫幅** 元素的子系，則使用者可以按一下橫幅圖形來存取 URL。

如果 **HREF** 屬性指定網站的 url，瀏覽器會開啟並流覽至 url。 如果 **HREF** 屬性指定了電子郵件地址，則會啟動使用者的電子郵件應用程式。 如果 **HREF** 屬性指定了指令碼命令，則指令碼命令會在瀏覽器中執行。

**注意**

如果 **MOREINFO** 專案出現在 **Asx** 或 **ENTRY 專案** 中，則將滑鼠游標停留在 [ **asx** ] 元素的 [顯示 (的標題) 或針對 **專案**) 的 [剪輯 (]，就可以選取並使用 Windows Media Player 來存取 **HREF** 屬性中定義的 URL。

**目標** 屬性會定義瀏覽器將在其中開啟 **HREF** 屬性所定義之頁面的框架或視窗。 這個屬性的值會遵循標準 HTML 語法和定義。 在內嵌于網頁的控制項的案例中，如果未定義 **目標** 屬性，URL 會載入目前的瀏覽器視窗，並取代現有的頁面，這表示內容會停止播放。 因此，建議您在網頁中內嵌 Windows Media Player 控制項時，一律指定 **目標** 屬性。

如果中繼檔是在獨立 Windows Media Player 中開啟，則會忽略 **目標** 屬性，並在現有的瀏覽器視窗中載入 URL。 如果目前沒有開啟瀏覽器視窗，則會在新的瀏覽器視窗中載入 URL。

## <a name="examples"></a>範例


```XML
<ASX VERSION="3.0">

   <TITLE>Example Media Player Show</TITLE>
   <MOREINFO HREF="https://example.microsoft.com/info/show_info.htm" />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <MOREINFO HREF="https://example.microsoft.com/info/clip1_info.htm" />
      <REF HREF="mms://example.microsoft.com/media.asf" />
   </ENTRY>
   
</ASX>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------|
| 版本<br/> | Windows Media Player 70 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Windows媒體中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows媒體中繼檔參考**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





