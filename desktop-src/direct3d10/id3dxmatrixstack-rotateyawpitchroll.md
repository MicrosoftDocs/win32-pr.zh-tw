---
description: 繞著任意軸的 (相對於全局座標空間) 旋轉。
ms.assetid: 35e237f6-40f2-4001-adb0-f489d61f64e7
title: 'ID3DXMATRIXStack：： RotateYawPitchRoll 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRoll
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8d57af31e9944c718419a3a90863c9960d0bdb36
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323375"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx10h"></a>ID3DXMATRIXStack：： RotateYawPitchRoll 方法 (D3DX10 .h) 

繞著任意軸的 (相對於全局座標空間) 旋轉。

## <a name="syntax"></a>語法


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*偏擺* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

以弧度為單位的 y 軸偏擺。

</dd> <dt>

*推銷* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

以弧度為單位的 X 軸左右間距。

</dd> <dt>

*滾動* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

以弧度為單位的 Z 軸左右滾動。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。

## <a name="remarks"></a>備註

這個方法會使用計算的旋轉矩陣，將旋轉加入矩陣堆疊中，如下所示：


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
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

 

 
