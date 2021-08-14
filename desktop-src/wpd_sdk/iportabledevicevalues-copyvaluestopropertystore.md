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
ms.openlocfilehash: 2d134cb61831426451b1c6068bde5ca787b027fbe5b153587b45d9693ef739c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697245"
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



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

這個方法不會將 VT LPWSTR 的值轉換 \_ 成 vt \_ BSTR。 許多與您的應用程式通訊的外部應用程式或元件（例如某些 shell 應用程式）都會使用 **IPropertyStore** 介面。 這種方法可讓您快速輕鬆地與這些程式交換資料。

Windows Vista 和更新版本的 Windows 支援此方法。

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

 

 




