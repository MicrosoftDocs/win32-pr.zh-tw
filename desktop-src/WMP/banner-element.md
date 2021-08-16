---
title: 橫幅元素
description: 橫幅元素會定義要出現在顯示面板中之圖形檔案的 URL。
ms.assetid: 8b4a3369-a687-40a8-b5df-afb0e0518cd1
keywords:
- 橫幅元素 Windows Media Player
topic_type:
- apiref
api_name:
- BANNER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91b3de50c1360337c1344a1af1a0696361614dbc293390470e7c196e53528a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135961"
---
# <a name="banner-element"></a>橫幅元素

**橫幅** 元素會定義要出現在顯示面板中之圖形檔案的 URL。

``` syntax
<BANNER
   HREF = "URL"
>
</BANNER>
```

## <a name="attributes"></a>屬性

需要) **HREF** (

顯示面板中顯示之圖形檔案的 URL。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素                   |
|-----------------|----------------------------|
| 父元素 | **ASX**， **進入**         |
| 子元素  | **ABSTRACT**、 **MOREINFO** |



 

## <a name="remarks"></a>備註

此元素會定義顯示在影片內容下方 Windows Media Player 顯示面板中的圖形檔案的 URL。 如果媒體只是音訊，則會顯示橫幅圖形。 Windows Media Player 會在圖形的橫幅橫條圖) 中保留空間32圖元高、194圖元寬 (。 如果在 URL 中定義的圖形小於該圖形，則會顯示其原始大小。 如果圖形大於保留空間，Windows Media Player 將會裁剪影像以符合空間。

您可以使用 **橫幅** 元素範圍內的 **抽象** 專案，在使用者將滑鼠指標暫停在橫幅圖形上時，將文字顯示為工具提示。 **橫幅** 元素內的 **MOREINFO** 專案會定義使用者按一下橫幅圖形時，使用者所使用的 URL。  (URL 可以是任何路徑或通訊協定，例如電子郵件連結、超文字傳輸通訊協定 (網站的 HTTP) URL，甚至是 Microsoft JScript 命令 ) 。當指標移到圖形上時，圖形會變成浮凸效果，並看起來像按鈕。

當播放清單中的所有剪輯都在播放時，會顯示為 **ASX** 元素定義的 **橫幅** 元素。 在 **專案專案** 中定義的 **橫幅** 元素只會在播放剪輯時顯示，而在這段期間，會覆寫父 **ASX** 元素內定義的任何橫幅。 您可以藉由設定 **ASX** 專案的 **BANNERBAR** 屬性，來指定 Windows Media Player 如何保留橫幅的空間。

使用 DRM 檔案時，或在網頁中內嵌 Windows Media Player 時，不支援橫幅影像。

## <a name="examples"></a>範例

以下是沒有子項目的 **橫幅** 元素範例：


```XML
<BANNER HREF="https://sample.microsoft.com/art/banner1.bmp" />
```



以下是包含 **抽象** 和 **MOREINFO** 專案的 **橫幅** 元素範例。


```XML
<BANNER HREF="https://www.proseware.com/logos/banner1.bmp">
    <ABSTRACT>Click here to go to our website.</ABSTRACT>
    <MOREINFO HREF="https://sample.microsoft.com" />
    <!-- The text in the Abstract element displays as a 
         ToolTip when the mouse hovers over the banner 
         graphic. When a user clicks the banner, the URL 
         given in the MoreInfo element opens in the 
         browser. -->
</BANNER>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Windows媒體中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows媒體中繼檔參考**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





