---
description: 在以緩衝區形式提供的來源和目標 (之間建立差異) 並傳回輸出 delta 作為 MSDelta 配置的緩衝區。
title: CreateDeltaB 函式
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: CreateDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: a2142f26499514c24967e5334d782c2dee559cd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977403"
---
# <a name="createdeltab-function"></a>CreateDeltaB 函式

在以緩衝區形式提供的來源和目標 (之間建立差異) 並傳回輸出 delta 作為 MSDelta 配置的緩衝區。

> [!NOTE]
> 完成此函式之後，您必須呼叫 [DeltaFree](msdelta-deltafree.md) 來釋放輸出緩衝區。

## <a name="syntax"></a>語法

```cpp
BOOL  WINAPI  CreateDeltaB(
           DELTA_FILE_TYPE  FileTypeSet,
           DELTA_FLAG_TYPE  SetFlags,
           DELTA_FLAG_TYPE  ResetFlags,
           DELTA_INPUT      Source,
           DELTA_INPUT      Target,
           DELTA_INPUT      SourceOptions,
           DELTA_INPUT      TargetOptions,
           DELTA_INPUT      GlobalOptions,
    const  FILETIME        *lpTargetFileTime,
           ALG_ID           HashAlgId,
           LPDELTA_OUTPUT   lpDelta
    );
```

## <a name="parameters"></a>參數

*FileTypeSet*

在 [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) 值，表示要用於建立進程的檔案類型集。

*SetFlags*

在一或多個 [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) 值，這個值會指定要在建立進程期間使用的旗標，以及預設旗標。

*ResetFlags*

在一或多個 [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) 值，這個值會指定要在建立進程期間重設的預設旗標。

*來源*

在 [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) 結構，包含包含來源資料之緩衝區的指標。

*Target*

在包含目標資料之緩衝區指標的 [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) 結構。

*SourceOptions*

[in] 保留。 傳遞 [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) 結構，並將 *可編輯* 的設定為 **FALSE**、 *LpStart* 設定為 **Null** ，並將 *uSize* 設定為0。

*TargetOptions*

[in] 保留。 傳遞 [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) 結構，並將 *可編輯* 的設定為 **FALSE**、 *LpStart* 設定為 **Null** ，並將 *uSize* 設定為0。

*GlobalOptions*

[in] 保留。 傳遞 [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) 結構，並將 *LpStart* 設定為 **Null** ，並將 *uSize* 設定為0。

*lpTargetFileTime*

在套用 delta 之後，于目標檔案上設定的時間戳記。 如果是 **Null**，則目標時間戳記將會是建立進程期間的目前時間。

*HashAlgId*

在用來產生目標特徵標記的演算法 ALG_ID。 某些特殊值為：

- 0 = 沒有簽章
- 32 = msdelta.dll 中定義的32位 CRC

*lpDelta*

擴展要寫入差異的 [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) 結構的指標。

## <a name="return-value"></a>傳回值

如果成功，則此函式會傳回 **TRUE** ;否則，它會傳回 **FALSE**。 當函數傳回 **FALSE** 時，您可以呼叫 [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 來取得對應的 Win32 系統錯誤碼。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|----------------|---------------------------------------------------------------------------------------|
| 標頭 | msdelta。h |
| DLL | msdelta.dll |
| Unicode | 不適用 |

## <a name="see-also"></a>另請參閱

[MSDelta](msdelta.md)

[DeltaFree](msdelta-deltafree.md)
