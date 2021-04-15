---
description: 產生網格邊緣清單以及共用每個邊緣的臉部清單。
ms.assetid: 3932e2b1-031d-4962-ad90-6e9da8cf2e0e
title: 'ID3DX10Mesh：： GenerateAdjacencyAndPointReps 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateAdjacencyAndPointReps
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c46cf83931c95116132798ca971f9d4e61da2af8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514653"
---
# <a name="id3dx10meshgenerateadjacencyandpointreps-method"></a>ID3DX10Mesh：： GenerateAdjacencyAndPointReps 方法

產生網格邊緣清單以及共用每個邊緣的臉部清單。

## <a name="syntax"></a>語法


```C++
HRESULT GenerateAdjacencyAndPointReps(
  [in] FLOAT Epsilon
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Epsilon* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

指定在位置中差異小於 epsilon 的頂點應視為重合。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

在應用程式產生網格的相鄰資訊之後，可以將網格資料優化，以提升繪製效能。

相鄰緩衝區中的專案順序是由索引緩衝區中的頂點索引順序所決定。 連續的三角形0一律對應至角落0和1的索引之間的邊緣。 連續的三角形1一律對應至角落1和2的索引之間的邊緣，連續的三角形2則對應至角落2與0的索引之間的邊緣。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
