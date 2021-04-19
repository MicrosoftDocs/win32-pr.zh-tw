---
title: 媒體元件
description: 媒體元件會指定播放清單中的其中一個媒體專案。
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- 媒體元件 Windows Media Player
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e693c8b17345d3ba7875d48b83b5e3e90d682dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988234"
---
# <a name="media-element"></a>媒體元件

**媒體** 元素會指定播放清單中的其中一個媒體專案。

``` syntax
<media
    src = "URL"
    cid = "WPL_GUID"
    tid = "WPL_GUID"
>
</media>
```

## <a name="attributes"></a>屬性



| 詞彙                                                                                                                       | 描述                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>需要 (**src**)  <br/> | 媒體專案的 URL。<br/>                                                              |
| <span id="cid"></span><span id="CID"></span>**Cid**<br/>                                                             | 此媒體專案特有的內容識別碼。<br/>                                     |
| <span id="tid"></span><span id="TID"></span>**tid**<br/>                                                             | 可以用來追蹤此媒體專案之檔案系統物件的追蹤識別碼。<br/> |



 

## <a name="parentchild-elements"></a>父/子項目



| 階層 | 元素               |
|-----------|------------------------|
| 父代    | [序列](seq-element.md) |
| 子系     | 無                   |



 

## <a name="remarks"></a>備註

**Cid** 屬性 (內容識別碼) 是由 Windows Media Player 填入，以唯一識別媒體內容的一部分，即使其中繼資料屬性已變更也是一樣。 這可讓您在電腦上共用播放清單，因為內容可以在另一部電腦上識別，而 Windows Media 播放清單可以「自動修復」內容的路徑。 當檔案的名稱或位置變更時，) 使用 Windows 檔案系統來自動修復媒體的路徑，則 [ **tid** ] 屬性 (追蹤識別碼。

## <a name="examples"></a>範例


```
<media
    src = "laure.wma"
    cid = "ABCDEFGH-abcd-1234-WXYZ-ABCDEF000000"
    tid = "12345678-1234-abcd-ABCD-123456abcDEF"
>
</media>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**seq 元素**](seq-element.md)
</dt> <dt>

[**Windows Media 播放清單元素參考**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





