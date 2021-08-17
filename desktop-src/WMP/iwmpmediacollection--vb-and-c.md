---
title: 'IWMPMediaCollection (VB 和 C ) 介面 (Wmp. h) '
description: 提供可用於組織大型媒體專案集合的方法。
ms.assetid: a9e3d466-7dcf-4f1b-ba6f-9d166a35f03d
keywords:
- IWMPMediaCollection (VB 和 C ) 介面 Windows Media Player
- IWMPMediaCollection (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPMediaCollection (VB and C )
- IWMPMediaCollection (VB and C ).isDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce15616b2059802610360b52d5af9bfa8d56b56b7ed06129bb849de567e22e26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468448"
---
# <a name="iwmpmediacollection-vb-and-c-interface"></a>IWMPMediaCollection (VB 和 c # ) 介面

提供可用於組織大型媒體專案集合的方法。

## <a name="members"></a>成員

**IWMPMediaCollection (VB 和 c # )** 介面都有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMPMediaCollection (VB 和 c # )** 介面都有這些方法。



| 方法                                                                                                                       | 描述                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**add**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)                                                   | 將新的媒體專案或播放清單新增至程式庫。<br/>                                                                                  |
| [**getAll**](wmplibiwmpmediacollection-iwmpmediacollection-getall--vb-and-c.md)                                             | 傳回 **IWMPPlaylist** 介面，這個介面對應于包含媒體櫃中所有媒體專案的播放清單。<br/>               |
| [**getAttributeStringCollection**](wmplibiwmpmediacollection-iwmpmediacollection-getattributestringcollection--vb-and-c.md) | 傳回 **IWMPStringCollection** 介面，這個介面表示媒體類型內指定之屬性的所有值集。<br/> |
| [**getByAlbum**](wmplibiwmpmediacollection-iwmpmediacollection-getbyalbum--vb-and-c.md)                                     | 傳回 **IWMPPlaylist** 介面，這個介面可讓您從指定的專輯存取媒體專案。<br/>                                |
| [**getByAttribute**](wmplibiwmpmediacollection-iwmpmediacollection-getbyattribute--vb-and-c.md)                             | 傳回 **IWMPPlaylist** 介面，這個介面會對應到具有指定值的指定屬性。<br/>                      |
| [**getByAuthor**](wmplibiwmpmediacollection-iwmpmediacollection-getbyauthor--vb-and-c.md)                                   | 傳回 **IWMPPlaylist** 介面，這個介面會提供指定作者對媒體專案的存取權。<br/>                             |
| [**getByGenre**](wmplibiwmpmediacollection-iwmpmediacollection-getbygenre--vb-and-c.md)                                     | 傳回 **IWMPPlaylist** 介面，這個介面可讓您存取指定之類型的媒體專案。<br/>                                  |
| [**getByName**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)                                       | 傳回 **IWMPPlaylist** 介面，這個介面會提供具有指定名稱之媒體專案的存取權。<br/>                                 |
| [**getMediaAtom**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)                                 | 傳回指定之屬性的索引。<br/>                                                                                        |
| **isDeleted**                                                                                                                | 不再支援。<br/>                                                                                                               |
| [**刪除**](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)                                             | 從媒體集合移除指定的媒體專案。<br/>                                                                        |
| [**setDeleted**](wmplibiwmpmediacollection-iwmpmediacollection-setdeleted--vb-and-c.md)                                     | 將指定的媒體專案移到 [刪除的專案] 資料夾。<br/>                                                                        |



 

使用透過下列物件或介面存取的下列屬性來取得 **IWMPMediaCollection** 介面。



| 物件或介面                                               | 屬性                                                                           |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**mediaCollection**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) |
| [**IWMPLibrary**](iwmplibrary--vb-and-c.md)                      | [**mediaCollection**](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**適用于 Visual Basic .net 和 C 的介面#**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2 介面**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection 介面 (VB 和 c # )**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





