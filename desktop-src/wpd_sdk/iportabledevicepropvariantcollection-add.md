---
description: Add 方法會將專案加入至集合。
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: 'IPortableDevicePropVariantCollection：： Add 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d9d5b4ee664d2fbbcc78550b1af5a48874d153d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994770"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a>IPortableDevicePropVariantCollection：： Add 方法

**Add** 方法會將專案加入至集合。

## <a name="syntax"></a>語法


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pValue* \[在\]
</dt> <dd>

要加入至集合之新 **PROPVARIANT** 物件的指標。 這個方法會將 **PROPVARIANT** 複製到集合中，因此您應該在呼叫這個方法之後，呼叫 **PropVariantClear** 來釋放變數的本機複本。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

當 *pValue* 的 VARTYPE 為 VT \_ VECTOR 或 vt \_ UI1 時，不支援設定和取出 **Null** 或零大小的緩衝區。 例如，不允許使用 pValue. caub. pElems = **Null** 或 pValue. caub = 0。

如果呼叫端嘗試加入集合中包含之不同 VARTYPE 的專案，而且這個介面無法自動變更 PROPVARIANT 值，此方法將會失敗。 若要手動變更集合類型，請呼叫 [**IPortableDevicePropVariantCollection：： ChangeType**](iportabledevicepropvariantcollection-changetype.md)。

## <a name="examples"></a>範例

如需如何使用此方法的範例，請參閱[從持續性唯一識別碼抓取物件識別碼](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[移動裝置上的內容](moving-content-on-the-device.md)
</dt> <dt>

[從持續性唯一識別碼中取出物件識別碼](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




