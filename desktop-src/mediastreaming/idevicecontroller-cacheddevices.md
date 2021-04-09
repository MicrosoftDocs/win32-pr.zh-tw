---
title: IDeviceController CachedDevices 方法
description: 抓取 IBasicDevice 介面指標的集合，表示所有可探索的 DLNA 裝置的快取視圖。 |IDeviceController CachedDevices 方法
ms.assetid: 94C2A7FF-5AF8-4F13-BBA5-54ED78C3BBF6
keywords:
- CachedDevices 方法媒體串流 API
- CachedDevices 方法媒體串流 API，IDeviceController 介面
- IDeviceController 介面媒體串流 API，CachedDevices 方法
topic_type:
- apiref
api_name:
- IDeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69be1faea277fa8999ae5ddf3658aaa61a1116b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103946016"
---
# <a name="idevicecontrollercacheddevices-method"></a>IDeviceController：： CachedDevices 方法

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



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDeviceController**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicecontroller)
</dt> </dl>

 

