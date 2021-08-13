---
title: 中繼元素
description: 中繼元素會指定適用于整個播放清單的中繼資料。
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- 中繼元素 Windows Media Player
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b2e4120b3eceea6d2a664edec9b48a46d33ad19b788bb820458a8802dccd2d9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415738"
---
# <a name="meta-element"></a>中繼元素

**中繼** 元素會指定適用于整個播放清單的中繼資料。

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a>屬性



| 詞彙                                                                       | 描述                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="name"></span><span id="NAME"></span>**名字**<br/>          | 中繼資料專案的名稱。<br/>                                                                                       |
| <span id="content"></span><span id="CONTENT"></span>**內容**<br/> | 中繼資料專案的值。 例如，如果 name 屬性為 "content-type"，則內容屬性可能是 "搖滾"。<br/> |



 

## <a name="parentchild-elements"></a>父/子項目



| 階層 | 元素                 |
|-----------|--------------------------|
| 父代    | [頭](head-element.md) |
| 子系     | 無                     |



 

## <a name="remarks"></a>備註

Windows 媒體播放清單的建立者可以將中繼元素的 name 屬性設定為任何字串。 下列清單顯示在 Windows Media Player 和其他 Microsoft 元件 Windows 媒體播放清單中找到的一些典型的名稱屬性。

-   作者
-   類別
-   Genre
-   使用者名稱
-   UserRating
-   Generator

## <a name="examples"></a>範例


```
<head>
    <meta name = "Author" content = "Frank Lee"/>
    <meta name = "Category" content = "Classic"/>
    <meta name = "Genre" content = "Rock"/>
</head>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**head 元素**](head-element.md)
</dt> <dt>

[**WindowsMedia 播放清單元素參考**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





