---
title: 'UpdateSubresources 函式 (D3dx12) '
description: 更新子資源，所有 subresource 陣列都應該填入，通常是藉由呼叫 ID3D12Device GetCopyableFootprints。
ms.assetid: D6885165-095E-452D-8D93-A2C43A215F48
keywords:
- UpdateSubresources 函式
topic_type:
- apiref
api_name:
- UpdateSubresources
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1e48f4bc574d0b032b878c19c7749f63f86aba21a659c1c0a8f6f526f5bce5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496598"
---
# <a name="updatesubresources-function"></a>UpdateSubresources 函式

更新子資源，所有 subresource 陣列都應該填入，通常是藉由呼叫 [**ID3D12Device：： GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)。

## <a name="syntax"></a>語法


```C++
UINT64 inline UpdateSubresources(
  _In_       ID3D12GraphicsCommandList          *pCmdList,
  _In_       ID3D12Resource                     *pDestinationResource,
  _In_       ID3D12Resource                     *pIntermediate,
  _In_       UINT                               FirstSubresource,
  _In_       UINT                               NumSubresources,
             UINT64                             RequiredSize,
  _In_ const D3D12_PLACED_SUBRESOURCE_FOOTPRINT *pLayouts,
  _In_ const UINT                               *pNumRows,
  _In_ const UINT64                             *pRowSizesInBytes,
  _In_ const D3D12_SUBRESOURCE_DATA             *pSrcData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCmdList* \[在\]
</dt> <dd>

類型： **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

命令清單，做為 [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)的指標。

</dd> <dt>

*pDestinationResource* \[在\]
</dt> <dd>

類型： **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

目的地資源，作為 [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)的指標。

</dd> <dt>

*pIntermediate* \[在\]
</dt> <dd>

類型： **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

中繼資源，作為 [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)的指標。

</dd> <dt>

*FirstSubresource* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

資源中第一個 subresource 的索引。 有效值的範圍是0到 D3D12 的要求 \_ \_ 子資源。

</dd> <dt>

*NumSubresources* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

資源中的子資源數目。 有效值的範圍是0到 (D3D12 \_ 需求 \_ 子資源- *FirstSubresource*) 。

</dd> <dt>

*RequiredSize* 
</dt> <dd>

類型： **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

更新所需的大小（以位元組為單位）。

</dd> <dt>

*pLayouts* \[在\]
</dt> <dd>

型別： **Const [**D3D12 \_ 放置 SUBRESOURCE 的 \_ \_ 佔用量**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) \***

陣列的指標， (長度 *NumSubresources*) 指標指向結構的指標，其中包含資源子資源的描述和位置。

</dd> <dt>

*pNumRows* \[在\]
</dt> <dd>

類型： **Const [**UINT**](/windows/desktop/WinProg/windows-data-types) \***

陣列的指標 (長度為 *NumSubresources* 的 UINTS) ，其中包含每個 subresource 的資料列數目。

</dd> <dt>

*pRowSizesInBytes* \[在\]
</dt> <dd>

類型： **Const [**UINT64**](/windows/desktop/WinProg/windows-data-types) \***

陣列的指標 (長度為 *NumSubresources* 的 UINTS) ，其中包含每個資料列的大小（以位元組為單位）。

</dd> <dt>

*pSrcData* \[在\]
</dt> <dd>

Type： **Const [**D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***

陣列的指標 (長度 *NumSubresources*) 指標指向 [**D3D12 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) 結構的指標，其中包含用於更新的 SUBRESOURCE 資料描述。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

緩衝區的大小 (以位元組為單位)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx12。h</dt> </dl>  |
| 程式庫<br/> | <dl> <dt>D3D12 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3D12 的 Helper 函式](helper-functions-for-d3d12.md)
</dt> <dt>

[子資源](subresources.md)
</dt> </dl>

 

