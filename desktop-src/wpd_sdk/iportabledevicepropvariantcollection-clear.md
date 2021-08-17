---
description: Clear 方法會釋出並移除集合中的所有專案。 呼叫這個方法之後，會將集合視為空白。
ms.assetid: f4b46713-8224-443a-99cc-13fa75e59e5d
title: 'IPortableDevicePropVariantCollection：： Clear 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0cec3f12757fe43c408488204de8b0dd95d5e95c75d8315ea758e4311ff5e9bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194136"
---
# <a name="iportabledevicepropvariantcollectionclear-method"></a>IPortableDevicePropVariantCollection：： Clear 方法

**Clear** 方法會釋出並移除集合中的所有專案。 呼叫這個方法之後，會將集合視為空白。

## <a name="syntax"></a>語法


```C++
HRESULT Clear();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

在呼叫 **Clear** 之後，集合會被視為不具型別，表示它先前設定的 VARTYPE 不再限制 **加入** 作業。 呼叫 **Clear** 之後要 **加入** 的呼叫會被視為此集合的「第一個」**加入**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDevicePropVariantCollection 介面**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




