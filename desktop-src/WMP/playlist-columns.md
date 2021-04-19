---
title: 播放清單。資料行
description: Columns 屬性會定義出現在播放清單元素中的資料行。
ms.assetid: a805ee06-cf73-4eab-bcda-c374e55cd11a
keywords:
- 播放清單. 資料行 Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.columns
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc5f8ef5dc76428ca892d079b60692e6949a5ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976002"
---
# <a name="playlistcolumns"></a>播放清單。資料行

**Columns** 屬性會定義出現在 **播放清單** 元素中的資料行。

``` syntax
        elementID.columns
```

## <a name="possible-values"></a>可能的值

這個屬性是具有下列格式的讀取/寫入 **字串** ：

DB \_ 名稱 = 易記 \_ 名稱; 資料庫 \_ 名稱 = 易記 \_ 名稱;

易記 \_ 名稱是顯示在播放清單元素之資料行標頭中的值，而資料庫 \_ 名稱是下表中的值。 請注意，播放清單專案可能是來自媒體櫃或 CD 的媒體專案，也可能是由使用者建立或取自 CD 的另一個 **播放清單** 。 某些資料行只有在 [描述] 欄中指出的特定播放清單專案才有效。



| 值             | 描述                                                                                                             |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| 專輯             | 專輯的名稱。 僅搭配媒體專案使用。                                                                      |
| 演出者            | 演出者的名稱。 不適用於使用者建立的播放清單。                                                           |
| 作者            | 演出者的名稱。                                                                                                 |
| Bitrate           | 內容的位元速率。 只能與媒體櫃中的媒體專案搭配使用。                                               |
| CDTrackEnabled    | 指出是否已啟用 CD 曲目。 只能搭配 CD 媒體專案使用。                                               |
| 已核取           | 保留供未來使用。                                                                                                |
| 著作權         | 播放清單的著作權。 未搭配 CD 播放清單或媒體專案使用。                                               |
| CreationDate      | 程式庫中專案的建立日期和時間。 只能與程式庫中的專案搭配使用。                     |
| DigitallySecure   | 指出專案是否以 Windows Media Rights Manager 保護。 只能與媒體櫃中的媒體專案搭配使用。 |
| 持續時間          | 媒體專案的持續時間。                                                                                         |
| FileType          | 保留供未來使用。                                                                                                |
| Genre             | 播放清單的類型。 不適用於 Cd 的播放清單。                                                            |
| MediaAttribute    | 保留供未來使用。                                                                                                |
| MediaType         | 媒體專案的類型 (音訊或影片) 。                                                                            |
| MetadataSource    | 此 CD 軌的中繼資料來源 (AMG、WindowsMedia.com 等) 。 只能搭配 CD 媒體專案使用。         |
| ModifiedBy        | 保留供未來使用。                                                                                                |
| Name              | 播放清單的名稱。                                                                                               |
| OriginalIndex     | 如果適用的話，則為對應的 CD 播放軌識別碼。 只能搭配 CD 媒體專案使用。                                    |
| PlayCount         | 已播放內容到結尾的次數。 只能與媒體櫃中的媒體專案搭配使用。        |
| PlaylistAttribute | 保留供未來使用。                                                                                                |
| 分級            | 保留供未來使用。                                                                                                |
| SourceURL         | 內容的路徑或 URL。 只能與媒體櫃中的媒體專案搭配使用。                                            |
| 狀態            | 要複製之 CD 播放軌的複製狀態。 只能搭配 CD 媒體專案使用。                                           |
| 樣式             | 保留供未來使用。                                                                                                |
| 目錄               | 如果適用的話，則為對應的 CD 目錄識別碼。 不適用於使用者建立的播放清單。                 |



 

## <a name="remarks"></a>備註

如果其中一個資料行不存在於文件庫中，則會保留空白。

最多可以指定31個數據行。

如果您指定重複的資料行，第一個資料行中的資料將會靠左對齊，但是所有其他重複的資料行都會靠右對齊。 例如，如果您有兩個持續時間資料行，資料將會靠左對齊，並在第二個靠右對齊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> <dt>

[**播放清單。 columnsVisible**](playlist-columnsvisible.md)
</dt> </dl>

 

 





