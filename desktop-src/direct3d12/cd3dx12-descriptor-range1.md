---
title: 'CD3DX12_DESCRIPTOR_RANGE1 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 描述項 \_ RANGE1 結構。
ms.assetid: 9D073158-5907-4D1C-8D75-72B304277DAD
keywords:
- CD3DX12_DESCRIPTOR_RANGE1 結構
topic_type:
- apiref
api_name:
- CD3DX12_DESCRIPTOR_RANGE1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 404cb41a019dac404bbe351f78f1d1e65277dd9ad2aecf2cc2d94d06fe242f6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989878"
---
# <a name="cd3dx12_descriptor_range1-structure"></a>CD3DX12 \_ 描述項 \_ RANGE1 結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 描述項 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_DESCRIPTOR_RANGE1  : public D3D12_DESCRIPTOR_RANGE1{
       CD3DX12_DESCRIPTOR_RANGE1();
       explicit CD3DX12_DESCRIPTOR_RANGE1(const D3D12_DESCRIPTOR_RANGE1 &o);
       CD3DX12_DESCRIPTOR_RANGE1(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void inline Init(D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
  void static inline Init(D3D12_DESCRIPTOR_RANGE1 &range, D3D12_DESCRIPTOR_RANGE_TYPE rangeType, UINT numDescriptors, UINT baseShaderRegister, UINT registerSpace = 0, D3D12_DESCRIPTOR_RANGE_FLAGS flags = D3D12_DESCRIPTOR_RANGE_FLAG_NONE, UINT offsetInDescriptorsFromTableStart = D3D12_DESCRIPTOR_RANGE_OFFSET_APPEND);
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 \_ 描述項 \_ RANGE1 ()**
</dt> <dd>

建立新的、未初始化的 CD3DX12 描述項 \_ \_ RANGE1 實例。

</dd> <dt>

**明確的 CD3DX12 \_ 描述項 \_ range1 (const D3D12 \_ 描述項 \_ range1 &o)**
</dt> <dd>

建立 CD3DX12 描述項 range1 的新 \_ 實例 \_ ，並以另一個 [**D3D12 \_ 描述項 \_ range1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 \_ 描述項 \_ RANGE1 (D3D12 \_ 描述項 \_ 範圍 \_ 類型 RANGETYPE、uint NUMDESCRIPTORS、UINT baseShaderRegister、UINT registerSpace = 0、D3D12 \_ 描述元 \_ 範圍 \_ 旗標 = D3D12 \_ 描述項 \_ 範圍旗標 \_ \_ 無、UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加)**
</dt> <dd>

建立 CD3DX12 描述項 RANGE1 的新 \_ 實例 \_ ，並初始化下列參數：

[**D3D12 \_描述項 \_ 範圍 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

[**D3D12 \_描述項 \_ 範圍 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) 標旗標 = D3D12 \_ 描述項 \_ 範圍旗標 \_ \_ 無

UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加

</dd> <dt>

**內嵌 Init (D3D12 \_ 描述項 \_ 範圍 \_ 類型 RangeType、UINT NumDescriptors、UINT BaseShaderRegister、uint registerSpace = 0、D3D12 \_ 描述元 \_ 範圍 \_ 旗標 = D3D12 描述項範圍旗標 \_ \_ \_ \_ 無、UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_描述項 \_ 範圍 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

[**D3D12 \_描述項 \_ 範圍 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) 標旗標 = D3D12 \_ 描述項 \_ 範圍旗標 \_ \_ 無

UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加

</dd> <dt>

**靜態內嵌 Init (D3D12 \_ 描述項 \_ RANGE1 &範圍、D3D12 \_ 描述項 \_ 範圍 \_ 類型 RANGETYPE、UINT NUMDESCRIPTORS、uint baseShaderRegister、UINT registerSpace = 0、D3D12 \_ 描述項 \_ 範圍 \_ 旗標旗標 = D3D12 描述項範圍 \_ 旗標 \_ \_ \_ 無、uint offsetInDescriptorsFromTableStart = \_ \_ \_ \_ D3D12 描述項範圍位移附加)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_描述項 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) &範圍

[**D3D12 \_描述項 \_ 範圍 \_ 類型**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) rangeType

UINT numDescriptors

UINT baseShaderRegister

UINT registerSpace = 0

[**D3D12 \_描述項 \_ 範圍 \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) 標旗標 = D3D12 \_ 描述項 \_ 範圍旗標 \_ \_ 無

UINT offsetInDescriptorsFromTableStart = D3D12 \_ 描述項 \_ 範圍 \_ 位移 \_ 附加

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 \_ 描述項 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





