---
title: 'IWMPPlaylist. attributeName (VB 和 C ) '
description: AttributeName 屬性 (get \_ attributeName 方法 In C \ ) 取得索引所指定之播放清單屬性的名稱。
ms.assetid: bb436657-5156-437e-af58-6497ad3b311b
keywords:
- IWMPPlaylist. attributeName (VB 和 C ) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.attributeName (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 727d58a0cf875ed29efe9235448c1d597e81656a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992777"
---
# <a name="iwmpplaylistattributename-vb-and-c"></a>IWMPPlaylist. attributeName (VB 和 c # ) 

**AttributeName** 屬性 (c # 中的 **get \_ attributeName** 方法 ) 取得索引所指定之播放清單屬性的名稱。


```
[Visual Basic]
ReadOnly Property attributeName(
  lIndex As System.Int32
) As System.String
```




```
[C#]
System.String get_attributeName(
  System.Int32 lIndex
);
```



## <a name="parameters"></a>參數

*lIndex*

表示播放清單屬性索引的 **system.string。**

## <a name="return-value"></a>傳回值

**System.string** ，這是播放清單屬性的名稱。

## <a name="remarks"></a>備註

**IWMPPlaylist** 在使用參數的 Visual Basic 中，attributeName 是唯讀屬性，而在 c # 中則稱為 **IWMPPlaylist. get \_ attributeName** 方法。

**IWMPPlaylist. attributeCount** 屬性會傳回與播放清單相關聯的屬性數目。

這個屬性所傳回的名稱可以提供給 **setItemInfo** 或 **getItemInfo** 方法，以指定或抓取指名屬性的值。

使用這個屬性之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 [屬性參考](attribute-reference.md)。

## <a name="examples"></a>範例

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

[**IWMPPlaylist. attributeCount (VB 和 c # )**](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. getItemInfo (VB 和 c # )**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist. setItemInfo (VB 和 c # )**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





