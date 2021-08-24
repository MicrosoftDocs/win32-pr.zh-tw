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
ms.openlocfilehash: dbc46ff05b6fa1846bb0e1ffc1fca928ca1d68ee38a43708c77a109b61a405da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751238"
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