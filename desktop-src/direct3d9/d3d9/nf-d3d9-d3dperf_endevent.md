---
title: D3DPERF_EndEvent 函式
description: 標記使用者定義事件的結尾。 PIX 可以使用此事件來觸發動作。
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_EndEvent
targetos: Windows
ms.openlocfilehash: bd12780dfdfcb86e83495ae877d8debf1e768517826329ccee8d40ffaa88fbbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989248"
---
# <a name="d3dperf_endevent-function"></a>D3DPERF_EndEvent 函式

標記使用者定義事件的結尾。 PIX 可以使用此事件來觸發動作。

## <a name="syntax"></a>語法

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a>傳回值

事件結束之階層的層級。 如果發生錯誤，此值為負數。

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **目標平台** | Windows |
| **標頭** | d3d9。h |
| **程式庫** | d3d9 .lib |
| **DLL** | d3d9.dll |