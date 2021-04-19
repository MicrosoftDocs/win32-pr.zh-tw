---
title: IWMPPlaylistCollection remove 方法
description: Remove 方法會從文件庫中移除播放清單。 |IWMPPlaylistCollection remove 方法
ms.assetid: 40c8ee1d-13fa-40d9-9532-4dc8383c4eb3
keywords:
- 移除方法 Windows Media Player
- remove 方法 Windows Media Player，IWMPPlaylistCollection 介面
- IWMPPlaylistCollection 介面 Windows Media Player、remove 方法
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99fbaa2f60c769599bd6173b8e38f4d99e9f42d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990851"
---
# <a name="iwmpplaylistcollectionremove-method"></a>IWMPPlaylistCollection：： remove 方法

**Remove** 方法會從文件庫中移除播放清單。

## <a name="syntax"></a>語法


```CSharp
public void remove(
  IWMPPlaylist pItem
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPPlaylist _
)
Implements IWMPPlaylistCollection.remove
```





## <a name="parameters"></a>參數

<dl> <dt>

*pItem* \[在\]
</dt> <dd>

此方法將移除之播放清單的 **WMPLib IWMPPlaylist** 介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在呼叫這個方法之前，您必須擁有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

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

[**IWMPPlaylistCollection 介面 (VB 和 c # )**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





