---
title: IDODownload：： GetStatus 方法
description: 抓取 **DO_DOWNLOAD_STATUS** 結構的指標，此結構會反映下載的目前狀態。
keywords:
- IDODownload：： GetStatus 方法
topic_type:
- apiref
api_name:
- IDODownload.GetStatus
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e3a5aec5e35187a51865e074dae26ff012b75dfa3a41ffd13a8bed7371515fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047106"
---
# <a name="idodownloadgetstatus-method"></a>IDODownload：： GetStatus 方法

抓取 **DO_DOWNLOAD_STATUS** 結構的指標，此結構會反映下載的目前狀態。

## <a name="syntax"></a>語法

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>參數

`status`

**DO_DOWNLOAD_STATUS** 結構的指標。

## <a name="return-value"></a>傳回值

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10 版本 1809 \[僅限 Win32 應用程式\] |
| **最低支援的伺服器** | WindowsServer，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | Do。h |
