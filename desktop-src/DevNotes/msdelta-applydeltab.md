---
description: 使用以緩衝區形式提供的差異和來源 (，) 建立目標資料的新複本。 輸出資料會在 MSDelta 配置的緩衝區中傳回。
title: ApplyDeltaB 函式
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: ApplyDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplyDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 368788ba894064aa8ac3f8c9711f987a32f306af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000920"
---
# <a name="applydeltab-function"></a>ApplyDeltaB 函式

使用以緩衝區形式提供的差異和來源 (，) 建立目標資料的新複本。 輸出資料會在 MSDelta 配置的緩衝區中傳回。

> [!NOTE]
> 完成此函式之後，您必須呼叫 [DeltaFree](msdelta-deltafree.md) 來釋放輸出緩衝區。

> [!NOTE]
> 如果指定的 delta 是使用 [PatchAPI](patchapi.md)所建立，且已設定 [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) 旗標，則 MSDelta 會呼叫 PatchAPI 以套用差異。

## <a name="syntax"></a>語法

```cpp
BOOL  WINAPI  ApplyDeltaB(
    DELTA_FLAG_TYPE  ApplyFlags,
    DELTA_INPUT      Source,
    DELTA_INPUT      Delta,
    LPDELTA_OUTPUT   lpTarget
   );
```

## <a name="parameters"></a>參數

*ApplyFlags*

在請 [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) 或 [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags)。

*來源*

在 [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) 結構，包含包含來源資料之緩衝區的指標。

*差異*

在包含差異資料之緩衝區指標的 [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) 結構。

*lpTarget*

擴展要寫入目標的 [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) 結構指標。

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
