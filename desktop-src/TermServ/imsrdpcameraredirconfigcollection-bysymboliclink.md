---
title: IMsRdpCameraRedirConfigCollection BySymbolicLink 屬性
description: 從集合中傳回 IMsRdpCameraRedirConfig 物件，這個集合會對應至相機的 **KSCATEGORY_VIDEO_CAMERA** 介面之指定符號連結。
ms.tgt_platform: multiple
keywords:
- BySymbolicLink 屬性遠端桌面服務
- BySymbolicLink 屬性遠端桌面服務，IMsRdpCameraRedirConfigCollection 介面
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務，BySymbolicLink 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.BySymbolicLink
- IMsRdpCameraRedirConfigCollection.get_BySymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: a46cd3daf8cc4270473433bb0c4c20dee0616dba3619b056d33136e0d4dd8f5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033628"
---
# <a name="imsrdpcameraredirconfigcollectionbysymboliclink-property"></a>IMsRdpCameraRedirConfigCollection::.BySymbolicLink 屬性

從集合中傳回 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件，這個集合會對應至相機的 **KSCATEGORY_VIDEO_CAMERA** 介面之指定符號連結。

這個屬性是唯讀的。

## <a name="syntax"></a>語法

```C++
HRESULT get_BySymbolicLink(
    [in]          BSTR symbolicLink,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a>屬性值

對應到指定符號連結的 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件。

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