---
title: DeviceDeparture 事件
description: 從 CachedDevices 方法傳回的裝置清單中移除新的裝置時發生。
ms.assetid: 10451878-e685-4042-9f92-ba3a408c4da0
keywords:
- DeviceDeparture 事件媒體串流 API
topic_type:
- apiref
api_name:
- DeviceDeparture
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e225afcbe8b373b22584eaa3d9fcb09e1eff29c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106966852"
---
# <a name="devicedeparture-event"></a>DeviceDeparture 事件

從 [**CachedDevices**](idevicecontroller-cacheddevices.md) 方法傳回的裝置清單中移除新的裝置時發生。

## <a name="syntax"></a>語法


```C++
void DeviceDeparture();
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

若要處理此事件的通知，請使用 [**add \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicedeparture)方法來註冊 [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))事件處理常式函式。 若要取消註冊事件處理常式，請使用 [**remove \_ DeviceDeparture**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicedeparture) 方法。

 

 