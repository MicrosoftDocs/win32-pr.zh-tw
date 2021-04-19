---
title: 基底元素
description: 基底元素會定義附加至傳送給 Windows Media Player 的 Url 前面的 URL 字串。
ms.assetid: 887cf860-d06e-44a1-b729-28a285f6c7d3
keywords:
- 基底元素 Windows Media Player
topic_type:
- apiref
api_name:
- BASE Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44b62a24f73ed6cf78820efe1ca76e0eccd3fb59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999444"
---
# <a name="base-element"></a>基底元素

**基底** 元素會定義附加至傳送給 Windows Media Player 的 url 前面的 url 字串。

``` syntax
<BASE
   HREF = "URL"
/>
```

## <a name="attributes"></a>屬性

需要) **HREF** (

附加至傳送給 Windows Media Player 之 Url 前面的字串。 預設值為 null 字串 ( "" ) 。

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素           |
|-----------------|--------------------|
| 父元素 | **ASX**， **進入** |
| 子元素  | 無               |



 

## <a name="remarks"></a>備註

此元素會定義 URL 字串，並附加至傳送至 Windows Media Player 的 URL 反向 Url 前面。 URL 翻轉是一種腳本機制，可讓 Windows Media Player 在瀏覽器或瀏覽器框架收到指令碼命令時，開啟新的 URL。

**基底** 元素類似于相對連結的主目錄。 它只會影響使用指令碼命令傳送的 Url，做為 Windows Media Player 中播放之內容資料流程的一部分。

定義為 **ASX** 元素子系的 **基底** 元素會變成整個中繼檔的預設值。 **專案專案** 中所定義的 **基底** 元素，會覆寫父 **ASX** 元素中的任何 **基底** 元素， (僅) 該 **entry 專案**。

> [!Note]  
> 如果 **HREF** 屬性不是以/字元結尾，Windows Media Player 會將其中一個字元附加至字串結尾。

 

## <a name="examples"></a>範例


```XML
<BASE HREF="https://msdn.microsoft.com/" />

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Windows Media 中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media 中繼檔參考**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





