---
description: SetFloatValue 方法會將新的 FLOAT 值新增 (型別 VT \_ R4) 或覆寫現有的值。
ms.assetid: 1e0c9d19-47bf-4d93-a0c0-27e2c4897012
title: 'IPortableDeviceValues：： SetFloatValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 347cf93fe68e989eebb921472d1e81e4d0aa650e92d2c535dfdd93a6d823ed1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657808"
---
# <a name="iportabledevicevaluessetfloatvalue-method"></a>IPortableDeviceValues：： SetFloatValue 方法

**SetFloatValue** 方法會將新的 **FLOAT** 值新增 (型別 VT \_ R4) 或覆寫現有的值。

## <a name="syntax"></a>語法


```C++
HRESULT SetFloatValue(
  [in]       REFPROPERTYKEY key,
  [in] const FLOAT          Value
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

包含新值的 **浮點數** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

如果現有的值具有 *金鑰* 參數所指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetFloatValue**](iportabledevicevalues-getfloatvalue.md)
</dt> </dl>

 

 




