---
title: BasicDevice 圖示屬性
description: 取得 IDeviceIcon 介面的向量。
ms.assetid: 54933FD0-27A6-48D8-A49A-200AD9214B9A
keywords:
- 圖示屬性媒體串流 API
- 圖示屬性媒體串流 API，BasicDevice 介面
- BasicDevice 介面媒體串流 API，圖示屬性
topic_type:
- apiref
api_name:
- BasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9807c41680c042ee74b2ddc659ad1558dd13ff8b4000d08cfa0591768c301bb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554658"
---
# <a name="basicdeviceicons-property"></a>BasicDevice 圖示屬性

取得 [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) 介面的向量。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="property-value"></a>屬性值

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)介面指標的可列舉集合。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

 