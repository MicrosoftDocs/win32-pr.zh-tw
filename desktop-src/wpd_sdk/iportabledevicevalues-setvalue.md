---
description: SetValue 方法會加入新的 PROPVARIANT 值，或覆寫現有值。
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
title: 'IPortableDeviceValues：： SetValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 4c2ba6c5b6f015e5961356ff8e246605bfeddd31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990593"
---
# <a name="iportabledevicevaluessetvalue-method"></a>IPortableDeviceValues：： SetValue 方法

**SetValue** 方法會加入新的 **PROPVARIANT** 值，或覆寫現有值。

## <a name="syntax"></a>語法


```C++
HRESULT SetValue(
  [in]       REFPROPERTYKEY key,
  [in] const PROPVARIANT    *pValue
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

指定新值的 **PROPVARIANT** 。 SDK 會複製值，讓呼叫端可以在呼叫這個方法之後呼叫 **PropVariantClear** ，藉以釋放本機變數。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

當 *pValue* 的 VARTYPE 為 VT \_ VECTOR 或 vt \_ UI1 時，不支援設定 **Null** 或零大小的緩衝區。 例如，不允許使用 pValue. caub. pElems = **Null** 或 pValue. caub = 0。

這個方法可以用來從集合中取出任何型別的值。 但是，如果您事先知道值型別，請使用此介面的其中一個特製化 **Set ...** 方法，以避免直接使用 PROPVARIANT 值的額外負荷。

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

[**IPortableDeviceValues：： GetValue**](iportabledevicevalues-getvalue.md)
</dt> <dt>

[**IPortableDeviceValues::RemoveValue**](iportabledevicevalues-removevalue.md)
</dt> </dl>

 

 




