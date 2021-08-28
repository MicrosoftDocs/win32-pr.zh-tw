---
title: BasicDevice. CanWakeDevices 屬性
description: 取得值，這個值會指出裝置是否可以喚醒。
ms.assetid: 0BF0B2CD-E09E-4A0B-9D48-A980CBFE4233
keywords:
- CanWakeDevices 屬性媒體串流 API
- CanWakeDevices 屬性媒體串流 API，BasicDevice 介面
- BasicDevice 介面媒體串流 API，CanWakeDevices 屬性
topic_type:
- apiref
api_name:
- BasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37aba33168993df0e6e2853ea5bbc5f618863c3f025b28ab8ab98b81025486bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100900"
---
# <a name="basicdevicecanwakedevices-property"></a>BasicDevice. CanWakeDevices 屬性

取得值，這個值會指出裝置是否可以喚醒。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_CanWakeDevices(
  [out] boolean *value
);
```



## <a name="property-value"></a>屬性值

布林值的指標，如果裝置可以喚醒則為 **True** 。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))
</dt> </dl>

 

 