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
ms.openlocfilehash: 78ff9eda9ab224faf4b2a117f6230e3361664bbfea35d8b2a8484ba7f5ab764a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805743"
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