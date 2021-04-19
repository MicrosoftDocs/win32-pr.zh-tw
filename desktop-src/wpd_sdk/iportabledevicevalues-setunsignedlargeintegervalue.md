---
description: SetUnsignedLargeIntegerValue 方法會將新的 ULONGLONG 值新增 (type VT \_ UI8) 或覆寫現有的值。
ms.assetid: 64874b86-7bf1-407a-8fff-a2c07c22f0cb
title: 'IPortableDeviceValues：： SetUnsignedLargeIntegerValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c1ade76b4242c7508cb325e90c567349afcdc9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992874"
---
# <a name="iportabledevicevaluessetunsignedlargeintegervalue-method"></a>IPortableDeviceValues：： SetUnsignedLargeIntegerValue 方法

**SetUnsignedLargeIntegerValue** 方法會將新的 **ULONGLONG** 值新增 (type VT \_ UI8) 或覆寫現有的值。

## <a name="syntax"></a>語法


```C++
HRESULT SetUnsignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONGLONG      Value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。

</dd> <dt>

*值* \[在\]
</dt> <dd>

指定新值的 **ULONGLONG** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[將資源新增至物件](adding-a-resource-to-an-object.md)
</dt> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetUnsignedLargeIntegerValue**](iportabledevicevalues-getunsignedlargeintegervalue.md)
</dt> </dl>

 

 




