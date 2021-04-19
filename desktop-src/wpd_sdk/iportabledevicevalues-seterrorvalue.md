---
description: SetErrorValue 方法會新增 HRESULT 值 (type VT \_ ERROR) 或覆寫現有的值。
ms.assetid: 87369791-42bd-4523-b15a-acf0ea1e5af8
title: 'IPortableDeviceValues：： SetErrorValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 19c7ca57d325e31fd9cd8e0bf5130dc594b0b8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996212"
---
# <a name="iportabledevicevaluesseterrorvalue-method"></a>IPortableDeviceValues：： SetErrorValue 方法

**SetErrorValue** 方法會新增 **HRESULT** 值 (type VT \_ ERROR) 或覆寫現有的值。

## <a name="syntax"></a>語法


```C++
HRESULT SetErrorValue(
  [in]       REFPROPERTYKEY key,
  [in] const HRESULT        Value
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

包含新值的 **HRESULT** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

如果現有的值具有 *金鑰* 參數指定的相同索引鍵，則會覆寫現有的值，而不會出現任何警告。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetErrorValue**](iportabledevicevalues-geterrorvalue.md)
</dt> </dl>

 

 




