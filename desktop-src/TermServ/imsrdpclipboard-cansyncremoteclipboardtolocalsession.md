---
title: IMsRdpClipboard CanSyncRemoteClipboardToLocalSession 方法
description: 指出遠端剪貼簿是否可同步處理至本機會話。
ms.tgt_platform: multiple
keywords:
- CanSyncRemoteClipboardToLocalSession 方法遠端桌面服務
- CanSyncRemoteClipboardToLocalSession 方法遠端桌面服務，IMsRdpClipboard 介面
- IMsRdpClipboard 介面遠端桌面服務，CanSyncRemoteClipboardToLocalSession 方法
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 40a9fc5d6dcdc2e96d9ce916bce0567cccc90adf10fcacc5d797f61ed292c116
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000838"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a>IMsRdpClipboard：： CanSyncRemoteClipboardToLocalSession 方法

指出遠端剪貼簿是否可同步處理至本機會話。

## <a name="syntax"></a>語法

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a>參數

如果遠端剪貼簿可以同步處理至本機會話，則為 **TRUE** ;否則 **為 FALSE**。

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