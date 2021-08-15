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
ms.openlocfilehash: c67f4321d85ec52babbc6f24c2cd9e3512f7c970eb3360ba2ddfd7ba53f82152
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996318"
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

**cid** 屬性 (內容識別碼) 是由 Windows Media Player 填入，以唯一識別媒體內容的一部分，即使其中繼資料屬性已變更也是一樣。 這可讓您在電腦上共用播放清單，因為內容可以在另一部電腦上識別，且 Windows 媒體播放清單可以「自動修復」的路徑。 當檔案的名稱或位置變更時，) 使用 Windows 檔案系統來自動修復媒體的路徑， (追蹤識別碼的 **tid** 屬性。

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

[**WindowsMedia 播放清單元素參考**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





