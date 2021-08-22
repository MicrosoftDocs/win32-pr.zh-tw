---
title: DO_DOWNLOAD_RANGE_INFO 結構
description: 識別要從檔案下載的位元組範圍陣列。
keywords:
- DO_DOWNLOAD_RANGE_INFO 結構
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE_INFO
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 30df22c7232ad1d28315e8152396ddd92bdab9a7cbf67d748af134c0f0760c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543742"
---
# <a name="do_download_range_info-structure"></a>DO_DOWNLOAD_RANGE_INFO 結構

**DO_DOWNLOAD_RANGE_INFO** 結構會識別要從檔案下載的位元組範圍陣列。 它通常會以選擇性引數形式傳遞至 **IDODownload：： Start** 函式。

## <a name="syntax"></a>語法
```cpp
typedef struct _DO_DOWNLOAD_RANGES_INFO
{
  UINT RangeCount;
  [size_is(RangeCount)] DO_DOWNLOAD_RANGE Ranges[];
} DO_DOWNLOAD_RANGES_INFO;
```

## <a name="members"></a>成員

`RangeCount`

範圍中的元素數目。

`Ranges`

一或多個 **DO_DOWNLOAD_RANGE** 結構的陣列，指定要下載的範圍。

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10 版本 1809 \[僅限 Win32 應用程式\] |
| **最低支援的伺服器** | WindowsServer，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | Do。h |
