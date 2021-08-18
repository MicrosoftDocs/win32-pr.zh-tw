---
description: ChangeType 方法會將集合中的所有專案轉換為指定的 VARTYPE。
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
title: 'IPortableDevicePropVariantCollection：： ChangeType 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.ChangeType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f32670883981abdac56d46424d8ff18d82cf9fbe0e8a3d2222efede797ffb43d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839328"
---
# <a name="iportabledevicepropvariantcollectionchangetype-method"></a>IPortableDevicePropVariantCollection：： ChangeType 方法

**ChangeType** 方法會將集合中的所有專案轉換為指定的 VARTYPE。

## <a name="syntax"></a>語法


```C++
HRESULT ChangeType(
  [in] const VARTYPE vt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*vt* \[在\]
</dt> <dd>

指定要將集合中的所有專案轉換成的 **VARTYPE** 。 範例類型包括 VT \_ UI4 和 vt \_ UI8。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

如果此方法失敗，則集合可能會保持為中繼狀態，而某些成員會進行轉換，而且不會轉換。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




