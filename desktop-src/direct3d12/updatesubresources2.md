---
title: 'UpdateSubresources (堆積-配置) 函數 (D3dx12 .h) '
description: 以堆積配置的執行更新子資源。
ms.assetid: 328D8755-D328-471D-AAF4-9771CBFF7539
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
ms.openlocfilehash: bc4e476501c91c3e7508c0aefdc1d9d6c99a057840b5a126879c8b4ff3608f68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460749"
---
# <a name="updatesubresources-heap-allocating-function"></a>UpdateSubresources (堆積配置) 函數

以堆積配置的執行更新子資源。

## <a name="syntax"></a>語法


```C++
UINT64 inline UpdateSubresources(
  _In_ ID3D12GraphicsCommandList *pCmdList,
  _In_ ID3D12Resource            *pDestinationResource,
  _In_ ID3D12Resource            *pIntermediate,
       UINT64                    IntermediateOffset,
  _In_ UINT                      FirstSubresource,
  _In_ UINT                      NumSubresources,
  _In_ D3D12_SUBRESOURCE_DATA    *pSrcData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCmdList* \[在\]
</dt> <dd>

類型： **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

命令清單的 [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) 介面指標。

</dd> <dt>

*pDestinationResource* \[在\]
</dt> <dd>

類型： **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

代表目的地資源之 [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) 介面的指標。

</dd> <dt>

*pIntermediate* \[在\]
</dt> <dd>

類型： **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

代表中繼資源之 [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) 介面的指標。

</dd> <dt>

*IntermediateOffset* 
</dt> <dd>

類型： **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

中繼資源的位移（以位元組為單位）。

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

*pSrcData* \[在\]
</dt> <dd>

類型： **[ **D3D12 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***

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

 

