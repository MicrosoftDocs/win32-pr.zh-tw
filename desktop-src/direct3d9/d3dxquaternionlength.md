---
description: 傳回四元數的長度。
ms.assetid: daa835c2-2370-4427-a4ca-eddfb43d5c67
title: 'D3DXQuaternionLength 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 21589f6e470c1f23bd537b2983c7073a3f8c29866534418077018f616ca6b25f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044686"
---
# <a name="d3dxquaternionlength-function"></a>D3DXQuaternionLength 函式

傳回四元數的長度。

## <a name="syntax"></a>語法


```C++
FLOAT D3DXQuaternionLength(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pQ* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***

來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

四元數的長度。

## <a name="remarks"></a>備註

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

[**D3DXQuaternionLengthSq**](d3dxquaternionlengthsq.md)
</dt> </dl>

 

 
