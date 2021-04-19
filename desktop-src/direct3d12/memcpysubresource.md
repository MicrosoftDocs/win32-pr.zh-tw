---
title: 'MemcpySubresource 函式 (D3dx12) '
description: 逐列複製 subresource 資料列。
ms.assetid: 33A9F99D-FD85-4FD6-AFD6-7A10F16C3D9B
keywords:
- MemcpySubresource 函式
topic_type:
- apiref
api_name:
- MemcpySubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955211a490927033186442480b3449773b4ebcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988202"
---
# <a name="memcpysubresource-function"></a>MemcpySubresource 函式

逐列複製 subresource 資料列。

## <a name="syntax"></a>語法


```C++
void inline MemcpySubresource(
  _In_ const D3D12_MEMCPY_DEST      *pDest,
  _In_ const D3D12_SUBRESOURCE_DATA *pSrc,
             SIZE_T                 RowSizeInBytes,
             UINT                   NumRows,
             UINT                   NumSlices
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDest* \[在\]
</dt> <dd>

Type： **Const [**D3D12 \_ MEMCPY \_ DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) \***

[**D3D12 \_ MEMCPY \_ 目的地**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest)結構的指標，此結構描述記憶體複製作業的目的地。

</dd> <dt>

*.psrc* \[在\]
</dt> <dd>

Type： **Const [**D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***

[**D3D12 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)結構的指標，此結構描述記憶體複製作業的來源。

</dd> <dt>

*RowSizeInBytes* 
</dt> <dd>

類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)**

每個資料列的大小（以位元組為單位）。

</dd> <dt>

*NumRows* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

列的數目。

</dd> <dt>

*NumSlices* 
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

配量的數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

也請考慮下列方法：

-   [**ID3D12Resource::WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)
-   [**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)
-   [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)

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

 

