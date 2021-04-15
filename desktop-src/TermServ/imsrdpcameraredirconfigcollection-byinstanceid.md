---
title: IMsRdpCameraRedirConfigCollection ByInstanceId 屬性
description: 從集合中傳回對應至指定實例識別碼的 IMsRdpCameraRedirConfig 物件。
ms.tgt_platform: multiple
keywords:
- ByInstanceId 屬性遠端桌面服務
- ByInstanceId 屬性遠端桌面服務，IMsRdpCameraRedirConfigCollection 介面
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務，ByInstanceId 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByInstanceId
- IMsRdpCameraRedirConfigCollection.get_ByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d90cb7d2f309a3df9e354ace04a840b667e5569b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104467393"
---
# <a name="imsrdpcameraredirconfigcollectionbyinstanceid-property"></a>IMsRdpCameraRedirConfigCollection：： ByInstanceId 屬性

從集合中傳回對應至指定實例識別碼的 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法

```C++
HRESULT get_ByInstanceId(
    [in]          BSTR instanceId,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>屬性值

對應到指定實例識別碼的 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|---------------------------------------|
| 最低支援的用戶端| Windows 10 1803 版 (組建 17134)      |
| 類型程式庫            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection 定義為 AE45252B-AAAB-4504-B681-649D6073A37A          |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>