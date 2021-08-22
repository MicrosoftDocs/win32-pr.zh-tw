---
title: 'CD3DX12_DESCRIPTOR_RANGE 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 描述項 \_ 範圍結構。
ms.assetid: F066ECA5-5E52-4483-B773-B43C5F12809B
keywords:
- CD3DX12_DESCRIPTOR_RANGE 結構
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 641afe973c89d66257a8fc7b46defe2e77d8a8667094448ef58ab4beb2839b8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989938"
---
# <a name="cd3dx12_descriptor_range-structure"></a>CD3DX12 \_ 描述項 \_ 範圍結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_DESCRIPTOR_RANGE  : public D3D12_DESCRIPTOR_RANGE{
       CD3DX12_DESCRIPTOR_RANGE();
       explicit CD3DX12_DESCRIPTOR_RANGE(const D3D12_DESCRIPTOR_RANGE &o);
       CD3DX12_DESCRIPTOR_RANGE(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 描述項 \_ 範圍 ()**
</dt> <dd>

建立新的、未初始化的 D3DX12 描述項 \_ \_ 範圍實例。

</dd> <dt>

**明確的 CD3DX12 \_ 描述項 \_ 範圍 (const D3D12 \_ 描述項 \_ 範圍 &o)**
</dt> <dd>

建立 D3DX12 描述元範圍的新 \_ 實例 \_ ，並以另一個 [**D3D12 \_ 描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ 描述項 \_ 範圍 (D3D12 \_ 描述項 \_ 範圍 \_ 類型 RANGETYPE、uint NUMDESCRIPTORS、UINT baseShaderRegister、UINT RegisterSpace = 0、UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加)**
</dt> <dd>

建立 D3DX12 描述項範圍的新 \_ 實例 \_ ，並初始化下列參數：

[**D3D12 \_描述項 \_ 範圍 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加

</dd> <dt>

**內嵌 Init (D3D12 \_ 描述項 \_ 範圍 \_ 類型 RangeType、UINT NumDescriptors、UINT BaseShaderRegister、UINT registerSpace = 0、UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_描述項 \_ 範圍 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加

</dd> <dt>

**靜態內嵌 Init (D3D12 \_ 描述元 \_ 範圍 &範圍、D3D12 \_ 描述項 \_ 範圍 \_ 類型 RANGETYPE、UINT NUMDESCRIPTORS、UINT baseShaderRegister、UINT RegisterSpace = 0、uint offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) &範圍

[**D3D12 \_描述項 \_ 範圍 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 描述元 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





