---
title: IWMPPlaylist (VB 和 C) 介面 (Wmp.h)
description: 提供屬性和方法來組織、管理和操作播放清單中的媒體專案。IWMPPlaylist 介面會公開下列屬性。
ms.assetid: c3f4f9dd-eb5f-493a-b8d0-22e70c63a2d1
keywords:
- IWMPPlaylist (VB 和 C ) 介面 Windows Media Player
- IWMPPlaylist (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPPlaylist (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52090588905e2fd79b218abe939f78c1e38fc79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989684"
---
# <a name="iwmpplaylist-vb-and-c-interface"></a>IWMPPlaylist (VB 和 c # ) 介面

提供屬性和方法來組織、管理和操作播放清單中的媒體專案。

**IWMPPlaylist** 介面會公開下列屬性。

## <a name="members"></a>成員

**IWMPPlaylist (VB 和 c # )** 介面都有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IWMPPlaylist (VB 和 c # )** 介面都有這些方法。



| 方法                                                                       | 描述                                                             |
|:-----------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**appendItem**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)   | 將媒體專案加入至播放清單的結尾。<br/>                |
| [**清楚**](iwmpplaylist-iwmpplaylist-clear--vb-and-c.md)                   | 保留供未來使用。<br/>                                     |
| [**getItemInfo**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) | 傳回依名稱指定的播放清單屬性值。<br/> |
| [**insertItem**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)   | 將媒體專案插入播放清單中的指定位置。<br/>  |
| [**moveItem**](wmplibiwmpplaylist-iwmpplaylist-moveitem--vb-and-c.md)       | 變更播放清單中媒體專案的位置。<br/>        |
| [**removeItem**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)   | 從播放清單中移除指定的媒體專案。<br/>          |
| [**setItemInfo**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md) | 設定播放清單屬性的值。<br/>                      |



 

### <a name="properties"></a>屬性

**IWMPPlaylist (VB 和 c # )** 介面都有這些屬性。



| 屬性                                                                                      | 存取類型           | Description                                                                                                                                         |
|:----------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attributeCount**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)<br/> | 唯讀<br/>  | 取得與播放清單相關聯的屬性數目。<br/>                                                                                |
| [**attributeName**](iwmpplaylist-attributename--vb-and-c.md)<br/>                      | 唯讀<br/>  | 取得索引所指定之播放清單屬性的名稱。 在 c # 中，這是 get \_ attributeName 方法。<br/>                               |
| [**count**](wmplibiwmpplaylist-iwmpplaylist-count--vb-and-c.md)<br/>                   | 唯讀<br/>  | 取得播放清單中的媒體專案數目。<br/>                                                                                            |
| [**isIdentical**](iwmpplaylist-isidentical--vb-and-c.md)<br/>                          | 唯讀<br/>  | 取得值，指出指定的播放清單是否與目前的播放清單相同。 在 c # 中，這是 get \_ isIdentical 方法。<br/> |
| [**項目**](iwmpplaylist-item--vb-and-c.md)<br/>                                        | 唯讀<br/>  | 取得位於指定索引處之媒體專案的介面。 在 c # 中，這是取得 \_ 專案方法。<br/>                                         |
| [**名字**](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)<br/>                     | 讀取/寫入<br/> | 取得或設定播放清單的名稱。<br/>                                                                                                   |



 

使用透過下列物件或介面存取的下列屬性或方法，取得 **IWMPPlaylist** 介面。



| 物件或介面                                                | 屬性或方法                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMPCdrom**](iwmpcdrom--vb-and-c.md)                           | [**播放 清單**](wmplibiwmpcdrom-iwmpcdrom-playlist--vb-and-c.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**IWMPMediaCollection**](iwmpmediacollection--vb-and-c.md)       | [**getAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)、 [**getByAlbum**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum)、 [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)、 [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)、 [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)、 [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md) |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md)  | [**currentPlaylist**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)、 [ **[]**](axwmplib-axwindowsmediaplayer-newplaylist.md)                                                                                                                                                                                                                                                                                                                                                                   |
| [**IWMPPlaylistArray**](iwmpplaylistarray--vb-and-c.md)           | [**項目**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistarray-item)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**IWMPPlaylistCollection**](iwmpplaylistcollection--vb-and-c.md) | [**[]**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylistcollection-newplaylist)                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**適用于 Visual Basic .NET 和 C 的介面#**](interfaces-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 





