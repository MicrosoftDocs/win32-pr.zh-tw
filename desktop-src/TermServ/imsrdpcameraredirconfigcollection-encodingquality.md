---
title: IMsRdpCameraRedirConfigCollection EncodingQuality 屬性
description: 指定編碼品質 (位速率) 。
ms.tgt_platform: multiple
keywords:
- EncodingQuality 屬性遠端桌面服務
- EncodingQuality 屬性遠端桌面服務，IMsRdpCameraRedirConfigCollection 介面
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務，EncodingQuality 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodingQuality
- IMsRdpCameraRedirConfigCollection.put_EncodingQuality
- IMsRdpCameraRedirConfigCollection.get_EncodingQuality
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 94537773a54ddeb9bceb2483b7f8db6766f7b3f32f9a8a7fe2d9a24659209870
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574428"
---
# <a name="imsrdpcameraredirconfigcollectionencodingquality-property"></a>IMsRdpCameraRedirConfigCollection：： EncodingQuality 屬性

指定編碼品質 (位速率) 。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax

```C++
HRESULT put_EncodingQuality(
    [in] CameraRedirEncodingQuality encodingQuality
);

HRESULT get_EncodingQuality(
    [out, retval] CameraRedirEncodingQuality* pEncodingQuality
);
```

## <a name="property-value"></a>屬性值

下列其中一個 **CameraRedirEncodingQuality** 列舉值，指定編碼品質 (位速率) 。

| 列舉成員名稱 | 值 |
|-----------------|--------|
| encodingQualityLow | 0x0000 |
| encodingQualityMedium | 0x0001 |
| encodingQualityHigh | 0x0002 |

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