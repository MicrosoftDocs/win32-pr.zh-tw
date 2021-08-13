---
title: DO_DOWNLOAD_RANGE 結構
description: 識別要從檔案下載的單一位元組範圍。
keywords:
- DO_DOWNLOAD_RANGE 結構
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 39672bff2e3a7194f7d674b2184d5de8c9c3c601e4a7777ef31ace80f5f9f327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047116"
---
# <a name="do_download_range-structure"></a>DO_DOWNLOAD_RANGE 結構

**DO_DOWNLOAD_RANGE** 結構會識別要從檔案下載的單一位元組範圍。 **DO_DOWNLOAD_RANGE** 結構包含在 **DO_DOWNLOAD_RANGES_INFO** 結構內，以提供要下載的範圍陣列。

## <a name="syntax"></a>語法
```cpp
typedef struct _DO_DOWNLOAD_RANGE
{
  UINT64 Offset;
  UINT64 Length;
} DO_DOWNLOAD_RANGE;
```

## <a name="members"></a>成員

`Offset`

從檔案下載的位元組範圍開頭以零為基底的位移。

`Length`

範圍的長度（以位元組為單位）。 請勿指定零位元組長度。 若要指出範圍延伸至檔案結尾，請指定 **DO_LENGTH_TO_EOF**。

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10 版本 1809 \[僅限 Win32 應用程式\] |
| **最低支援的伺服器** | WindowsServer，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | DeliveryOptimizationDownloadTypes。h |
