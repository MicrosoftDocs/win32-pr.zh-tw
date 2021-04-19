---
description: CopyValuesToPropertyStore 方法會將集合中的所有值複製到 IPropertyStore 介面中。
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
title: 'IPortableDeviceValues：： CopyValuesToPropertyStore 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesToPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d6ab6b4614c336d3e0da50c0291b2e69a260ae1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978428"
---
# <a name="iportabledevicevaluescopyvaluestopropertystore-method"></a>IPortableDeviceValues：： CopyValuesToPropertyStore 方法

**CopyValuesToPropertyStore** 方法會將集合中的所有值複製到 **IPropertyStore** 介面中。

## <a name="syntax"></a>語法


```C++
HRESULT CopyValuesToPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStore* \[在\]
</dt> <dd>

存放區物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

這個方法不會將 VT LPWSTR 的值轉換 \_ 成 vt \_ BSTR。 許多與您的應用程式通訊的外部應用程式或元件（例如某些 shell 應用程式）都會使用 **IPropertyStore** 介面。 這種方法可讓您快速輕鬆地與這些程式交換資料。

Windows Vista 和更新版本的 Windows 中支援這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::CopyValuesFromPropertyStore**](iportabledevicevalues-copyvaluesfrompropertystore.md)
</dt> </dl>

 

 




