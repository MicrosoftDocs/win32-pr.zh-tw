---
description: D3DXVec2CatmullRom 函式 (D3dx9math) -使用指定的2D 向量執行 Catmull-Rom 插補。
ms.assetid: dacda32d-b4c4-4d8b-9d20-9a4bb1d3ce6c
title: 'D3DXVec2CatmullRom 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CatmullRom
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c734727f3f2f44c9094885e0e743f605f16c91d2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114316"
---
# <a name="d3dxvec2catmullrom-function-d3dx9mathh"></a>D3DXVec2CatmullRom 函式 (D3dx9math) 

使用指定的2D 向量，執行 Catmull-Rom 插補。

## <a name="syntax"></a>語法


```C++
D3DXVECTOR2* D3DXVec2CatmullRom(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV0,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_    const D3DXVECTOR2 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***

[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*pV0* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***

來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標，也就是位置向量。

</dd> <dt>

*pV1* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***

來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標，也就是位置向量。

</dd> <dt>

*pV2* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***

來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標，也就是位置向量。

</dd> <dt>

*pV3* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR2**](d3dxvector2.md) \***

來源 [**D3DXVECTOR2**](d3dxvector2.md) 結構的指標，也就是位置向量。

</dd> <dt>

 \[ 中的 s\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

加權係數。 請參閱＜備註＞。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXVECTOR2**](d3dxvector2.md)\***

[**D3DXVECTOR2**](d3dxvector2.md)結構的指標，此結構是 Catmull-Rom 插補的結果。

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

v2 是 pV1 的內容。

p3 是 pV2 的內容。

p4 是 pV3 的內容。

使用 Hermite 曲線方程式：


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



而以 v1、v2、t1 替代，t2 會產生：


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2)/2
```



這可以重新排列為：


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3CatmullRom**](d3dxvec3catmullrom.md)
</dt> <dt>

[**D3DXVec4CatmullRom**](d3dxvec4catmullrom.md)
</dt> </dl>

 

 
