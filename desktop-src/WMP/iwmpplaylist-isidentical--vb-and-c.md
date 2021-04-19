---
title: 'IWMPPlaylist. isIdentical (VB 和 C ) '
description: IsIdentical 屬性 (\_ 在 C \ ) 的 get isIdentical 方法取得值，指出指定的播放清單是否與目前的播放清單相同。
ms.assetid: 0e5520ee-3d41-4e36-98f4-7bc2ec45fcb8
keywords:
- IWMPPlaylist. isIdentical (VB 和 C ) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee30441e8f0275bba06f71a01095c39da8eae9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982924"
---
# <a name="iwmpplaylistisidentical-vb-and-c"></a>IWMPPlaylist. isIdentical (VB 和 c # ) 

**IsIdentical** 屬性 (c # 中的 **get \_ isIdentical** 方法 ) 取得值，指出指定的播放清單是否與目前的播放清單相同。


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPPlaylist As IWMPPlaylist
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPPlaylist pIWMPPlaylist
);
```



## <a name="parameters"></a>參數

*pIWMPPlaylist*

適用于播放清單的 **WMPLib IWMPPlaylist** 介面，這個方法會與目前的播放清單比較。

## <a name="property-value"></a>屬性值

**布林值**，指出比較的播放清單是否相同。

## <a name="remarks"></a>備註

**IWMPPlaylist** 是採用參數的 Visual Basic 中的屬性，而在 c # 中則稱為 **IWMPPlaylist. get \_ isIdentical** 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





