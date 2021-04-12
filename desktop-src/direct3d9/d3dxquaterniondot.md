---
description: 傳回兩個四元數的點乘積。
ms.assetid: 2ed9aca9-0526-4b92-bd66-b09dcf4f474a
title: 'D3DXQuaternionDot 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e893ed9260c0d843e8454d96ab5b634741ee60d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323184"
---
# <a name="d3dxquaterniondot-function"></a>D3DXQuaternionDot 函式

傳回兩個四元數的點乘積。

## <a name="syntax"></a>語法


```C++
FLOAT D3DXQuaternionDot(
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pQ1* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***

來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。

</dd> <dt>

*pQ2* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***

來源 [**D3DXQUATERNION**](d3dxquaternion.md) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

兩個四元數的點乘積。

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
</dt> </dl>

 

 
