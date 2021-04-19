---
title: IWMPPlaylistCollection [] 方法
description: '[] 方法會傳回程式庫中新的空白播放清單的 IWMPPlaylist 介面。'
ms.assetid: cc0cb356-9a90-421c-8d1a-b79585f71124
keywords:
- '[] 方法 Windows Media Player'
- '[] 方法 Windows Media Player，IWMPPlaylistCollection 介面'
- IWMPPlaylistCollection 介面 Windows Media Player，[] 方法
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.newPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc455c5815cee1aaac139886bca1d847ddc62b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981098"
---
# <a name="iwmpplaylistcollectionnewplaylist-method"></a>IWMPPlaylistCollection：： [] 方法

**[]** 方法會傳回程式庫中新的空白播放清單的 **IWMPPlaylist** 介面。

## <a name="syntax"></a>語法


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.newPlaylist
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrName* \[在\]
</dt> <dd>

**System.string** ，這是新播放清單的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

新播放清單的 **WMPLib IWMPPlaylist** 介面。

## <a name="remarks"></a>備註

這個方法會在文件庫中建立空的播放清單。 若要以媒體專案填滿播放清單，請使用 **IWMPPlaylist. appendItem** 或 **IWMPPlaylist. insertItem**。

程式庫中允許有多個具有相同名稱的播放清單。 若要避免使用這個方法建立重複的播放清單名稱，請使用 **getByName** 方法和 **IWMPPlaylistArray** 來探索具有特定名稱的播放清單是否已存在。

播放清單名稱中不允許前置和尾端空格，並且會自動從 *bstrName* 參數指定的值中移除。

在呼叫這個方法之前，您必須擁有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列範例會建立名為 "ThreeList" 的新空白播放清單，並將其新增至播放清單集合，並將介面傳回給它。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Add a new empty playlist, named ThreeList, to the playlist collection.
WMPLib.IWMPPlaylist newList = player.playlistCollection.newPlaylist("ThreeList");
```


```VB

'  Add a new empty playlist, named ThreeList, to the playlist collection.
Dim newList As WMPLib.IWMPPlaylist = player.playlistCollection.newPlaylist(&quot;ThreeList&quot;)
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player  9  系列或更新的版本。<br/>                                                                     |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. appendItem (VB 和 c # )**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. insertItem (VB 和 c # )**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray (VB 和 c # )**](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection 介面 (VB 和 c # )**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB 和 c # )**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





