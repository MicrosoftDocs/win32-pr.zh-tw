---
description: 從差異解壓縮標頭資訊。
title: ExtractPatchHeaderToFileA/W 函數
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: ExtractPatchHeaderToFileA, ExtractPatchHeaderToFileW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtractPatchHeaderToFileW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 626bd53e3361f4d29cc76e17ae2788ddea3bc8b99b580196bcbf77c27a6983d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571798"
---
# <a name="extractpatchheadertofileaw-function"></a>ExtractPatchHeaderToFileA/W 函數

**ExtractPatchHeaderToFileA** 和 **ExtractPatchHeaderToFileW** 函式會從差異中解壓縮標頭資訊。 差異會以檔案路徑的形式提供。 輸出標頭也會寫入至提供的路徑。

## <a name="syntax"></a>語法

```cpp
BOOL  PATCHAPI  ExtractPatchHeaderToFileA(
    LPCTSTR  PatchFileName,
    LPCTSTR  PatchHeaderFileName
    );

BOOL  PATCHAPI  ExtractPatchHeaderToFileW(
    LPCWSTR  PatchFileName,
    LPCWSTR  PatchHeaderFileName
    );
```

## <a name="parameters"></a>參數

*PatchFileName*

包含標頭之差異的名稱。

*PatchHeaderFileName*

要建立的標頭檔名稱。

## <a name="return-value"></a>傳回值

如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|----------------|---------------------------------------------------------------------------------------|
| 標頭 | patchapi。h |
| DLL | mspatchc.dll |
| Unicode | 實作為 ExtractPatchHeaderToFileW (Unicode) 和 ExtractPatchHeaderToFileA (ANSI)  |

## <a name="see-also"></a>另請參閱

[PatchAPI](patchapi.md)
