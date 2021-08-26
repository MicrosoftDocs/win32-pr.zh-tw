---
description: 傳回識別四元數。
ms.assetid: 8088897b-5755-4ea0-afef-bd49d1921f5c
title: 'D3DXQuaternionIdentity 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ca40cf6e600d63d7f50403821b39d41ff88104c68587416370202d0bfc66ef5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986428"
---
# <a name="d3dxquaternionidentity-function"></a>D3DXQuaternionIdentity 函式

傳回識別四元數。

## <a name="syntax"></a>語法


```C++
D3DXQUATERNION* D3DXQuaternionIdentity(
  _Inout_ D3DXQUATERNION *pOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*不悅* \[in、out\]
</dt> <dd>

類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是作業的結果。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

[**D3DXQUATERNION**](d3dxquaternion.md)結構的指標，此結構是身分識別四元數。

## <a name="remarks"></a>備註

假設有一個四元數 (x、y、z、w) ， **D3DXQuaternionIdentity** 函數會傳回四元數 (0、0、0、1) 。

此函式的傳回值與 *不悅* 參數中所傳回的值相同。 如此一來， **D3DXQuaternionIdentity** 函式就可以用來做為另一個函式的參數。

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

[**D3DXQuaternionIsIdentity**](d3dxquaternionisidentity.md)
</dt> </dl>

 

 




