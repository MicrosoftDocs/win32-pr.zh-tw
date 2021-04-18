---
title: IDODownload：： Abort 方法
description: 中止下載。
keywords:
- IDODownload：： Abort 方法
topic_type:
- apiref
api_name:
- IDODownload.Abort
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: babcd5ee00689ac103288074467980777f644668
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "106968476"
---
# <a name="idodownloadabort-method"></a>IDODownload：： Abort 方法

中止下載。

## <a name="syntax"></a>語法

```cpp
HRESULT Abort();
```

## <a name="return-value"></a>傳回值

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | \[僅限 Windows 10 版本1809的 Win32 應用程式\] |
| **最低支援的伺服器** | Windows Server，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | Do。h |
