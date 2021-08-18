---
title: AlbumInfo 元素
description: AlbumInfo 元素會指定當使用者選擇要查看特定媒體專案的詳細資訊時，Windows Media Player 顯示之網頁的 URL。
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- AlbumInfo 元素 Windows Media Player
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9a5f8fab7da8f61ce6ee5451ebcef4dc33517aae2396f0817fac19222713db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055376"
---
# <a name="albuminfo-element"></a>AlbumInfo 元素

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**AlbumInfo** 元素會指定當使用者選擇要查看特定媒體專案的詳細資訊時，Windows Media Player 顯示之網頁的 URL。

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a>屬性

<dl> <dt>

<span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>需要 (**URL**) 
</dt> <dd>

Windows Media Player 顯示之網頁的 URL。

</dd> </dl>

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素         |
|-----------------|-----------------|
| 父元素 | **ServiceInfo** |
| 子元素  | 無            |



 

## <a name="remarks"></a>備註

當使用者按一下 Windows Media Player 中的按鈕來查看特定媒體專案的其他資訊時，播放玩家會使用問號 (？ ) 查詢字串分隔符號，以附加的參數來傳送 URL 要求。 下表詳細說明以 URL 要求傳送的參數。 其他可能存在於舊版相容性的用途。



| 名稱         | 值                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *專輯*      | 媒體專案之 **WM/AlbumTitle** 屬性的值。                                                                                                        |
| *演出者*     | **WM/AlbumArtist** 屬性的值（如果有的話），否則為媒體專案的 **Author** 屬性值。                                         |
| *大地 水準面*      | Windows 的地理位置識別碼。 在主控台的 [地區及語言選項] 設定的 [ **位置** ] 區域中，使用者會指定位置識別碼。 |
| *locale*     | Windows Media Player 地區設定識別碼。                                                                                                                                     |
| *標題*      | 媒體專案的 **標題** 屬性值。                                                                                                                |
| *UFID*       | 媒體專案之 **WM/UniqueFileIdentifier** 屬性的值。                                                                                              |
| *userlocale* | Windows 地區設定識別碼。 地區設定是由使用者在主控台的 [地區及語言選項] 設定的 [ **標準] 和 [格式** ] 區域中所指定。        |
| *version*    | 使用下列格式的 Windows Media Player 版本號碼： 10.0. x. x. x. x. x. x. x. x. x。                                                                         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------|
| 版本<br/> | Windows Media Player 10 或更新版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Type 2 線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> </dl>

 

 





