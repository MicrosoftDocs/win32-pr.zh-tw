---
description: ID3DXMATRIXStack：： RotateAxis 方法 (D3DX10 .h) -在任意軸的周圍旋轉 (相對於全球座標空間) 。
ms.assetid: 7c842bf6-2d13-422e-8136-0506a76ce9fe
title: 'ID3DXMATRIXStack：： RotateAxis 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxis
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0a2e52eed1c1957de9a0fcfed4ba3d3d05f89cb9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107907"
---
# <a name="id3dxmatrixstackrotateaxis-method-d3dx10h"></a>ID3DXMATRIXStack：： RotateAxis 方法 (D3DX10 .h) 

繞著任意軸的 (相對於全局座標空間) 旋轉。

## <a name="syntax"></a>語法


```C++
HRESULT RotateAxis(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pV* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

任意旋轉軸的指標。 請參閱 [**D3DXVECTOR3**](d3d10-d3dxvector3.md)。

</dd> <dt>

*角度* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

任意軸的旋轉角度（以弧度為單位）。 朝原點查看任意軸時，會以逆時針測量角度。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

這個方法會使用計算的旋轉矩陣，將旋轉加入矩陣堆疊中，如下所示：


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



由於旋轉會靠右乘以矩陣堆疊，所以旋轉是相對於全球座標空間。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
