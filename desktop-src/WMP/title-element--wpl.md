---
title: .WPL) 的 title 元素 (
description: Title 元素會指定播放清單的標題。
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- title 元素 (.WPL) Windows Media Player
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1de2679d5f78b48ceef569491ef21998fc13faf7126e61f76ad31959bdc2ac6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122778"
---
# <a name="title-element-wpl"></a>.WPL) 的 title 元素 (

**Title** 元素會指定播放清單的標題。

``` syntax
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```

## <a name="attributes"></a>屬性

這個元素沒有屬性。

## <a name="parentchild-elements"></a>父/子項目



| 階層 | 元素                 |
|-----------|--------------------------|
| 父代    | [頭](head-element.md) |
| 子系     | 無                     |



 

## <a name="remarks"></a>備註

選擇 Windows 媒體播放清單的標題 (.wpl) 時，請考慮播放清單的內容可以是動態的。 一個不錯的方法是以 **引數** 元素的邏輯作為標題，因為這是定義播放清單內容的專案。 這種情況的範例包括「我最愛的1966中的石頭」或「最近未玩過的 Dance 歌曲」。

## <a name="examples"></a>範例


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**引數元素**](argument-element.md)
</dt> <dt>

[**head 元素**](head-element.md)
</dt> <dt>

[**WindowsMedia 播放清單元素參考**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





