---
title: DO_DOWNLOAD_ENUM_CATEGORY 結構
description: 由 **IDOManager：： EnumDownloads** 用來依特定屬性的值篩選下載列舉。
keywords:
- DO_DOWNLOAD_ENUM_CATEGORY 結構
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_ENUM_CATEGORY
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a78c94cd9d8854453517976300e12a031f65b8cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "106966018"
---
# <a name="do_download_enum_category-structure"></a>DO_DOWNLOAD_ENUM_CATEGORY 結構

**IDOManager：： EnumDownloads** 會使用 **DO_DOWNLOAD_ENUM_CATEGORY** 結構，根據特定屬性的值篩選下載列舉。

## <a name="syntax"></a>語法
```cpp
typedef struct _DO_DOWNLOAD_ENUM_CATEGORY
{
  DODownloadProperty Property;
  LPCWSTR Value;
} DO_DOWNLOAD_ENUM_CATEGORY;
```

## <a name="members"></a>成員

`Property`

要用於下載列舉的屬性名稱。 這些屬性支援列舉用途。
- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

`Value`

屬性的值。

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | \[僅限 Windows 10 版本1809的 Win32 應用程式\] |
| **最低支援的伺服器** | Windows Server，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | Do。h |
