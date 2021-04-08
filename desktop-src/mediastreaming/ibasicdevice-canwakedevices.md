---
title: IBasicDevice CanWakeDevices 方法
description: 抓取值，指出裝置是否可以喚醒。
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- CanWakeDevices 方法媒體串流 API
- CanWakeDevices 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，CanWakeDevices 方法
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08a893ac880a426f604f2dc1c73173585e507cc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022542"
---
# <a name="ibasicdevicecanwakedevices-method"></a>IBasicDevice：： CanWakeDevices 方法

抓取值，指出裝置是否可以喚醒。

## <a name="syntax"></a>語法


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[擴展\]
</dt> <dd>

接收布林值的指標，如果裝置可以喚醒則為 **True** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





