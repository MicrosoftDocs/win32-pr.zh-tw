---
description: SetStringValue 方法會將新的字串值新增 (type VT \_ LPWSTR) 或覆寫現有的字串值。
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: 'IPortableDeviceValues：： SetStringValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 163b5cd81ce8da64fc6d9f4304de5783b248522f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981347"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a>IPortableDeviceValues：： SetStringValue 方法

**SetStringValue** 方法會將新的字串值新增 (type VT \_ LPWSTR) 或覆寫現有的字串值。

## <a name="syntax"></a>語法


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
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

指定新值的 **LPCWSTR** 。 會複製字串，讓呼叫端可以在呼叫這個方法之後釋放配置給這個值的記憶體。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

任何現有的金鑰記憶體都會適當地發行。

## <a name="examples"></a>範例

如需如何使用此方法的範例，請參閱 [指定用戶端資訊](specifying-client-information.md)。

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

[**IPortableDeviceValues：： GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[設定單一物件的屬性](setting-properties-for-a-single-object.md)
</dt> <dt>

[設定多個物件的屬性](setting-properties-for-multiple-objects.md)
</dt> <dt>

[指定用戶端資訊](specifying-client-information.md)
</dt> <dt>

[寫入內容物件屬性](writing-content-object-properties.md)
</dt> </dl>

 

 




