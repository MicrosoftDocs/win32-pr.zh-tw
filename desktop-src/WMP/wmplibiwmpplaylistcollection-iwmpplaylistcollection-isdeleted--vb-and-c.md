---
title: IWMPPlaylistCollection isDeleted 方法
description: IsDeleted 方法會傳回值，指出指定的播放清單是否在 [刪除的專案] 資料夾中。
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- isDeleted 方法 Windows Media Player
- isDeleted 方法 Windows Media Player，IWMPPlaylistCollection 介面
- IWMPPlaylistCollection 介面 Windows Media Player，isDeleted 方法
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.isDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ce4a314378c5a4a211a52b99ea1b36ae1fda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000651"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a>IWMPPlaylistCollection：： isDeleted 方法

**IsDeleted** 方法會傳回值，指出指定的播放清單是否在 [刪除的專案] 資料夾中。

## <a name="syntax"></a>語法


```CSharp
public System.Boolean isDeleted(
  IWMPPlaylist pItem
);
```


```VB

Public Function isDeleted( _
  ByVal pItem As IWMPPlaylist _
) As System.Boolean
Implements IWMPPlaylistCollection.isDeleted
```





## <a name="parameters"></a>參數

<dl> <dt>

*pItem* \[在\]
</dt> <dd>

所查詢播放清單的 **WMPLib IWMPPlaylist** 介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

指定播放清單是否已刪除的 **布林值** 。

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

 

 





