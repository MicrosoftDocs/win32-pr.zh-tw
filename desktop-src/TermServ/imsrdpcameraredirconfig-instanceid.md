---
title: IMsRdpCameraRedirConfig InstanceId 屬性
description: 取得相機的實例識別碼。
ms.tgt_platform: multiple
keywords:
- InstanceId 屬性遠端桌面服務
- InstanceId 屬性遠端桌面服務，IMsRdpCameraRedirConfig 介面
- IMsRdpCameraRedirConfig 介面遠端桌面服務，InstanceId 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.InstanceId
- IMsRdpCameraRedirConfig.get_InstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 621c865f9727cf484430d00609dcfcfac2431a514cf2bade714fdd4d81b0408c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400998"
---
# <a name="imsrdpcameraredirconfiginstanceid-property"></a>IMsRdpCameraRedirConfig：： InstanceId 屬性

取得相機的實例識別碼。

這個屬性是唯讀的。

## <a name="syntax"></a>語法

```C++
HRESULT get_InstanceId(
    [out, retval] BSTR* pInstanceId
);
```

## <a name="property-value"></a>屬性值

攝影機的實例識別碼。

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