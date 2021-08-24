---
title: DeviceArrival 事件
description: 當新的裝置新增至 CachedDevices 方法所傳回的裝置清單時發生。
ms.assetid: C7CB49AE-C05F-4A2A-8A30-4B4BB7C7D9D2
keywords:
- DeviceArrival 事件媒體串流 API
topic_type:
- apiref
api_name:
- DeviceArrival
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed65c2b1c37eb91f9bf0a0c060fb76b85cd1f5b3d06b6ff1ab795ec89a0db6bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721208"
---
# <a name="devicearrival-event"></a>DeviceArrival 事件

當新的裝置新增至 [**CachedDevices**](idevicecontroller-cacheddevices.md) 方法所傳回的裝置清單時發生。

## <a name="syntax"></a>語法


```C++
void DeviceArrival();
```



## <a name="parameters"></a>參數

此事件沒有任何參數。

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

若要處理此事件的通知，請使用 [**add \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-add_devicearrival)方法來註冊 [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))事件處理常式函式。 若要取消註冊事件處理常式，請使用 [**remove \_ DeviceArrival**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-idevicecontroller-remove_devicearrival) 方法。

 

 