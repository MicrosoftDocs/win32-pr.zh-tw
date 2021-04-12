---
description: 描述在主要畫面格動畫中使用的四元數索引鍵。 四元數索引鍵是指定時間的四元值。
ms.assetid: 8f5b74a3-f712-40ac-942c-a2189c2327c8
title: 'D3DXKEY_QUATERNION 結構 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_QUATERNION
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 12e4deead606c1a2c5b103ed9fd0e31e23515982
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322900"
---
# <a name="d3dxkey_quaternion-structure"></a>D3DXKEY \_ 四元數結構

描述在主要畫面格動畫中使用的四元數索引鍵。 四元數索引鍵是指定時間的四元值。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXKEY_QUATERNION {
  FLOAT          Time;
  D3DXQUATERNION Value;
} D3DXKEY_QUATERNION, *LPD3DXKEY_QUATERNION;
```



## <a name="members"></a>成員

<dl> <dt>

**Time**
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

時間值。

</dd> <dt>

**值**
</dt> <dd>

類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)**

</dd> <dd>

提供旋轉值的 [**D3DXQUATERNION**](d3dxquaternion.md)四元數。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9anim。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
