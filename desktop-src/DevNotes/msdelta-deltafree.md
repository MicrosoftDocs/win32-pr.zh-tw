---
description: 釋出指定的記憶體區塊。
title: DeltaFree 函式
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: DeltaFree
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- DeltaFree
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 15885cfa3e879ed6a1e85b2f9553af92d436ca71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990239"
---
# <a name="deltafree-function"></a>DeltaFree 函式

釋出指定的記憶體區塊。 在成功呼叫 [CreateDeltaB](msdelta-createdeltab.md) 和 [ApplyDeltaB](msdelta-applydeltab.md) 之後，您必須呼叫此函式，以釋放 MSDelta 配置的記憶體緩衝區。

## <a name="syntax"></a>語法

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a>參數

*lpMemory*

在要釋放的記憶體區塊。

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

[CreateDeltaB](msdelta-createdeltab.md)

[ApplyDeltaB](msdelta-applydeltab.md)
