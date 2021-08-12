---
title: 'IWMPPlaylistCollection (VB 和 C ) 介面 (Wmp. h) '
description: 提供在集合中操作 IWMPPlaylist 和 IWMPPlaylistArray 介面的方法。
ms.assetid: 19a4e0d7-cb3f-42ec-9acb-7ac0c5837662
keywords:
- IWMPPlaylistCollection (VB 和 C ) 介面 Windows Media Player
- IWMPPlaylistCollection (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection (VB and C )
- IWMPPlaylistCollection (VB and C ).setDeleted
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ae130b9134d9ad6e19fa062946a591cdf7749b428201750fda8ff55252c3212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575214"
---
# <a name="iwmpplaylistcollection-vb-and-c-interface"></a>IWMPPlaylistCollection (VB 和 c # ) 介面

提供在集合中操作 **IWMPPlaylist** 和 **IWMPPlaylistArray** 介面的方法。

## <a name="members"></a>成員

**IWMPPlaylistCollection (VB 和 c # )** 介面都有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMPPlaylistCollection (VB 和 c # )** 介面都有這些方法。



| 方法                                                                                                 | 描述                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**getAll**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)                 | 傳回 **IWMPPlaylistArray** 介面，此介面可讓您存取媒體櫃中的所有播放清單。<br/>             |
| [**getByName**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)           | 傳回 **IWMPPlaylistArray** 介面，這個介面會提供具有指定名稱的播放清單存取權（如果有的話）。<br/> |
| [**importPlaylist**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md) | 將靜態播放清單新增至程式庫。<br/>                                                                              |
| [**isDeleted**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-isdeleted--vb-and-c.md)           | 傳回值，指出指定的播放清單是否在 [刪除的專案] 資料夾中。<br/>                           |
| [**[]**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)       | 傳回程式庫中新的空白播放清單的 **IWMPPlaylist** 介面。<br/>                                     |
| [**刪除**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-remove--vb-and-c.md)                 | 從媒體櫃移除播放清單。<br/>                                                                                |
| **setDeleted**                                                                                         | 不再支援。<br/>                                                                                                |



 

使用下列屬性來取得 **IWMPPlaylistCollection** 介面。



| Object                                                                   | 屬性                                                                                 |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [AxWindowsMediaPlayer 物件](axwindowsmediaplayer-object--vb-and-c.md) | [**playlistCollection**](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md) |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**適用于 Visual Basic .net 和 C 的介面#**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray 介面 (VB 和 c # )**](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





