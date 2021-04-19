---
description: GetAt 方法會依據以零為基底的索引，從集合中抓取專案。
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: 'IPortableDevicePropVariantCollection：： GetAt 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0833c69b537fa230320ef69707a6f4302a8ca1ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992841"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a>IPortableDevicePropVariantCollection：： GetAt 方法

**GetAt** 方法會依據以零為基底的索引，從集合中抓取專案。

## <a name="syntax"></a>語法


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwIndex* \[在\]
</dt> <dd>

**DWORD** ，其中包含要抓取之專案的以零為基底的索引。

</dd> <dt>

*pValue* \[擴展\]
</dt> <dd>

**PROPVARIANT** 結構的指標。 呼叫端會負責呼叫 **PropVariantClear** 來釋出這個記憶體。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                  | Description                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法已成功。<br/>                          |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | 必要的指標引數為 **Null**。<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 傳入的索引超出範圍。<br/> |



 

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

[從持續性唯一識別碼中取出物件識別碼](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[正在抓取支援的服務事件](retrieving-supported-events.md)
</dt> <dt>

[正在抓取支援的服務格式](retrieving-supported-formats.md)
</dt> <dt>

[正在抓取支援的服務方法](retrieving-supported-methods.md)
</dt> <dt>

[正在抓取裝置支援的內容類型](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[正在抓取裝置支援的功能分類](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[正在抓取裝置的功能物件識別碼](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[正在抓取裝置所支援的轉譯功能](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[設定多個物件的屬性](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




