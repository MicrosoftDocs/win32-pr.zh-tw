---
description: GetType 方法會抓取集合中專案的資料類型。
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
title: 'IPortableDevicePropVariantCollection：： GetType 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: de5ea5b1eeaa9cf494c24e13b8b9b36f7490b84d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982957"
---
# <a name="iportabledevicepropvariantcollectiongettype-method"></a>IPortableDevicePropVariantCollection：： GetType 方法

**GetType** 方法會抓取集合中專案的資料類型。

## <a name="syntax"></a>語法


```C++
HRESULT GetType(
  [out] VARTYPE *pvt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pvt* \[擴展\]
</dt> <dd>

Platform SDK **VARTYPE** 列舉值，指出集合中所有專案的資料類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                               | Description                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 此方法已成功。<br/>                     |
| <dl> <dt>**E \_ 指標**</dt> </dl> | 必要的指標引數為 **Null**。<br/> |



 

## <a name="remarks"></a>備註

儲存在 **IPortableDevicePropVariantCollection** 中的所有專案都是相同的類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




