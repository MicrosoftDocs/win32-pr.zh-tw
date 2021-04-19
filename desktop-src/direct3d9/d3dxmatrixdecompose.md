---
description: 將一般3D 轉換矩陣細分為其純量、旋轉和平移元件。
ms.assetid: 73d3c248-1254-444e-9fd8-4f144424ddb7
title: 'D3DXMatrixDecompose 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDecompose
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 92f120f1c3637216d77a5298b5de219f5605d571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986760"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a>D3DXMatrixDecompose 函式 (D3dx9math) 

將一般3D 轉換矩陣細分為其純量、旋轉和平移元件。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXMatrixDecompose(
  _Inout_       D3DXVECTOR3    *pOutScale,
  _Inout_       D3DXQUATERNION *pOutRotation,
  _Inout_       D3DXVECTOR3    *pOutTranslation,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pOutScale* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***

輸出 [**D3DXVECTOR3**](d3dxvector3.md) 的指標，其中包含沿著 x、y 和 Z 軸套用的縮放因數。

</dd> <dt>

*pOutRotation* \[in、out\]
</dt> <dd>

類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

描述旋轉之 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。

</dd> <dt>

*pOutTranslation* \[in、out\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](d3dxvector3.md)\***

描述轉譯的 [**D3DXVECTOR3**](d3dxvector3.md) 向量指標。

</dd> <dt>

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](d3dxmatrix.md) \***

要分解之輸入 [**D3DXMATRIX**](d3dxmatrix.md) 矩陣的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為 S \_ OK。 如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




