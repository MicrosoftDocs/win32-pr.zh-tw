---
description: D3DXQuaternionSquad 函式 (D3DX10Math) -使用球形四邊形插補在四元數之間進行插補。
ms.assetid: ba953731-4372-4b32-942b-23abfe479704
title: 'D3DXQuaternionSquad 函式 (D3DX10Math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: acd1c3e816d8f5a88b266a71e7579227be2def3452fbc25307fb4fa899ecacb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070018"
---
# <a name="d3dxquaternionsquad-function-d3dx10mathh"></a>D3DXQuaternionSquad 函式 (D3DX10Math) 

使用球面四邊形插補在四元數之間進行插補。

## <a name="syntax"></a>語法


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

作業結果之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。

</dd> <dt>

*pQ1* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

來源 D3DXQUATERNION 結構的指標。

</dd> <dt>

*pA* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

來源 D3DXQUATERNION 結構的指標。

</dd> <dt>

*pB* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

來源 D3DXQUATERNION 結構的指標。

</dd> <dt>

*電腦* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

來源 D3DXQUATERNION 結構的指標。

</dd> <dt>

 \[ 中的 t\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

指出在四元數之間插離的參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

D3DXQUATERNION 結構的指標，此結構是指球形四邊形插補的結果。

## <a name="remarks"></a>備註

此函式會使用下列一連串的球面線性插補作業：


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



此函式的傳回值與不悅參數中所傳回的值相同。 如此一來，D3DXQuaternionSquad 函式就可以用來做為另一個函式的參數。

針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
