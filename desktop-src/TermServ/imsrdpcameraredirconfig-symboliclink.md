---
title: IMsRdpCameraRedirConfig >symboliclink 屬性
description: 取得相機之 **KSCATEGORY_VIDEO_CAMERA** 介面的符號連結。
ms.tgt_platform: multiple
keywords:
- '>symboliclink 屬性遠端桌面服務'
- '>symboliclink 屬性遠端桌面服務，IMsRdpCameraRedirConfig 介面'
- IMsRdpCameraRedirConfig 介面遠端桌面服務，>symboliclink 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.SymbolicLink
- IMsRdpCameraRedirConfig.SymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 439ead6fa0868887cc5965205b22236abb5aada6
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "103845659"
---
# <a name="imsrdpcameraredirconfigsymboliclink-property"></a>IMsRdpCameraRedirConfig：： >symboliclink 屬性

取得相機之 **KSCATEGORY_VIDEO_CAMERA** 介面的符號連結。

這個屬性是唯讀的。

## <a name="syntax"></a>語法

```C++
HRESULT get_SymbolicLink(
    [out, retval] BSTR* pSymbolicLink
);
```

## <a name="property-value"></a>屬性值

攝影機 **KSCATEGORY_VIDEO_CAMERA** 介面的符號連結。

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