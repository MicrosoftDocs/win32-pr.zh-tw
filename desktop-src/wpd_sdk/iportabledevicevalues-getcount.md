---
description: IPortableDeviceValues：： GetCount 方法-GetCount 方法會抓取集合中的專案數。
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
title: 'IPortableDeviceValues：： GetCount 方法 (PortableDeviceTypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b7a2f1f71f81296f56be779a4c6eea746ebd0963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086236"
---
# <a name="iportabledevicevaluesgetcount-method"></a>IPortableDeviceValues：： GetCount 方法

**GetCount** 方法會抓取集合中的專案數。

## <a name="syntax"></a>語法


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcelt* \[在\]
</dt> <dd>

**DWORD** 的指標，其中包含集合中的專案數。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>PortableDeviceTypes。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>PortableDeviceGUIDs .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPortableDeviceValues 介面**](iportabledevicevalues.md)
</dt> </dl>

 

 




