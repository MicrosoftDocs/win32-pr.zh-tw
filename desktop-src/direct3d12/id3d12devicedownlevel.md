---
title: ID3D12DeviceDownlevel 介面
description: 提供 Windows 7 特定的記憶體統計資料查詢。
keywords:
- ID3D12DeviceDownlevel 介面
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 401cbd0045211ef51e3ef6b06042262964ae2ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998996"
---
# <a name="id3d12devicedownlevel-interface"></a>ID3D12DeviceDownlevel 介面

在 [Windows 7 上使用 direct3d](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)12 裝置時，可以透過 **QueryInterface** 從 [direct3d 12 裝置](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)存取這個介面。 它會提供 Windows 7 特定的記憶體統計資料查詢。

### <a name="methods"></a>方法

**ID3D12DeviceDownlevel** 介面具有這些方法。

| 方法 | 描述 |
|:-------|:------------|
| [**QueryVideoMemoryInfo**](id3d12devicedownlevel-queryvideomemoryinfo.md) | 提供 Windows 7 的記憶體統計資料。 |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------|------------------|
| 標頭 | d3d12downlevel。h |
| DLL    | D3D12.dll 只 (Windows 7)  |

## <a name="see-also"></a>另請參閱
* [Windows 7 上的 Direct3D 12 介面](direct3d-12on7-interfaces.md)
* [Windows 7 上的 Direct3D 12 參考 (d3d12downlevel .h) ](direct3d-12on7-reference.md)
* [Windows 7 上的 Direct3D 12](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
