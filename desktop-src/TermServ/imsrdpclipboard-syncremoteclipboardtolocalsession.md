---
title: IMsRdpClipboard SyncRemoteClipboardToLocalSession 方法
description: 將遠端剪貼簿同步處理至本機會話。
ms.tgt_platform: multiple
keywords:
- SyncRemoteClipboardToLocalSession 方法遠端桌面服務
- SyncRemoteClipboardToLocalSession 方法遠端桌面服務，IMsRdpClipboard 介面
- IMsRdpClipboard 介面遠端桌面服務，SyncRemoteClipboardToLocalSession 方法
topic_type:
- apiref
api_name:
- IMsRdpClipboard.SyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d397d7c1ca4407a5125877721be9aa022f8132a7
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104509742"
---
# <a name="imsrdpclipboardsyncremoteclipboardtolocalsession-method"></a>IMsRdpClipboard：： SyncRemoteClipboardToLocalSession 方法

將遠端剪貼簿同步處理至本機會話。

## <a name="syntax"></a>語法

```C++
HRESULT SyncRemoteClipboardToLocalSession();
```

## <a name="parameters"></a>參數

這個方法沒有任何參數。

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