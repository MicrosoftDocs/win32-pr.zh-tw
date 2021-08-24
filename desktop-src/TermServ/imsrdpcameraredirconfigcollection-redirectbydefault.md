---
title: IMsRdpCameraRedirConfigCollection RedirectByDefault 屬性
description: 指定是否根據預設，將任何新的相機重新導向。
ms.tgt_platform: multiple
keywords:
- RedirectByDefault 屬性遠端桌面服務
- RedirectByDefault 屬性遠端桌面服務，IMsRdpCameraRedirConfigCollection 介面
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務，RedirectByDefault 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.RedirectByDefault
- IMsRdpCameraRedirConfigCollection.put_RedirectByDefault
- IMsRdpCameraRedirConfigCollection.get_RedirectByDefault
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 8c95431132acf5e3c08ede859520c844c4cae542f6b07dcb8e5781726078e754
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475868"
---
# <a name="imsrdpcameraredirconfigcollectionredirectbydefault-property"></a>IMsRdpCameraRedirConfigCollection：： RedirectByDefault 屬性

指定是否根據預設，將任何新的相機重新導向。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax

```C++
HRESULT put_RedirectByDefault(
    [in] VARIANT_BOOL fRedirect
);

HRESULT get_RedirectByDefault(
    [out, retval] VARIANT_BOOL* pfRedirect
);
```

## <a name="property-value"></a>屬性值

值，指出是否根據預設，將任何新的相機重新導向。

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