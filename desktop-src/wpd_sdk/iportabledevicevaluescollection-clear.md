---
description: Clear 方法會釋放集合中的所有專案。
ms.assetid: 151d1f61-11f0-40f0-8da1-79e9eb2001ce
title: 'IPortableDeviceValuesCollection：： Clear 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 4cc810ae7871ffcd5bffc50eabda8682f1d2cd334d6e0b09fac715d3749f300d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697022"
---
# <a name="iportabledevicevaluescollectionclear-method"></a>IPortableDeviceValuesCollection：： Clear 方法

**Clear** 方法會釋放集合中的所有專案。

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

方法會釋放配置給集合中專案的所有記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValuesCollection 介面**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




