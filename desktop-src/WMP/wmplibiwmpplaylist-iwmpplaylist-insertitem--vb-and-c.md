---
title: IWMPPlaylist insertItem 方法
description: InsertItem 方法會將媒體專案插入播放清單中的指定位置。
ms.assetid: 6e472f0a-13df-41d9-8e6f-8430d87fe978
keywords:
- insertItem 方法 Windows Media Player
- insertItem 方法 Windows Media Player，IWMPPlaylist 介面
- IWMPPlaylist 介面 Windows Media Player，insertItem 方法
topic_type:
- apiref
api_name:
- IWMPPlaylist.insertItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10717c0891443aaa663b748be6a0cb57e04e58b96beb91db6b02b2f6a4b5b621
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464928"
---
# <a name="iwmpplaylistinsertitem-method"></a>IWMPPlaylist：： insertItem 方法

**InsertItem** 方法會將媒體專案插入播放清單中的指定位置。

## <a name="syntax"></a>語法


```CSharp
public void insertItem(
  System.Int32 lIndex,
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub insertItem( _
  ByVal lIndex As System.Int32, _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.insertItem
```





## <a name="parameters"></a>參數

<dl> <dt>

*lIndex* \[在\]
</dt> <dd>

以零為基底的索引，也就是媒體專案將插入播放清單中的位置 **。**

</dd> <dt>

*pIWMPMedia* \[在\]
</dt> <dd>

代表要插入之媒體專案的 **WMPLib IWMPMedia** 介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

插入專案之後的所有媒體專案都會增加一個索引。

在呼叫這個方法之前，您必須擁有程式庫的完整存取權。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. removeItem (VB 和 c # )**](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> </dl>

 

 





