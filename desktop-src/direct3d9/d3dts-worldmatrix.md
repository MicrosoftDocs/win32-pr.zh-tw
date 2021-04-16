---
description: 將範圍0到255之間的索引對應到相對應的轉換狀態。
ms.assetid: b0a1548c-de5d-4eff-baf9-4aecb5e13443
title: 'D3DTS_WORLDMATRIX 宏 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDMATRIX
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: f80996a37e2fb48bf8ca7ea73f714b04e711b263
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514576"
---
# <a name="d3dts_worldmatrix-macro"></a>D3DTS \_ WORLDMATRIX 宏

將範圍0到255之間的索引對應到相對應的轉換狀態。

## <a name="syntax"></a>語法


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLDMATRIX(
   int index
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*index* 
</dt> <dd>

範圍0到255的索引值。

</dd> </dl>

## <a name="return-value"></a>傳回值

對應至指定 *索引* 的 [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) 。

## <a name="remarks"></a>備註

系統會保留範圍256到511的轉換狀態，以儲存最多可使用8位索引編制索引的256矩陣。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[巨集](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> </dl>

 

 
