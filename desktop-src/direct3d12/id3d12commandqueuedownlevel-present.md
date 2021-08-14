---
title: ID3D12CommandQueueDownlevel：:P 重發方法
description: 將內容從 Direct3D 12 Texture2D 資源複製到視窗。 |ID3D12CommandQueueDownlevel：:P 重發方法
keywords:
- 現在時方法
- 目前的方法，ID3D12CommandQueueDownlevel 介面
- ID3D12CommandQueueDownlevel 介面，存在方法
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel.Present
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: b21a97d15d2666dcfe0a304f2393d6d14c5dbcc4142d8b42f43f295d8751614b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118529128"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a>ID3D12CommandQueueDownlevel：:P 重發方法

將內容從 Direct3D 12 Texture2D 資源複製到視窗。

## <a name="syntax"></a>語法

```cpp
HRESULT Present
    ID3D12GraphicsCommandList *pOpenCommandList,
    ID3D12Resource *pSourceTex2D,
    HWND hWindow,
    D3D12_DOWNLEVEL_PRESENT_FLAGS Flags
);
```

## <a name="parameters"></a>參數

`pOpenCommandList`

類型： **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

開啟的命令清單，Direct3D 12 會將目前的命令，然後為您關閉並提交。

`pSourceTex2D`

類型： **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***

包含要顯示之所需內容的資源，包含維度 [**D3D12 \_ 資源 \_ 維度 \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)，以及下列其中一種格式。

* DXGI_FORMAT_R16G16B16A16_FLOAT
* DXGI_FORMAT_R10G10B10A2_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM_SRGB
* DXGI_FORMAT_B8G8R8X8_UNORM
* DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM_SRGB

`hWindow`

類型： **[HWND](/windows/desktop/WinProg/windows-data-types)**

應顯示內容的視窗控制碼。

`Flags`

類型： **[D3D12 \_ 下層 \_ 目前的 \_ 旗標](d3d12_downlevel_present_flags.md)**

用以修改 **目前** 作業的旗標。

## <a name="return-value"></a>傳回值

會在成功時傳回 **S_OK** ，否則會傳回失敗的 HRESULT。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------|------------------|
| 標頭 | d3d12downlevel。h |
| DLL    | D3D12.dll 只 (Windows 7)  |

## <a name="see-also"></a>另請參閱
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Windows 7 介面上的 Direct3D 12](direct3d-12on7-interfaces.md)
* [Windows 7 參考上的 Direct3D 12 (d3d12downlevel .h) ](direct3d-12on7-reference.md)
* [Windows 7 上的 Direct3D 12](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
