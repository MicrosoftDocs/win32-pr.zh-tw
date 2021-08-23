---
description: 取得網格中的頂點數目。
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: 'ID3DX10Mesh：： GetVertexCount 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 00fd0cd84aedb32e2da567a92ffc421f41394a991872f9216b06a4f28f895183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566888"
---
# <a name="id3dx10meshgetvertexcount-method"></a>ID3DX10Mesh：： GetVertexCount 方法

取得網格中的頂點數目。 網格可能包含多個頂點緩衝區 (也就是一個頂點緩衝區可能包含所有位置資料、另一個可能包含所有紋理座標資料等 ) ，不過每個頂點緩衝區都包含相同數目的元素。

## <a name="syntax"></a>語法


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

類型： **[ **UINT**](../winprog/windows-data-types.md)**

網格中的頂點數目。

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

 

 
