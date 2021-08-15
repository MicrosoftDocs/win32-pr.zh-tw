---
title: IWMPPlaylistArray Item 方法
description: Item 方法會傳回 IWMPPlaylist 介面，代表指定索引處的播放清單。
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- Item 方法 Windows Media Player
- Item 方法 Windows Media Player，IWMPPlaylistArray 介面
- IWMPPlaylistArray 介面 Windows Media Player，Item 方法
topic_type:
- apiref
api_name:
- IWMPPlaylistArray.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e73614e1ef00f29d6b09d3d49e2c7e514bae807245f00f30f4d3382d8f1a2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331157"
---
# <a name="iwmpplaylistarrayitem-method"></a>IWMPPlaylistArray：： Item 方法

**Item** 方法會傳回 **IWMPPlaylist** 介面，代表指定索引處的播放清單。

## <a name="syntax"></a>語法


```CSharp
public IWMPPlaylist Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPPlaylist
Implements IWMPPlaylistArray.Item
```





## <a name="parameters"></a>參數

<dl> <dt>

*lIndex* \[在\]
</dt> <dd>

包含索引的 **system.object** ，此索引會識別該方法應該抓取的播放清單。

</dd> </dl>

## <a name="return-value"></a>傳回值

已抓取播放清單的 **WMPLib IWMPPlaylist** 介面。

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

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistArray 介面 (VB 和 c # )**](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





