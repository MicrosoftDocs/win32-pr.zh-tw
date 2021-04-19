---
description: SetIPortableDeviceKeyCollectionValue 方法會將新的 SetIPortableDeviceKeyCollectionValue 值新增 (type VT \_ UNKNOWN) 或覆寫現有的值。
ms.assetid: f470cb89-e7a0-470d-83d1-eb643b062e45
title: 'IPortableDeviceValues：： SetIPortableDeviceKeyCollectionValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: face82230b9dd3bf6cbde18aaee8dd857e17d0a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984021"
---
# <a name="iportabledevicevaluessetiportabledevicekeycollectionvalue-method"></a>IPortableDeviceValues：： SetIPortableDeviceKeyCollectionValue 方法

**SetIPortableDeviceKeyCollectionValue** 方法會將新的 **SetIPortableDeviceKeyCollectionValue** 值新增 (type VT \_ UNKNOWN) 或覆寫現有的值。

## <a name="syntax"></a>語法


```C++
HRESULT SetIPortableDeviceKeyCollectionValue(
  [in] REFPROPERTYKEY               key,
  [in] IPortableDeviceKeyCollection *pValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

指定要建立或覆寫之專案的 **REFPROPERTYKEY** 。

</dd> <dt>

*pValue* \[在\]
</dt> <dd>

**IPortableDeviceKeyCollection** 介面的指標，指定新的值。 SDK 會將參考複製到已提交的介面，並在其上呼叫 **AddRef** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

如果現有的值具有 *金鑰* 參數所指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。 會適當地釋放現有的金鑰記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)
</dt> </dl>

 

 




