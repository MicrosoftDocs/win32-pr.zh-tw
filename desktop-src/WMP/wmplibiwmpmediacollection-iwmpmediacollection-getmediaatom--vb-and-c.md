---
title: IWMPMediaCollection getMediaAtom 方法
description: GetMediaAtom 方法會傳回一組可用屬性中指定屬性的索引。
ms.assetid: 01e3d073-677b-4939-96d3-63ae96eaa25d
keywords:
- getMediaAtom 方法 Windows Media Player
- getMediaAtom 方法 Windows Media Player，IWMPMediaCollection 介面
- IWMPMediaCollection 介面 Windows Media Player，getMediaAtom 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getMediaAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08487cf60c351ff4f8e0741209655cb78c30c3f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999730"
---
# <a name="iwmpmediacollectiongetmediaatom-method"></a>IWMPMediaCollection：： getMediaAtom 方法

方法會傳回 `getMediaAtom` 一組可用屬性中指定屬性的索引。

## <a name="syntax"></a>語法


```CSharp
public System.Int32 getMediaAtom(
  System.String bstrItemName
);
```


```VB

Public Function getMediaAtom( _
  ByVal bstrItemName As System.String _
) As System.Int32
Implements IWMPMediaCollection.getMediaAtom
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrItemName* \[在\]
</dt> <dd>

**System.string** ，此為應抓取索引的專案名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

做為索引的 **system.object** 。

## <a name="remarks"></a>備註

使用這個方法取出的索引編號可以傳遞給 **IWMPMedia. getItemInfoByAtom** 以存取屬性值。 使用大型播放清單時，這項技術通常更有效率，而不是透過 **IWMPMedia. getItemInfo** 存取屬性值。

在呼叫這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPMedia. getItemInfo (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfoByAtom (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection 介面 (VB 和 c # )**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





