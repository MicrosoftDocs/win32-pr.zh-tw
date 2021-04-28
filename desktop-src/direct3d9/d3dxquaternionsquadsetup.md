---
description: D3DXQuaternionSquadSetup 函式 (D3dx9math) -設定球形四邊形插補的控制點。
ms.assetid: f800d457-8546-49a1-800e-e5c27af96710
title: 'D3DXQuaternionSquadSetup 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquadSetup
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1dcaa90380ec703b4b56458906ab8bd965d7568c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093946"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx9mathh"></a>D3DXQuaternionSquadSetup 函式 (D3dx9math) 

設定球形四邊形插補的控制點。

## <a name="syntax"></a>語法


```C++
void D3DXQuaternionSquadSetup(
  _Out_       D3DXQUATERNION *pAOut,
  _Out_       D3DXQUATERNION *pBOut,
  _Out_       D3DXQUATERNION *pCOut,
  _In_  const D3DXQUATERNION *pQ0,
  _In_  const D3DXQUATERNION *pQ1,
  _In_  const D3DXQUATERNION *pQ2,
  _In_  const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAOut* \[擴展\]
</dt> <dd>

類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

有關的指標。

</dd> <dt>

*pBOut* \[擴展\]
</dt> <dd>

類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Bout about 的指標。

</dd> <dt>

*pCOut* \[擴展\]
</dt> <dd>

類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

COut 的指標。

</dd> <dt>

*pQ0* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***

輸入控制點的指標，Q0。

</dd> <dt>

*pQ1* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***

輸入控制點的指標，Q1。

</dd> <dt>

*pQ2* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***

輸入控制點的指標，Q2。

</dd> <dt>

*pQ3* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***

輸入控制點的指標，第3季。

</dd> </dl>

## <a name="return-value"></a>傳回值

無。

## <a name="remarks"></a>備註

此函式會採用四個控制點，提供給輸入 pQ0、pQ1、pQ2 和 pQ3。 然後，此函式會改變這些值，以找出沿著最短路徑流動的曲線。 Q0、q2 和 q3 的值的計算方式如下所示。


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



在計算新的 Q 值之後，有關、Bout about 和 COut 的值的計算方式如下：

有關 = q1 \* e<sup> \[ -0.25 \ \* ( \ Ln \[ exp (q1) \* q2 \] \ + \ ln \[ exp (q1) \* q0 \] \ ) \ \] </sup>

Bout about = q2 \* e<sup> \[ -0.25 \ \* ( \ Ln \[ Exp (q2) \* q3 \ \] + \ ln \[ exp (q2) \* q1 \] \ ) \ \] </sup>

COut = q2

> [!Note]  
> Ln 是 API 方法 [**D3DXQuaternionLn**](d3dxquaternionln.md) ，而 EXP 是 Api 方法 [**D3DXQuaternionExp**](d3dxquaternionexp.md)。

 

針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。

### <a name="examples"></a>範例

下列範例示範如何使用一組四元數索引鍵 (Q0、Q1、Q2、Q3) 來計算內部四邊形點 (A，B，C) 。 這可確保相鄰區段之間的切線是連續的。


```
      A     B
Q0    Q1    Q2    Q3
```



下列程式碼範例將示範如何在 Q1 和 Q2 之間進行插補。


```
// Rotation about the z-axis
D3DXQUATERNION Q0 = D3DXQUATERNION(0,  0, 0.707f, -.707f);
D3DXQUATERNION Q1 = D3DXQUATERNION(0,  0, 0.000f, 1.000f);
D3DXQUATERNION Q2 = D3DXQUATERNION(0,  0, 0.707f, 0.707f);
D3DXQUATERNION Q3 = D3DXQUATERNION(0,  0, 1.000f, 0.000f);
D3DXQUATERNION A, B, C, Qt;
FLOAT time = 0.5f;

D3DXQuaternionSquadSetup(&A, &B, &C, &Q0, &Q1, &Q2, &Q3);
D3DXQuaternionSquad(&Qt, &Q1, &A, &B, &C, time);
```



> [!Note]
>
> -   C 是 +/-Q2，視函數的結果而定。
> -   Qt 是函數的結果。
>
> 結果是時間 = 0.5 的 Z 軸周圍的45度旋轉。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
</dt> </dl>

 

 




