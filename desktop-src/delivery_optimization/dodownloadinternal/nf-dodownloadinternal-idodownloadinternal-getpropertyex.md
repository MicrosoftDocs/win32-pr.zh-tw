---
title: IDODownloadInternal：： GetPropertyEx 方法
description: 抓取包含特定延伸下載屬性值之 **變數** 的指標。
keywords:
- IDODownloadInternal：： GetPropertyEx 方法
topic_type:
- apiref
api_name:
- IDODownloadInternal.GetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 908f9b15df5c0c4a2769149419ff12d545201e5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375836"
---
# <a name="idodownloadinternalgetpropertyex-method"></a>IDODownloadInternal：： GetPropertyEx 方法

> [!IMPORTANT]
> **IDODownloadInternal** 介面已被取代。 請改用 [IDODownload](../do/nn-do-idodownload.md) 介面。

抓取包含特定延伸下載屬性值之 **變數** 的指標。

## <a name="syntax"></a>語法

```cpp
HRESULT GetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a>參數

`propId`

取得 **DODownloadPropertyEx**) 類型 (所需的屬性識別碼。

`propVal`

產生的屬性值，儲存在 **變數** 中。

## <a name="return-value"></a>傳回值

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。

|傳回值|描述|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* 未知。|
|DO_E_WRITE_ONLY_PROPERTY|屬性為僅限寫入，無法讀取。|
|E_NOT_SET|未透過 **SetPropertyEx** 設定此屬性。|

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | \[僅限 Windows 10 版本1809的 Win32 應用程式\] |
| **最低支援的伺服器** | Windows Server，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | DODownloadInternal。h |