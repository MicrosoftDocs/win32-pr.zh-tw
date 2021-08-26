---
title: IMsRdpCameraRedirConfigCollection AddConfig 方法
description: 將 IMsRdpCameraRedirConfig 物件新增至集合 (對應的相機不需要連線) 。
ms.tgt_platform: multiple
keywords:
- AddConfig 方法遠端桌面服務
- AddConfig 方法遠端桌面服務，IMsRdpCameraRedirConfigCollection 介面
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務，AddConfig 方法
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.AddConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 88d4f7952497ca0afd970a979441f98864b2855ed3f36f3e556dc4241ed52769
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033648"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a>IMsRdpCameraRedirConfigCollection：： AddConfig 方法

將 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件新增至集合 (對應的相機不需要連線) 。

## <a name="syntax"></a>語法

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a>參數

*>symboliclink* \[在\]

新 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件的符號連結。

*fRedirected* \[在\]

指定是否預設會重新導向新的相機。

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。

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