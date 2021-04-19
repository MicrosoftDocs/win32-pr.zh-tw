---
title: IWMPPlaylistCollection importPlaylist 方法
description: ImportPlaylist 方法會將靜態播放清單新增至程式庫。 |IWMPPlaylistCollection importPlaylist 方法
ms.assetid: 7a64e618-920d-419d-8769-612ab5dff49b
keywords:
- importPlaylist 方法 Windows Media Player
- importPlaylist 方法 Windows Media Player，IWMPPlaylistCollection 介面
- IWMPPlaylistCollection 介面 Windows Media Player，importPlaylist 方法
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.importPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ca727155d6ae859123d427812d93ebaa0b05c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989691"
---
# <a name="iwmpplaylistcollectionimportplaylist-method"></a>IWMPPlaylistCollection：： importPlaylist 方法

**ImportPlaylist** 方法會將靜態播放清單新增至程式庫。

## <a name="syntax"></a>語法


```CSharp
public IWMPPlaylist importPlaylist(
  IWMPPlaylist pItem
);
```


```VB

Public Function importPlaylist( _
  ByVal pItem As IWMPPlaylist _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.importPlaylist
```





## <a name="parameters"></a>參數

<dl> <dt>

*pItem* \[在\]
</dt> <dd>

此方法將新增之播放清單的 **WMPLib IWMPPlaylist** 介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

已新增播放清單的 **WMPLib IWMPPlaylist** 介面。

## <a name="remarks"></a>備註

未包含任何媒體專案的播放清單，無法使用此方法新增至程式庫。 若要在程式庫中建立空的播放清單，請使用 **[]** 方法。 然後，您可以使用 **IWMPPlaylist. appendItem** 或 **IWMPPlaylist**，以媒體專案填滿產生的播放清單。

如果您將此方法傳遞給自動播放清單，則查詢會執行一次，並將結果以靜態播放清單的形式新增至程式庫。 若要將自動播放清單新增至程式庫並保留其自動行為，請使用 **IWMPMediaCollection。** 如需詳細資訊，請參閱 [靜態和自動播放清單](static-and-auto-playlists.md)。

在呼叫這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player  9  系列或更新的版本。<br/>                                                                     |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPMediaCollection：新增 (VB 和 c # )**](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. appendItem (VB 和 c # )**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. insertItem (VB 和 c # )**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection 介面 (VB 和 c # )**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. [] (VB 和 c # )**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





