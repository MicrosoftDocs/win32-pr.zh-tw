---
description: IPortableDevicePropVariantCollection：： RemoveAt 方法-RemoveAt 方法會移除儲存在指定索引所指定之位置的元素。
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: 'IPortableDevicePropVariantCollection：： RemoveAt 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5c62df57a95a9f5a8238ff61c4ca6dc3cb73ed36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109939"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a>IPortableDevicePropVariantCollection：： RemoveAt 方法

**RemoveAt** 方法會移除儲存在指定索引所指定之位置的元素。

## <a name="syntax"></a>語法


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwIndex* \[在\]
</dt> <dd>

指定要移除之元素的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                  | Description                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法已成功。<br/>                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 指定的索引超出範圍。<br/> |



 

## <a name="remarks"></a>備註

您必須指定以零為基底的索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




