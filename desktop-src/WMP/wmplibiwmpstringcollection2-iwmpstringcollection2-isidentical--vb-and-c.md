---
title: IWMPStringCollection2 isIdentical 方法
description: IsIdentical 方法會傳回值，指出提供的介面所表示的物件是否與目前的介面相同。
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- isIdentical 方法 Windows Media Player
- isIdentical 方法 Windows Media Player，IWMPStringCollection2 介面
- IWMPStringCollection2 介面 Windows Media Player，isIdentical 方法
topic_type:
- apiref
api_name:
- IWMPStringCollection2.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb760dae213f28d44fbc707b4430cb151cfe578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000936"
---
# <a name="iwmpstringcollection2isidentical-method"></a>IWMPStringCollection2：： isIdentical 方法

**IsIdentical** 方法會傳回值，指出提供的介面所表示的物件是否與目前的介面相同。

## <a name="syntax"></a>語法


```CSharp
public System.Boolean isIdentical(
  IWMPStringCollection2 pIWMPStringCollection2
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPStringCollection2 As IWMPStringCollection2 _
) As System.Boolean
Implements IWMPStringCollection2.isIdentical
```





## <a name="parameters"></a>參數

<dl> <dt>

*pIWMPStringCollection2* \[在\]
</dt> <dd>

**WMPLib. IWMPStringCollection2** 介面，表示要與目前物件比較的物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此為比較結果的 **system.object** 。 **True** 值表示字串集合物件相同。

## <a name="remarks"></a>備註

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11。<br/>                                                                                    |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPStringCollection2 介面 (VB 和 c # )**](iwmpstringcollection2--vb-and-c.md)
</dt> </dl>

 

 





