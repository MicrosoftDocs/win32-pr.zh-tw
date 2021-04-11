---
description: 將一般3D 轉換矩陣細分為其純量、旋轉和平移元件。
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: 'D3DXMatrixDecompose 函式 (D3DX10Math) '
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 507c8f177db0f71b3d333a8343e4166e649f424a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196409"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a>D3DXMatrixDecompose 函式 (D3DX10Math) 

將一般3D 轉換矩陣細分為其純量、旋轉和平移元件。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pOutScale* \[在\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

輸出 [**D3DXVECTOR3**](d3d10-d3dxvector3.md) 的指標，其中包含沿著 x、y 和 Z 軸套用的縮放因數。

</dd> <dt>

*pOutRotation* \[在\]
</dt> <dd>

類型： **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

描述旋轉之 [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) 的指標。

</dd> <dt>

*pOutTranslation* \[在\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

描述轉譯的 D3DXVECTOR3 向量指標。

</dd> <dt>

*pM* \[在\]
</dt> <dd>

Type： **Const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

要分解之輸入 [**D3DXMATRIX**](d3d10-d3dxmatrix.md) 矩陣的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為 S \_ OK。 如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10Math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[數學函數](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
