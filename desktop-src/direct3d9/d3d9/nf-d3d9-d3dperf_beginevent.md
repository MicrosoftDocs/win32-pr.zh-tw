---
title: D3DPERF_BeginEvent 函式
description: 標記使用者定義事件的開頭。 PIX 可以使用此事件來觸發動作。
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
- D3DPERF_BeginEvent
targetos: Windows
ms.openlocfilehash: 3958d1a9227b39dc65d702d91d0bb389b1c81ad333fd5b8def468be8fd342f7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096930"
---
# <a name="d3dperf_beginevent-function"></a>D3DPERF_BeginEvent 函式

標記使用者定義事件的開頭。 PIX 可以使用此事件來觸發動作。

## <a name="syntax"></a>語法

```cpp
int WINAPI D3DPERF_BeginEvent(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a>參數

`col`

事件色彩。 這是在事件檢視器中顯示事件的色彩。

`wszName`

事件名稱。

## <a name="return-value"></a>傳回值

此事件開始的階層之以零為基底的層級。 如果發生錯誤，傳回值將會是負數。

## <a name="remarks"></a>備註

使用者自訂事件會以對目的程式有意義的方式，將其他事件群組在一起，使其在效能分析工具中更能呈現。 例如， *Draw 太空船* 事件可能會括住一些處理遊戲中繪製太空船的 Direct3D 呼叫。 事件可以進行嵌套。

每個 **D3DPERF_BeginEvent** 呼叫都應該有相符的 **D3DPERF_EndEvent** 呼叫。  (不會將其他事件放在) 的即時事件，應該使用 **D3DPERF_SetMarker** 來標記，而不是 **D3DPERF_BeginEvent** 和 **D3DPERF_EndEvent**。

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **目標平台** | Windows |
| **標頭** | d3d9。h |
| **程式庫** | d3d9 .lib |
| **DLL** | d3d9.dll |