---
title: IWMPMediaCollection2 getByAttributeAndMediaType 方法
description: GetByAttributeAndMediaType 方法會傳回 IWMPPlaylist 介面，以提供具有指定屬性和媒體類型的媒體專案存取權。
ms.assetid: dce9cef4-1d12-4bee-a75d-42274556c5bc
keywords:
- getByAttributeAndMediaType 方法 Windows Media Player
- getByAttributeAndMediaType 方法 Windows Media Player，IWMPMediaCollection2 介面
- IWMPMediaCollection2 介面 Windows Media Player，getByAttributeAndMediaType 方法
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getByAttributeAndMediaType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e08d38954dd24246b4d35b7842f890caba6eea94868901a528396e9a22b38c1a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246424"
---
# <a name="iwmpmediacollection2getbyattributeandmediatype-method"></a>IWMPMediaCollection2：： getByAttributeAndMediaType 方法

`getByAttributeAndMediaType`方法會傳回 **IWMPPlaylist** 介面，以提供具有指定屬性和媒體類型之媒體專案的存取權。

## <a name="syntax"></a>語法


```CSharp
public IWMPPlaylist getByAttributeAndMediaType(
  System.String bstrAttribute,
  System.String bstrValue,
  System.String bstrMediaType
);
```


```VB

Public Function getByAttributeAndMediaType( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getByAttributeAndMediaType
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrAttribute* \[在\]
</dt> <dd>

指定之屬性的 **system.string** 。

</dd> <dt>

*bstrValue* \[在\]
</dt> <dd>

*BstrAttribute* 中所指定之屬性的指定值的 **system.string。**

</dd> <dt>

*bstrMediaType* \[在\]
</dt> <dd>

指定媒體類型的 **system.string** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

已抓取播放清單的 **WMPLib IWMPPlaylist** 介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 11。<br/>                                                                                    |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPMediaCollection2 介面 (VB 和 c # )**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist 介面 (VB 和 c # )**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





