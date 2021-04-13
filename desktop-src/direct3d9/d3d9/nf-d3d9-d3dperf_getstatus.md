---
title: D3DPERF_GetStatus 函式
description: 從目的程式判斷 profiler 的目前狀態。
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
- D3DPERF_GetStatus
targetos: Windows
ms.openlocfilehash: 626d56dd449b0a0aa92e85c82dabda119900680d
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/08/2020
ms.locfileid: "104314466"
---
# <a name="d3dperf_getstatus-function"></a>D3DPERF_GetStatus 函式

從目的程式判斷 profiler 的目前狀態。

## <a name="syntax"></a>語法

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a>傳回值

當 PIX 正在分析目的程式時，非零值;否則為零。

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **目標平台** | Windows |
| **標頭** | d3d9。h |
| **程式庫** | d3d9 .lib |
| **DLL** | d3d9.dll |