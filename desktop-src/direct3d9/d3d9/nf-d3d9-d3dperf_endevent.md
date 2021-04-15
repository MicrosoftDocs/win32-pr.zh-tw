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
ms.openlocfilehash: 91c2a6a19b926cd9f5549fae084ce8973432b0f2
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/08/2020
ms.locfileid: "104374707"
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