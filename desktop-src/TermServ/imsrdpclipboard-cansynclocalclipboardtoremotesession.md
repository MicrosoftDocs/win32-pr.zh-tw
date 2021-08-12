---
title: IMsRdpClipboard CanSyncLocalClipboardToRemoteSession 方法
description: 指出本機剪貼簿是否可以同步到遠端會話。
ms.tgt_platform: multiple
keywords:
- CanSyncLocalClipboardToRemoteSession 方法遠端桌面服務
- CanSyncLocalClipboardToRemoteSession 方法遠端桌面服務，IMsRdpClipboard 介面
- IMsRdpClipboard 介面遠端桌面服務，CanSyncLocalClipboardToRemoteSession 方法
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: dabc12064ff43a2bb64a562d1aa3050681f46c31dd2698154beb1dafe3cfd85e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606913"
---
# <a name="imsrdpclipboardcansynclocalclipboardtoremotesession-method"></a>IMsRdpClipboard：： CanSyncLocalClipboardToRemoteSession 方法

指出本機剪貼簿是否可以同步到遠端會話。

## <a name="syntax"></a>語法

```C++
HRESULT CanSyncLocalClipboardToRemoteSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>參數

如果本機剪貼簿可以同步到遠端會話，則 **為 TRUE** ;否則 **為 FALSE**。

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|---------------------------------------|
| 最低支援的用戶端| Windows 10 1803 版 (組建 17134)      |
| 類型程式庫            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClipboard 定義為2E769EE8-00C7-43DC-AFD9-235D75B72A40          |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClipboard**](imsrdpclipboard.md)
</dt> </dl>