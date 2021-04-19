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
ms.openlocfilehash: 0f328565c80350a05cbfb23f178ea3580586f326
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "106968079"
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
| **最低支援的用戶端** | \[僅限 Windows 10 版本1809的 Win32 應用程式\] |
| **最低支援的伺服器** | Windows Server，僅限1809版的 \[ Win32 應用程式\] |
| **標頭** | DeliveryOptimizationDownloadTypes。h |
