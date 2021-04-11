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
ms.openlocfilehash: bdd0235a2b07ea86cbace87defb92f44d6b42315
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375257"
---
# <a name="basicdeviceicons-property"></a>BasicDevice 圖示屬性

取得 [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) 介面的向量。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="property-value"></a>屬性值

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)介面指標的可列舉集合。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

 