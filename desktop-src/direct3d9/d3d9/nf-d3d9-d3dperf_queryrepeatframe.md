---
title: D3DPERF_QueryRepeatFrame 函式
description: 判斷效能分析工具是否要求將目前的框架重新提交給 Direct3D 以進行效能分析。 PIX 目前不支援此函式。
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
- D3DPERF_QueryRepeatFrame
targetos: Windows
ms.openlocfilehash: c4054a0704fd0258483ee0d3d3d555cb5eabe7f9
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/08/2020
ms.locfileid: "103681503"
---
# <a name="d3dperf_queryrepeatframe-function"></a>D3DPERF_QueryRepeatFrame 函式

判斷效能分析工具是否要求將目前的框架重新提交給 Direct3D 以進行效能分析。 PIX 目前不支援此函式。

## <a name="syntax"></a>語法

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a>傳回值

如果傳回值為 TRUE，則呼叫端應該重複相同的呼叫順序。 如果為 FALSE，則呼叫端應該繼續。

## <a name="remarks"></a>備註

函式應該在 IDirect3DDevice9 之後立即呼叫：會呼叫 **:P** 重新傳送。

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **目標平台** | Windows |
| **標頭** | d3d9。h |
| **程式庫** | d3d9 .lib |
| **DLL** | d3d9.dll |