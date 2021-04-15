---
title: D3DPERF_SetOptions 函式
description: 設定目的程式所指定的 profiler 選項。
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
- D3DPERF_SetOptions
targetos: Windows
ms.openlocfilehash: 8bd877469864ccdaa833ce80d00eb06ae5fc18de
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/08/2020
ms.locfileid: "104462753"
---
# <a name="d3dperf_setoptions-function"></a>D3DPERF_SetOptions 函式

設定目的程式所指定的 profiler 選項。

## <a name="syntax"></a>語法

```cpp
int WINAPI D3DPERF_SetOptions(
  DWORD dwOptions
);
```

## <a name="parameters"></a>參數

`dwOptions`

PIX 可辨識的使用者選項。 將此設定為1，以通知 PIX 目的程式未提供要分析的許可權。

## <a name="return-value"></a>傳回值

此函數不會傳回值。

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **目標平台** | Windows |
| **標頭** | d3d9。h |
| **程式庫** | d3d9 .lib |
| **DLL** | d3d9.dll |