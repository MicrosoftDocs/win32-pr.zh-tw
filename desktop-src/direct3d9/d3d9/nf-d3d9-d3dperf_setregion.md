---
title: D3DPERF_SetRegion 函式
description: 在 PIXRun 檔案中，以指定的色彩和名稱來標記一系列的框架。 PIX 目前不支援此函式。
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
- D3DPERF_SetRegion
targetos: Windows
ms.openlocfilehash: 650cc6063865da5ce30b97ed1468c1718ace5da6
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/08/2020
ms.locfileid: "106966443"
---
# <a name="d3dperf_setregion-function"></a>D3DPERF_SetRegion 函式

在 PIXRun 檔案中，以指定的色彩和名稱來標記一系列的框架。 PIX 目前不支援此函式。

## <a name="syntax"></a>語法

```cpp
void WINAPI D3DPERF_SetRegion(
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

為了讓分析變得更容易，目的程式可以使用色彩來標記目的程式的每個層級。

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **目標平台** | Windows |
| **標頭** | d3d9。h |
| **程式庫** | d3d9 .lib |
| **DLL** | d3d9.dll |