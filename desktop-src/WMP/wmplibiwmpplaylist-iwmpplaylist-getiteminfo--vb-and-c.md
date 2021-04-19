---
title: IWMPPlaylist getItemInfo 方法
description: GetItemInfo 方法會傳回依名稱指定的播放清單屬性值。
ms.assetid: 62e882d6-66bb-450c-9700-b99d30dd42fa
keywords:
- getItemInfo 方法 Windows Media Player
- getItemInfo 方法 Windows Media Player，IWMPPlaylist 介面
- IWMPPlaylist 介面 Windows Media Player，getItemInfo 方法
topic_type:
- apiref
api_name:
- IWMPPlaylist.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced433b13f5af2d1df8c12dba023b7fbb55c5f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990077"
---
# <a name="iwmpplaylistgetiteminfo-method"></a>IWMPPlaylist：： getItemInfo 方法

**GetItemInfo** 方法會傳回依名稱指定的播放清單屬性值。

## <a name="syntax"></a>語法


```CSharp
public System.String getItemInfo(
  System.String bstrName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrName As System.String _
) As System.String
Implements IWMPPlaylist.getItemInfo
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrName* \[在\]
</dt> <dd>

**System.string** ，這是播放清單屬性的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

**System.string** ，這是播放清單屬性的值。

## <a name="remarks"></a>備註

使用這個方法之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

如需使用這個屬性的範例程式碼，請參閱 [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) 屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. setItemInfo (VB 和 c # )**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





