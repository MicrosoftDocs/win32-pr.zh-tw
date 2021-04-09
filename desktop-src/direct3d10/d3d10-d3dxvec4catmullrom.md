---
description: 使用指定的4D 向量，執行 Catmull-Rom 插補。
ms.assetid: e3a10989-e25e-46fa-b72e-bade936cacf1
title: 'D3DXVec4CatmullRom 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4CatmullRom
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 8e027272a038f17a77dbeda861d6be909afa2f7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946071"
---
# <a name="d3dxvec4catmullrom-function-d3dx10mathh"></a>D3DXVec4CatmullRom 函式 (D3DX10Math) 

使用指定的4D 向量，執行 Catmull-Rom 插補。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR4* D3DXVec4CatmullRom(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV0,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

作業結果之 [**D3DXVECTOR4**](d3d10-d3dxvector4.md) 的指標。

</dd> <dt>

*pV0* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

來源 D3DXVECTOR4 結構的指標，也就是位置向量。

</dd> <dt>

*pV1* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

來源 D3DXVECTOR4 結構的指標，也就是位置向量。

</dd> <dt>

*pV2* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

來源 D3DXVECTOR4 結構的指標，也就是位置向量。

</dd> <dt>

*pV3* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

來源 D3DXVECTOR4 結構的指標，也就是位置向量。

</dd> <dt>

 \[ 中的 s\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

加權係數。 請參閱＜備註＞。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

D3DXVECTOR4 結構的指標，此結構是 Catmull-Rom 插補的結果。

## <a name="remarks"></a>備註

假設有四個點 (p1、p2、p3、p4) 、找出函式 Q (s) ，如下所示：


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



您可以藉由設定下列各項，從 Hermite 曲線衍生出 Catmull-Rom 曲線：


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



其中：

v1 是 pV0 的內容。

pV1 內容中的 v2。

p3 是 pV2 的內容。

p4 是 pV3 的內容。

使用 Hermite 曲線方程式：


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



而以 v1、v2、t1 替代，t2 會產生：


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



這可以重新排列為：


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
