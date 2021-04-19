---
title: IWMPLibrary isIdentical 方法
description: IsIdentical 方法會傳回一個值，這個值會指出提供的物件是否與目前的物件相同。
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- isIdentical 方法 Windows Media Player
- isIdentical 方法 Windows Media Player，IWMPLibrary 介面
- IWMPLibrary 介面 Windows Media Player，isIdentical 方法
topic_type:
- apiref
api_name:
- IWMPLibrary.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53071caa98b8f8e3ccb95e926969926cc68e7860
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987836"
---
# <a name="iwmplibraryisidentical-method"></a>IWMPLibrary：： isIdentical 方法

**IsIdentical** 方法會傳回一個值，這個值會指出提供的物件是否與目前的物件相同。

## <a name="syntax"></a>語法


```CSharp
public System.Boolean isIdentical(
  IWMPLibrary pIWMPLibrary
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPLibrary As IWMPLibrary _
) As System.Boolean
Implements IWMPLibrary.isIdentical
```





## <a name="parameters"></a>參數

<dl> <dt>

*pIWMPLibrary* \[在\]
</dt> <dd>

**WMPLib IWMPLibrary** 介面，表示要與目前的物件比較的物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

表示比較結果的 **system.object** 。 值 **true** 表示物件相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11。<br/>                                                                                    |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPLibrary 介面 (VB 和 c # )**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





