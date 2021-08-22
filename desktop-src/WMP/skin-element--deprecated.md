---
title: " (已淘汰的面板元素) "
description: 本頁記載了未來版本的 Windows Media Player 和 Windows Media Player SDK 可能無法使用的功能。
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- 面板元素 (已淘汰的) Windows Media Player
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b868b756ed190301c66987b6e26249762bac71842f4a5425d6d7c6d4b16816a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507908"
---
# <a name="skin-element-deprecated"></a> (已淘汰的面板元素) 

本頁記載了未來版本的 Windows Media Player 和 Windows Media Player SDK 可能無法使用的功能。

面板 **元素會** 指定框線的 URL。

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a>屬性

需要) **HREF** (

副檔名為 wmz 之壓縮框線檔的 URL。 針對 Windows Media Player 9 系列或更新版本，此值只能參考使用者硬碟上與中繼檔播放清單相同的框線檔。 請參閱範例程式碼。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素 |
|-----------------|----------|
| 父元素 | **.ASX**  |
| 子元素  | 無     |



 

## <a name="remarks"></a>備註

面板 **元素用** 來建立框線，類似于面板，但會顯示在完整模式 Windows Media Player 的 [**立即播放**] 區域中。 面板 **元素只** 適用于框線，這會出現在完整模式 Windows Media Player 中，而不適用於一般的面板，這會完全取代 Windows Media Player 的 compact 模式。

在 Windows 媒體下載套件 () 副檔名為 wmd 的情況下，**面板元素可** 讓框線具有內容，並連結至其他網站。 Windows 媒體下載套件是壓縮檔案，其中包含 border 檔案和 Windows 媒體中繼檔。 副檔名為 wmz 的框線檔 () 會壓縮，並且包含具有 wms 副檔名) 的外觀 (定義檔。

**外觀** 元素有三個元件：

-   外觀
-   部分內容
-   中繼檔

Windows 媒體下載套件隨附的面板必須是圖形中的矩形。 使用非矩形的外觀建立框線可能會產生非預期的結果。

## <a name="examples"></a>範例


```XML
<ASX version = "3.0">
    <TITLE>A Skin Element</TITLE>
    <SKIN HREF = "YourTest.wmz" />

    <ENTRY>
        <PARAM name="YourAlbumTitle" value="YourTitle.jpg"/>
        <PARAM name="link" value="https://www.proseware.com"/>
        <TITLE>(The Artist)-YourTitle</TITLE>
        <REF HREF="(The Artist)-YourSongTitle.wma"/>
    </ENTRY>

</ASX>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------|
| 版本<br/> | Windows Media Player 70 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Windows Media Player (已淘汰) 的框線**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Windows媒體中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows媒體中繼檔參考**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





