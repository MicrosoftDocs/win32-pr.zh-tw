---
title: IMsRdpCameraRedirConfig 重新導向屬性
description: 指定是否將相機重新導向。
ms.tgt_platform: multiple
keywords:
- 重新導向的屬性遠端桌面服務
- 重新導向的屬性遠端桌面服務，IMsRdpCameraRedirConfig 介面
- IMsRdpCameraRedirConfig 介面遠端桌面服務，重新導向的屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.Redirected
- IMsRdpCameraRedirConfig.put_Redirected
- IMsRdpCameraRedirConfig.get_Redirected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: f81dc643f7911029df088bbb692d7c8c06fddac4
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104467400"
---
# <a name="imsrdpcameraredirconfigredirected-property"></a>IMsRdpCameraRedirConfig：：重新導向的屬性

指定是否將相機重新導向。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax

```C++
HRESULT put_Redirected(
    [in] VARIANT_BOOL fRedirected
);

HRESULT get_Redirected(
    [out, retval] VARIANT_BOOL* pfRedirected
);
```

## <a name="property-value"></a>屬性值

值，指定是否重新導向相機。

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