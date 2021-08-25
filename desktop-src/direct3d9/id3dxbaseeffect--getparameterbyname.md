---
description: 藉由查詢名稱來取得最上層參數或結構成員參數的控制碼。
ms.assetid: fb03685e-e512-4293-80d7-6c2c0fc9ebfd
title: 'ID3DXBaseEffect：： GetParameterByName 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 30a1e585cbbbaee4891e3e7dc2cd4e3d3c871fd33fe36daa51c9137c26bfdc7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848678"
---
# <a name="id3dxbaseeffectgetparameterbyname-method"></a>ID3DXBaseEffect：： GetParameterByName 方法

藉由查詢名稱來取得最上層參數或結構成員參數的控制碼。

## <a name="syntax"></a>語法


```C++
D3DXHANDLE GetParameterByName(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hParameter* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

參數的控制碼，或最上層參數的 **Null** 。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*pName* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

包含參數名稱的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

傳回指定之參數的控制碼，如果索引無效，則 **為 Null** 。 請參閱 [處理 (Direct3D 9) ](handles.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
