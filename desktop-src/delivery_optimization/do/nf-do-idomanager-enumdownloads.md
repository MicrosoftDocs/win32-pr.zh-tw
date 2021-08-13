---
title: IDOManager：： EnumDownloads 方法
description: 抓取列舉值物件的介面指標，此列舉值物件是用來列舉現有的下載。
keywords:
- IDOManager：： EnumDownloads 方法
topic_type:
- apiref
api_name:
- IDOManager.EnumDownloads
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5442196b95e654755b4f84fe85375afb8f5b9372ddae453ca4ddffb567882fda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543825"
---
# <a name="idomanagerenumdownloads-method"></a>IDOManager：： EnumDownloads 方法

抓取列舉值物件的介面指標，此列舉值物件是用來列舉現有的下載。

## <a name="syntax"></a>語法

```cpp
HRESULT EnumDownloads(
  DO_DOWNLOAD_ENUM_CATEGORY *category, 
  IEnumUnknown **ppEnum
);
```

## <a name="parameters"></a>參數

`category`

選擇性。 要用來做為列舉類別的屬性名稱。 傳遞 `nullptr` 將會取得所有現有的下載。 以下是支援類別的屬性。

- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

`ppEnum`

**IEnumUnknown** 介面指標的位址，用來列舉現有的下載。 列舉值的內容取決於 *類別* 的值。 列舉介面中包含的下載專案是先前由相同呼叫端為此函式建立的下載專案。 

## <a name="return-value"></a>傳回值

如果函式成功，它會傳回 **S_OK**。 否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10 版本 1809 \[僅限 Win32 應用程式\] |
| **最低支援的伺服器** | WindowsServer，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | Do。h |
