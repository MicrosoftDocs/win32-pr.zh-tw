---
description: D3DXComputeBoundingSphere 函式 (D3DX10math) -計算網格的周框球體。
ms.assetid: 54f486d2-45e9-4fc1-90a3-97488ed4d900
title: 'D3DXComputeBoundingSphere 函式 (D3DX10math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingSphere
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0041d775b21d1af37bc51d6ec2f432e616b2abd6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113296"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx10mathh"></a>D3DXComputeBoundingSphere 函式 (D3DX10math) 

計算網格的周框球體。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_ const D3DXVECTOR3 *pFirstPosition,
  _In_       DWORD       NumVertices,
  _In_       DWORD       dwStride,
  _In_       D3DXVECTOR3 *pCenter,
  _In_       FLOAT       *pRadius
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFirstPosition* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

第一個位置的指標。

</dd> <dt>

*NumVertices* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

頂點數目。

</dd> <dt>

*dwStride* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

位置向量之間的位元組數目。

</dd> <dt>

*pCenter* \[在\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

[**D3DXVECTOR3**](d3d10-d3dxvector3.md) 結構，定義傳回之周框球體的座標中心。

</dd> <dt>

*pRadius* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

傳回之周框球體的半徑。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10math。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
