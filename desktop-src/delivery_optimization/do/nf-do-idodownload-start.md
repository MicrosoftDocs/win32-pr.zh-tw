---
title: IDODownload：： Start 方法
description: 啟動或繼續進行下載。
keywords:
- IDODownload：： Start 方法
topic_type:
- apiref
api_name:
- IDODownload.Start
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: b2a06de8319ac07983fd13cb8523fa1dcf92365ca9275da80b699b290a4a6435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736255"
---
# <a name="idodownloadstart-method"></a>IDODownload：： Start 方法

啟動或繼續下載，將選擇性範圍傳遞為 [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) 結構的指標。

## <a name="syntax"></a>語法

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a>參數

`ranges`

選擇性。 [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md)結構的指標， (只下載檔案) 的特定範圍。 傳遞 `nullptr` 以下載整個檔案。

## <a name="return-value"></a>傳回值

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10 版本 1809 \[僅限 Win32 應用程式\] |
| **最低支援的伺服器** | WindowsServer，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | Do。h |
