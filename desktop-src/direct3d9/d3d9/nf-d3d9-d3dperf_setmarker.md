---
title: D3DPERF_SetMarker 函式
description: 標示瞬間事件。 PIX 可以使用此事件來觸發動作。
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
- D3DPERF_SetMarker
targetos: Windows
ms.openlocfilehash: 8eef59b9914ce30b95751641c16becf1963b19e0
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/08/2020
ms.locfileid: "104374706"
---
# <a name="d3dperf_setmarker-function"></a>D3DPERF_SetMarker 函式

標示瞬間事件。 PIX 可以使用此事件來觸發動作。

## <a name="syntax"></a>語法

```cpp
void WINAPI D3DPERF_SetMarker(
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

此函數不會傳回值。

## <a name="remarks"></a>備註

瞬間的使用者事件不會將其他事件括住或群組。 例如，當使用者在遊戲中引發武器時， **D3DPERF_SetMarker** 的呼叫可能會建立 *引發引發* 的事件。 若要將多個事件以單一、使用者定義的名稱群組在一起，請使用 **D3DPERF_BeginEvent** 和 **D3DPERF_EndEvent** ，而不是 **D3DPERF_SetMarker**。

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **目標平台** | Windows |
| **標頭** | d3d9。h |
| **程式庫** | d3d9 .lib |
| **DLL** | d3d9.dll |