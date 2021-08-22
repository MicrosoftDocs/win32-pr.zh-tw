---
description: D3DXQuaternionRotationYawPitchRoll 函式 (D3dx9math) -使用指定的偏擺、音調和變換建立四元數。
ms.assetid: be4a3bd5-114b-4652-8e0a-e51338317c16
title: 'D3DXQuaternionRotationYawPitchRoll 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 954fee40015b558b10ba83ef12b1555d06896413c6396ca12ed6e4374131caeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988430"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx9mathh"></a>D3DXQuaternionRotationYawPitchRoll 函式 (D3dx9math) 

使用指定的偏擺、音調和變換建立四元數。

## <a name="syntax"></a>語法


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是作業的結果。

</dd> <dt>

*偏擺* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

偏擺圍繞 y 軸，以弧度為單位。

</dd> <dt>

*推銷* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

X 軸的間距，以弧度為單位。

</dd> <dt>

*滾動* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

以弧度為單位，圍繞 Z 軸。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，該結構具有指定的偏擺、音調和滾動。

## <a name="remarks"></a>備註

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXQuaternionRotationYawPitchRoll** 函式就可以用來做為另一個函式的參數。

針對尚未正規化的任何四元數輸入，請使用 [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md)
</dt> <dt>

[**D3DXQuaternionRotationMatrix**](d3dxquaternionrotationmatrix.md)
</dt> </dl>

 

 
