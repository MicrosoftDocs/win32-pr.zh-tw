---
title: ID3D12DeviceDownlevel：： QueryVideoMemoryInfo 方法
description: 將內容從 Direct3D 12 Texture2D 資源複製到視窗。 |ID3D12DeviceDownlevel：： QueryVideoMemoryInfo 方法
keywords:
- QueryVideoMemoryInfo 方法
- QueryVideoMemoryInfo 方法，ID3D12DeviceDownlevel 介面
- ID3D12DeviceDownlevel 介面，QueryVideoMemoryInfo 方法
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel.QueryVideoMemoryInfo
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 526d25e8331fc949eb470c0813a083774afddc94312ed6751aaab9672e557d3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124106"
---
# <a name="id3d12devicedownlevelqueryvideomemoryinfo-method"></a>ID3D12DeviceDownlevel：： QueryVideoMemoryInfo 方法

提供 Windows 7 的記憶體統計資料。 這個方法相當於 Windows 7 上未提供的[IDXGIAdapter3：： QueryVideoMemoryInfo](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo)。

## <a name="syntax"></a>語法

```cpp
HRESULT QueryVideoMemoryInfo( 
    UINT NodeIndex,
    DXGI_MEMORY_SEGMENT_GROUP MemorySegmentGroup,
    DXGI_QUERY_VIDEO_MEMORY_INFO *pVideoMemoryInfo
);
```

## <a name="parameters"></a>參數

`NodeIndex`

類型： **UINT**

指定要查詢其影片記憶體資訊的裝置實體介面卡。 若為單一 GPU 作業，請將此值設定為零。 如果有多個 GPU 節點，請將此設定為節點的索引， (裝置的實體介面卡) 來查詢影片的記憶體資訊。 請參閱 [多介面卡系統](multi-engine.md)。

`MemorySegmentGroup`

類型： **[DXGI_MEMORY_SEGMENT_GROUP](/windows/win32/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)**

指定將群組識別為本機或非本機的 **DXGI_MEMORY_SEGMENT_GROUP** 。

`pVideoMemoryInfo`

類型： **[DXGI_QUERY_VIDEO_MEMORY_INFO](/windows/win32/api/dxgi1_4/ns-dxgi1_4-dxgi_query_video_memory_info)\***

以目前的值填滿 **DXGI_QUERY_VIDEO_MEMORY_INFO** 結構。

## <a name="return-value"></a>傳回值

會在成功時傳回 **S_OK** ，否則會傳回失敗的 HRESULT。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------|------------------|
| 標頭 | d3d12downlevel .h 和 dxgi1_4。h |
| DLL    | D3D12.dll 只 (Windows 7)  |

## <a name="see-also"></a>另請參閱
* [ID3D12DeviceDownlevel](id3d12devicedownlevel.md)
* [Windows 7 介面上的 Direct3D 12](direct3d-12on7-interfaces.md)
* [Windows 7 參考上的 Direct3D 12 (d3d12downlevel .h) ](direct3d-12on7-reference.md)
* [Windows 7 上的 Direct3D 12](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
