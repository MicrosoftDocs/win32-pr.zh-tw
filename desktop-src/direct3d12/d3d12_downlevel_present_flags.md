---
title: D3D12_DOWNLEVEL_PRESENT_FLAGS 列舉
description: 傳遞至 ID3D12CommandQueueDownlevel 的旗標：:P 重發的方法。
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
topic_type:
- APIRef
api_name:
- D3D12_DOWNLEVEL_PRESENT_FLAGS
api_type:
- HeaderDef
ms.openlocfilehash: 1ce1536945748bae09fc7a0981c14c076fc6394e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993858"
---
# <a name="d3d12_downlevel_present_flags-enumeration"></a>D3D12 \_ 下層 \_ 目前的 \_ 旗標列舉

傳遞至 ID3D12CommandQueueDownlevel 的旗標 [**：:P**](id3d12commandqueuedownlevel-present.md) 重新傳送的函式來修改行為。

## <a name="syntax"></a>Syntax

```cpp
enum D3D12_DOWNLEVEL_PRESENT_FLAGS
{
    D3D12_DOWNLEVEL_PRESENT_FLAG_NONE = 0,
    D3D12_DOWNLEVEL_PRESENT_FLAG_WAIT_FOR_VBLANK = 1
};
```

## <a name="constants"></a>常數

**D3D12 \_ 下層 \_ 目前 \_ 旗標 \_ 無**

未選取任何選項。

**D3D12 \_ 下層 \_ 目前 \_ 旗 \_ 標 \_ 等候 \_ VBLANK**

**目前** 的作業將不會執行，直到您上次 **顯示** ed 之後發生 VSync 為止。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------|------------------|
| 標頭 | d3d12downlevel。h |
| DLL    | D3D12.dll 只 (Windows 7)  |

## <a name="see-also"></a>另請參閱
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Windows 7 上的 Direct3D 12 列舉](direct3d-12on7-enumerations.md)
* [Windows 7 上的 Direct3D 12 參考 (d3d12downlevel .h) ](direct3d-12on7-reference.md)
* [Windows 7 上的 Direct3D 12](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
