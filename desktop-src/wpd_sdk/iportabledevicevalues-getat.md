---
description: GetAt 方法會使用提供的以零為基底的索引，從集合中抓取值。
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: 'IPortableDeviceValues：： GetAt 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 4e234d0fe24eec947b388b5da798c55e7478ffa6bda69a9b9fe57c279af6d96e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843021"
---
# <a name="iportabledevicevaluesgetat-method"></a>IPortableDeviceValues：： GetAt 方法

**GetAt** 方法會使用提供的以零為基底的索引，從集合中抓取值。

## <a name="syntax"></a>語法


```C++
HRESULT GetAt(
  [in]      const DWORD       index,
  [in, out]       PROPERTYKEY *pKey,
  [in, out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

**DWORD** ，指定集合中以零為基底的索引。

</dd> <dt>

*pKey* \[in、out\]
</dt> <dd>

選擇性的 **PROPERTYKEY** 指標，可抓取指定專案的索引鍵。

</dd> <dt>

*pValue* \[in、out\]
</dt> <dd>

可抓取指定專案值的選擇性 **PROPVARIANT** 。 呼叫端完成時，必須呼叫 **PropVariantClear** 來釋放記憶體。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                  | 描述                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法已成功。<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 指定了不正確索引編號。<br/> |



 

## <a name="remarks"></a>備註

如果屬性工作表示 VT 不明類型的值 \_ ，則此屬性會是 Windows 的可攜式裝置之一 ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)、 [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)、 [**IPortableDeviceValues**](iportabledevicevalues.md)或 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)) 。 Windows 可攜式裝置無法傳回其他介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues：： GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




