---
title: IDODownloadStatusCallback：： OnStatusChange 方法
description: 只要下載狀態變更，就會呼叫此方法的執行。
keywords:
- IDODownloadStatusCallback：： OnStatusChange 方法
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback.OnStatusChange
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 9abf13969a6183f98102792b9bcf7a3329ca243d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104022880"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a>IDODownloadStatusCallback：： OnStatusChange 方法

只要下載狀態變更，就會呼叫此方法的執行。

## <a name="syntax"></a>語法

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a>參數

`download`

**IDODownload** 介面的指標，其狀態已變更。

`status`

**DO_DOWNLOAD_STATUS** 結構的指標，其中包含下載的狀態。

## <a name="return-value"></a>傳回值

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | \[僅限 Windows 10 版本1809的 Win32 應用程式\] |
| **最低支援的伺服器** | Windows Server，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | Do。h |
