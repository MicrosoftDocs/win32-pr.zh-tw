---
title: 'CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING 結構 (D3dx12 .h) '
description: 用來包裝 [CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md) 結構的 helper 結構。 允許著色器使用單一繪製呼叫轉譯成多個視圖;適用于身歷聲視覺或立方體貼圖產生。
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING 結構
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/05/2021
ms.openlocfilehash: 6bf5d69232f9cf61e7b650df1f53229eabff4e0a0199ef5ec804e6d592855a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261765"
---
# <a name="cd3dx12_pipeline_state_stream_view_instancing-structure"></a>CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING 結構

用來包裝 [CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md) 結構的 helper 結構。 允許著色器使用單一繪製呼叫轉譯成多個視圖;適用于身歷聲視覺或立方體貼圖產生。

## <a name="syntax"></a>Syntax

```cpp
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_VIEW_INSTANCING_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VIEW_INSTANCING, CD3DX12_DEFAULT> CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING;
```

**CD3DX12_PIPELINE_STATE_STREAM_VIEW_INSTANCING** 是 `typedef` [CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT](cd3dx12-pipeline-state-stream-subobject.md) 範本的特製化。

## <a name="members"></a>成員

請參閱 [CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT](cd3dx12-pipeline-state-stream-subobject.md) 和 [CD3DX12_VIEW_INSTANCING_DESC](cd3dx12-view-instancing-desc.md)。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭 | [D3dx12。h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>另請參閱

* [Direct3D 12 的 Helper 結構](helper-structures-for-d3d12.md)
* [CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT](cd3dx12-pipeline-state-stream-subobject.md)
* [D3D12_PIPELINE_STATE_SUBOBJECT_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
* [D3DX12_VIEW_INSTANCING_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
