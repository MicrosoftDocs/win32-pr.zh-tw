---
description: GetCount 方法會抓取此集合中的專案數。
ms.assetid: b7c8acd2-67f2-47d3-b42a-26aa701fd613
title: 'IPortableDevicePropVariantCollection：： GetCount 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d3a06cb5d89bc09a35a58f9269ba19c488c11e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990547"
---
# <a name="iportabledevicepropvariantcollectiongetcount-method"></a>IPortableDevicePropVariantCollection：： GetCount 方法

**GetCount** 方法會抓取此集合中的專案數。

## <a name="syntax"></a>語法


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcElems* \[在\]
</dt> <dd>

**DWORD** 的指標，其中包含集合中的專案數。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                               | Description                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 此方法已成功。<br/>                     |
| <dl> <dt>**E \_ 指標**</dt> </dl> | 必要的指標引數為 **Null**。<br/> |



 

## <a name="examples"></a>範例

如需如何使用此方法的範例，請參閱抓取 [裝置所支援的功能分類](retrieving-the-functional-categories-supported-by-a-device.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[正在抓取支援的服務事件](retrieving-supported-events.md)
</dt> <dt>

[正在抓取支援的服務格式](retrieving-supported-formats.md)
</dt> <dt>

[正在抓取支援的服務方法](retrieving-supported-methods.md)
</dt> <dt>

[正在抓取裝置支援的功能分類](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[設定多個物件的屬性](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




