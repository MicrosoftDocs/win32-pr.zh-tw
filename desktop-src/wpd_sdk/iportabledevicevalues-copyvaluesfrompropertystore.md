---
description: CopyValuesFromPropertyStore 方法會將 IPropertyStore 的內容複寫到集合中。
ms.assetid: 887c9569-ff76-41cf-8782-62c59c04e831
title: 'IPortableDeviceValues：： CopyValuesFromPropertyStore 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesFromPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fbc2508d300fe4d0680d539153fde5f86603e04d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995389"
---
# <a name="iportabledevicevaluescopyvaluesfrompropertystore-method"></a>IPortableDeviceValues：： CopyValuesFromPropertyStore 方法

**CopyValuesFromPropertyStore** 方法會將 **IPropertyStore** 的內容複寫到集合中。

## <a name="syntax"></a>語法


```C++
HRESULT CopyValuesFromPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStore* \[在\]
</dt> <dd>

要複製到集合中之 **IPropertyStore** 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

這個方法會自動將所有 **VT \_ BSTR** 值轉換成 **VT \_ LPWSTR** 值。

許多與您的應用程式通訊的外部應用程式或元件（例如某些 shell 應用程式）都會使用 **IPropertyStore** 介面。 這種方法可讓您快速輕鬆地與這些程式交換資料。

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

[**IPortableDeviceValues::CopyValuesToPropertyStore**](iportabledevicevalues-copyvaluestopropertystore.md)
</dt> </dl>

 

 




