---
description: GetValue 方法會抓取索引鍵所指定的 PROPVARIANT 值。
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
title: 'IPortableDeviceValues：： GetValue 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 6ab5ec24e67d5259eec86c6a33d32766a5426b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993988"
---
# <a name="iportabledevicevaluesgetvalue-method"></a>IPortableDeviceValues：： GetValue 方法

**GetValue** 方法會抓取索引鍵所指定的 **PROPVARIANT** 值。

## <a name="syntax"></a>語法


```C++
HRESULT GetValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPVARIANT    *pValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

指定要取出之專案的 **REFPROPERTYKEY** 索引鍵。

</dd> <dt>

*pValue* \[擴展\]
</dt> <dd>

已抓取 **PROPVARIANT** 值的指標。 呼叫端完成時，必須呼叫 **PropVariantClear** 來釋放記憶體。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                                            | Description                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                   | 此方法已成功。<br/>                                     |
| <dl> <dt>**\_ \_ \_ 找不到 WIN32 (錯誤 \_) 的 HRESULT**</dt> </dl> | 索引 *鍵* 所指定的屬性不在集合中。<br/> |



 

## <a name="remarks"></a>備註

當 *pValue* 的 VARTYPE 為 VT \_ VECTOR 或 vt \_ UI1 時，不支援取出 **Null** 或零大小的緩衝區。 例如，不允許使用 pValue. caub. pElems = **Null** 或 pValue. caub = 0。

這個方法可以用來從集合中取出任何型別的值。 但是，如果您事先知道值型別，請使用此介面的其中一個特製化抓取方法，以避免直接使用 PROPVARIANT 值的額外負荷。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::RemoveValue**](iportabledevicevalues-removevalue.md)
</dt> <dt>

[**IPortableDeviceValues：： SetValue**](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




