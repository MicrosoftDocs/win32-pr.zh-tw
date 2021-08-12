---
title: IDODownload：： SetProperty 方法
description: 設定下載屬性。
keywords:
- IDODownload：： SetProperty 方法
topic_type:
- apiref
api_name:
- IDODownload.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a7d966edb083107b80f0723bce195bfc588797efb8ad1931e0e75a468bec5a3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543897"
---
# <a name="idodownloadsetproperty-method"></a>IDODownload：： SetProperty 方法

設定下載屬性。 方法會接受 VARIANT 的指標，該 **變數** 包含要套用至下載的特定屬性。

## <a name="syntax"></a>語法

```cpp
HRESULT SetProperty(
  DODownloadProperty propId,
  VARIANT* propVal
);
```

## <a name="parameters"></a>參數

`propId`

要設定 **DODownloadProperty**) 類型 (所需的屬性識別碼。

`propVal`

要設定的屬性值，儲存在 **變數** 中。

## <a name="return-value"></a>傳回值

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。

|傳回值|描述|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* 未知。|
|DO_E_INVALID_STATE|下載目前不是允許設定屬性的狀態。|

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10 版本 1809 \[僅限 Win32 應用程式\] |
| **最低支援的伺服器** | WindowsServer，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | Do。h |
