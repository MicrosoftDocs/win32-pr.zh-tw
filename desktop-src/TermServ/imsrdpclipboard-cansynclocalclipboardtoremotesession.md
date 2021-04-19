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
ms.openlocfilehash: d2dd6fa5fc4d442d7cc22f036c293ebfaba841b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "106973933"
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