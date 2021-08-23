---
description: 在指定的來源檔案和指定的目標檔案之間建立差異。
title: CreatePatchFileExA/W 函數
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: CreatePatchFileExA, CreatePatchFileExW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePatchFileExW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 7d73b6f4d10c52e9eca147227fdbfece31cba157af84fdf56dbef5cacda516b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690868"
---
# <a name="createpatchfileexaw-function"></a>CreatePatchFileExA/W 函數

**CreatePatchFileExA** 和 **CreatePatchFileExW** 函數會在指定的來源檔案和指定的目標檔案之間建立差異。 來源和目標檔案都會以路徑形式提供。 輸出差異也會寫入至提供的路徑。 這些函數會在建立程式期間提供進度報告。

## <a name="syntax"></a>語法

```cpp
BOOL  PATCHAPI  CreatePatchFileExA(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCTSTR                   NewFileName,
    LPCTSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );

BOOL  PATCHAPI  CreatePatchFileExW(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCWSTR                   NewFileName,
    LPCWSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );
```

## <a name="parameters"></a>參數

*OldFileCount*

原始程式檔總數。 用來針對多個來源檔案建立差異， (最大的 255) 。

*OldFileInfoArray*

來源檔案資訊陣列的指標。

*NewFileName*

目標檔案的名稱。

*PatchFileName*

所建立之差異的名稱。

*OptionFlags*

建立旗標。

*ProgressCallback*

應用程式定義的進度回呼的指標。

*CallbackCoNtext*

應用程式定義內容的指標。

## <a name="return-value"></a>傳回值

如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|----------------|---------------------------------------------------------------------------------------|
| 標頭 | patchapi。h |
| DLL | mspatchc.dll |
| Unicode | 實作為 CreatePatchFileExW (Unicode) 和 CreatePatchFileExA (ANSI)  |

## <a name="see-also"></a>另請參閱

[PatchAPI](patchapi.md)
