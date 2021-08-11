---
title: DeviceController. CachedDevices 方法
description: 抓取 IBasicDevice 介面指標的集合，表示所有可探索的 DLNA 裝置的快取視圖。 |DeviceController. CachedDevices 方法
ms.assetid: 89CFA4BB-EDA8-461A-A3A0-A84CBDA99EA4
keywords:
- CachedDevices 方法媒體串流 API
- CachedDevices 方法媒體串流 API，DeviceController 介面
- DeviceController 介面媒體串流 API，CachedDevices 方法
topic_type:
- apiref
api_name:
- DeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 86e2c4209649450fb3a8df46cde151a0b9899cd26e58bfc0b35fd7ac6e7d02b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236358"
---
# <a name="devicecontrollercacheddevices-method"></a>DeviceController. CachedDevices 方法

抓取 [**IBasicDevice**](ibasicdevice.md) 介面指標的集合，表示所有可探索的 DLNA 裝置的快取視圖。

## <a name="syntax"></a>語法


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收 [**IBasicDevice**](ibasicdevice.md) 介面指標的可列舉集合。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))
</dt> </dl>

 

