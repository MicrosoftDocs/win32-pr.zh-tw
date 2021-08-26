---
title: IMsRdpCameraRedirConfig DeviceExists 屬性
description: 指定相機裝置目前是否存在 (也就是相機連線) 。
ms.tgt_platform: multiple
keywords:
- DeviceExists 屬性遠端桌面服務
- DeviceExists 屬性遠端桌面服務，IMsRdpCameraRedirConfig 介面
- IMsRdpCameraRedirConfig 介面遠端桌面服務，DeviceExists 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.DeviceExists
- IMsRdpCameraRedirConfig.get_DeviceExists
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 617c91491d88736ca60218d71f9dd5aa02ad0f9faeefdda6b872ba9262cec587
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990658"
---
# <a name="imsrdpcameraredirconfigdeviceexists-property"></a>IMsRdpCameraRedirConfig：:D eviceExists 屬性

指定相機裝置目前是否存在 (也就是相機連線) 。

這個屬性是唯讀的。

## <a name="syntax"></a>語法

```C++
HRESULT get_DeviceExists(
    [out, retval] VARIANT_BOOL* pfExists
);
```

## <a name="property-value"></a>屬性值

值，指出攝影機裝置目前是否存在 (也就是相機連線) 。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|---------------------------------------|
| 最低支援的用戶端| Windows 10 1803 版 (組建 17134)      |
| 類型程式庫            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfig 定義為 09750604-D625-47C1-9FCD-F09F735705D7            |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
</dt> </dl>