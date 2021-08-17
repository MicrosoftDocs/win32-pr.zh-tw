---
description: 判斷四元數是否為識別四元數。
ms.assetid: 1cd39e1b-9b68-434d-b7b0-3ec6cddb8757
title: 'D3DXQuaternionIsIdentity 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b34debbe70ec6edcd3f08a1ec83383335a0d4f97801d122bc1bd73a82a81ff36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731590"
---
# <a name="d3dxquaternionisidentity-function"></a>D3DXQuaternionIsIdentity 函式

判斷四元數是否為識別四元數。

## <a name="syntax"></a>語法


```C++
BOOL D3DXQuaternionIsIdentity(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pQ* \[在\]
</dt> <dd>

Type： **Const [**D3DXQUATERNION**](d3dxquaternion.md) \***

將針對身分識別進行測試的 [**D3DXQUATERNION**](d3dxquaternion.md) 結構指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

如果四元數是識別四元數，此函數會傳回 **TRUE**。 否則，此函式會傳回 **FALSE**。

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

[**D3DXQuaternionIdentity**](d3dxquaternionidentity.md)
</dt> </dl>

 

 
