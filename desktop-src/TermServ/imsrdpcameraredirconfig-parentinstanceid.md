---
title: IMsRdpCameraRedirConfig ParentInstanceId 屬性
description: 取得相機的父裝置實例識別碼。
ms.tgt_platform: multiple
keywords:
- ParentInstanceId 屬性遠端桌面服務
- ParentInstanceId 屬性遠端桌面服務，IMsRdpCameraRedirConfig 介面
- IMsRdpCameraRedirConfig 介面遠端桌面服務，ParentInstanceId 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.ParentInstanceId
- IMsRdpCameraRedirConfig.get_ParentInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 149e4f536996376193596db6c4fd4cf659637c05bb92e3afcdb7ee78c480b893
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574558"
---
# <a name="imsrdpcameraredirconfigparentinstanceid-property"></a>IMsRdpCameraRedirConfig：:P arentInstanceId 屬性

取得相機的父裝置實例識別碼。

這個屬性是唯讀的。

## <a name="syntax"></a>語法

```C++
HRESULT get_ParentInstanceId(
    [out, retval] BSTR* pParentInstanceId
);
```

## <a name="property-value"></a>屬性值

相機的父裝置實例識別碼。

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