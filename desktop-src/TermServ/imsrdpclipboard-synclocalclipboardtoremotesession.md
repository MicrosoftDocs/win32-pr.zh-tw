---
title: IMsRdpClipboard SyncLocalClipboardToRemoteSession 方法
description: 將本機剪貼簿同步到遠端會話。
ms.tgt_platform: multiple
keywords:
- SyncLocalClipboardToRemoteSession 方法遠端桌面服務
- SyncLocalClipboardToRemoteSession 方法遠端桌面服務，IMsRdpClipboard 介面
- IMsRdpClipboard 介面遠端桌面服務，SyncLocalClipboardToRemoteSession 方法
topic_type:
- apiref
api_name:
- IMsRdpClipboard.SyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 516782dcb86dd02b0d3fd31fee5cc463a64b0e86726c826a855e245f37ba5908
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606903"
---
# <a name="imsrdpclipboardsynclocalclipboardtoremotesession-method"></a>IMsRdpClipboard：： SyncLocalClipboardToRemoteSession 方法

將本機剪貼簿同步到遠端會話。

## <a name="syntax"></a>語法

```C++
HRESULT SyncLocalClipboardToRemoteSession();
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
