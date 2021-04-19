---
title: IWMPMedia getItemInfoByAtom 方法
description: GetItemInfoByAtom 方法會傳回具有指定之索引編號的屬性值。
ms.assetid: d9a4b737-add1-4bbd-8e03-e58f45d65a62
keywords:
- getItemInfoByAtom 方法 Windows Media Player
- getItemInfoByAtom 方法 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，getItemInfoByAtom 方法
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfoByAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb37243960360120fbfe508a39db31e37728ac39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999496"
---
# <a name="iwmpmediagetiteminfobyatom-method"></a>IWMPMedia：： getItemInfoByAtom 方法

**GetItemInfoByAtom** 方法會傳回具有指定之索引編號的屬性值。

## <a name="syntax"></a>語法


```CSharp
public System.String getItemInfoByAtom(
  System.Int32 lAtom
);
```


```VB

Public Function getItemInfoByAtom( _
  ByVal lAtom As System.Int32 _
) As System.String
Implements IWMPMedia.getItemInfoByAtom
```





## <a name="parameters"></a>參數

<dl> <dt>

*lAtom* \[在\]
</dt> <dd>

指定所要求屬性位於可用屬性集合內之索引的 **system.object。**

</dd> </dl>

## <a name="return-value"></a>傳回值

**System.string** ，此為屬性的值。

## <a name="remarks"></a>備註

這個方法可以用來使用屬性索引編號來取得特定媒體專案的中繼資料。 **AttributeCount** 屬性可以用來判斷媒體專案可用的屬性數目。

**IWMPMediaCollection** 介面的 **getMediaAtom** 方法也可以用來取得特定屬性的索引。 這項技術通常比使用大型播放清單時的 **getItemInfo** 或 **getItemInfoByType** 方法更有效率。

在呼叫這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

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

[**IWMPMedia. attributeCount (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfo (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. setItemInfo (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB 和 c # )**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection. getMediaAtom (VB 和 c # )**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)
</dt> </dl>

 

 





