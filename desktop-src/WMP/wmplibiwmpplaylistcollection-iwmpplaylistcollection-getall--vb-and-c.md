---
title: IWMPPlaylistCollection getAll 方法
description: GetAll 方法會傳回 IWMPPlaylistArray 介面，此介面可讓您存取媒體櫃中的所有播放清單。
ms.assetid: d36dbc5c-ccb0-400a-ab5b-918598c218f1
keywords:
- getAll 方法 Windows Media Player
- getAll 方法 Windows Media Player，IWMPPlaylistCollection 介面
- IWMPPlaylistCollection 介面 Windows Media Player，getAll 方法
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4260f5c960650cf6c04a1dd8b39d887f711fb8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980104"
---
# <a name="iwmpplaylistcollectiongetall-method"></a>IWMPPlaylistCollection：： getAll 方法

**GetAll** 方法會傳回 **IWMPPlaylistArray** 介面，此介面可讓您存取媒體櫃中的所有播放清單。

## <a name="syntax"></a>語法


```CSharp
public IWMPPlaylistArray getAll();
```


```VB

Public Function getAll() As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getAll
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

已抓取之播放清單陣列的 **WMPLib IWMPPlaylistArray** 介面。

## <a name="remarks"></a>備註

在呼叫這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player  9  系列或更新的版本。<br/>                                                                     |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPPlaylistArray 介面 (VB 和 c # )**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection 介面 (VB 和 c # )**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





