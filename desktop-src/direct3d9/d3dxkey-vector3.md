---
description: 描述在主要畫面格動畫中使用的向量索引鍵。 它會在指定的時間指定一個向量。 這可用於調整和轉譯金鑰。
ms.assetid: 7a7ba2ce-c9f3-4a04-b865-39de9070868b
title: 'D3DXKEY_VECTOR3 結構 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_VECTOR3
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0214582b3fb1267caeb30a6cca905cbf7243ecf5dd1af40365841b315359317f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119178"
---
# <a name="d3dxkey_vector3-structure"></a>D3DXKEY \_ VECTOR3 結構

描述在主要畫面格動畫中使用的向量索引鍵。 它會在指定的時間指定一個向量。 這可用於調整和轉譯金鑰。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXKEY_VECTOR3 {
  FLOAT       Time;
  D3DXVECTOR3 Value;
} D3DXKEY_VECTOR3, *LPD3DXKEY_VECTOR3;
```



## <a name="members"></a>成員

<dl> <dt>

**Time**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

主要畫面格時間戳記。

</dd> <dt>

**值**
</dt> <dd>

類型： **[ **D3DXVECTOR3**](d3dxvector3.md)**

</dd> <dd>

提供尺規和/或轉譯值的 [**D3DXVECTOR3**](d3dxvector3.md) 3d 向量。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9anim。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
