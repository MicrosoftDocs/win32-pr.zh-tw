---
description: Add 方法會將專案加入至集合。
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: 'IPortableDeviceValuesCollection：： Add 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 1f423ac7243c8d16fa75978ae5c9bcf04136bb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993959"
---
# <a name="iportabledevicevaluescollectionadd-method"></a>IPortableDeviceValuesCollection：： Add 方法

**Add** 方法會將專案加入至集合。

## <a name="syntax"></a>語法


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pValues* \[在\]
</dt> <dd>

要加入至集合之 **IPortableDeviceValues** 介面的指標。 介面不會實際複製，但會在其上呼叫 **AddRef** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                   | Description                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 此方法已成功。<br/>                                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 沒有足夠的記憶體可將值新增至集合。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValuesCollection 介面**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




