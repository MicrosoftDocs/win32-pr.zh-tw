---
description: SetUnsignedIntegerValue 方法會將新的 ULONG 值新增 (型別 VT \_ UI4) 或覆寫現有的值。
ms.assetid: 9b5d1b8c-7863-4807-a34b-56d30a47bd5c
title: 'IPortableDeviceValues：： SetUnsignedIntegerValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7dc237e5cdba120a08899035dc20f6fb6b2b63f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981282"
---
# <a name="iportabledevicevaluessetunsignedintegervalue-method"></a>IPortableDeviceValues：： SetUnsignedIntegerValue 方法

**SetUnsignedIntegerValue** 方法會將新的 **ULONG** 值新增 (型別 VT \_ UI4) 或覆寫現有的值。

## <a name="syntax"></a>語法


```C++
HRESULT SetUnsignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONG          Value
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

指定新值的 **ULONG** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

如果現有的值具有 *金鑰* 參數所指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。

## <a name="examples"></a>範例

如需如何使用此方法的範例，請參閱 [**指定用戶端資訊**](specifying-client-information.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md)
</dt> <dt>

[**指定用戶端資訊**](specifying-client-information.md)
</dt> </dl>

 

 




