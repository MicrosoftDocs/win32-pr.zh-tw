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
ms.openlocfilehash: 3ebd0cfe9bf773d78297454d4a7643a74c3d6ea23aea01eeb54cd5c014ce73e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847668"
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



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBasicDevice**](ibasicdevice.md)
</dt> </dl>

 

 





