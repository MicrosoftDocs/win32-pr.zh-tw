---
title: 'GetRequiredIntermediateSize 函式 (D3dx12) '
description: 傳回要用於資料上傳的緩衝區所需大小。
ms.assetid: 424B52E9-DE52-40D2-B8B0-C27FD3D3C298
keywords:
- GetRequiredIntermediateSize 函式
topic_type:
- apiref
api_name:
- GetRequiredIntermediateSize
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15293ce1588704d55f41c364c35db57cbf4c869d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976507"
---
# <a name="getrequiredintermediatesize-function"></a>GetRequiredIntermediateSize 函式

傳回要用於資料上傳的緩衝區所需大小。

## <a name="syntax"></a>語法


```C++
UINT64 inline GetRequiredIntermediateSize(
  _In_ ID3D12Resource *pDestinationResource,
  _In_ UINT           FirstSubresource,
  _In_ UINT           NumSubresources
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDestinationResource* \[在\]
</dt> <dd>

類型： **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

代表目的地資源之 [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) 介面的指標。

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

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

緩衝區的大小（以位元組為單位）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx12。h</dt> </dl>  |
| 程式庫<br/> | <dl> <dt>D3D12 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3D12 的 Helper 函式](helper-functions-for-d3d12.md)
</dt> </dl>

 

