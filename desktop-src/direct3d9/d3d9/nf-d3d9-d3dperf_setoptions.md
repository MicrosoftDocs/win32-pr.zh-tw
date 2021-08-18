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
ms.openlocfilehash: 579c07d8f93696e4e3c83b1e61c1ff5fca65e12b5a7cf0a5937a254ecc6dc306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805733"
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