---
title: IDODownload：： GetProperty 方法
description: 抓取包含特定下載屬性之 **變數** 的指標。
keywords:
- IDODownload：： GetProperty 方法
topic_type:
- apiref
api_name:
- IDODownload.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: f498900e8dd2e87460a5fe4e75ea1269272788488159379d64f5332f2006f97a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736245"
---
# <a name="idodownloadgetproperty-method"></a>IDODownload：： GetProperty 方法

抓取包含特定下載屬性之 **變數** 的指標。

## <a name="syntax"></a>語法

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>參數

`propId`

取得 **DODownloadProperty**) 類型 (所需的屬性識別碼。

`propVal`

產生的屬性值，儲存在 **變數** 中。

## <a name="return-value"></a>傳回值

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。

|傳回值|描述|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* 未知。|
|DO_E_WRITE_ONLY_PROPERTY|屬性為僅限寫入，無法讀取。|
|E_NOT_SET|未透過 **SetProperty** 設定此屬性。|

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10 版本 1809 \[僅限 Win32 應用程式\] |
| **最低支援的伺服器** | WindowsServer，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | Do。h |
