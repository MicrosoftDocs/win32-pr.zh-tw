---
description: 藉由使用不區分大小寫的搜尋來查閱其語義，取得最上層參數或結構成員參數的控制碼。
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: 'ID3DXBaseEffect：： GetParameterBySemantic 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterBySemantic
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fa00ef4585462f068e95fcefca8332acd46930efaf1bb1c108a471511ab63eb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791008"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a>ID3DXBaseEffect：： GetParameterBySemantic 方法

藉由使用不區分大小寫的搜尋來查閱其語義，取得最上層參數或結構成員參數的控制碼。

## <a name="syntax"></a>語法


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hParameter* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

參數的控制碼，或最上層參數的 **Null** 。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*pSemantic* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

包含語義名稱的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

傳回符合指定之語義的第一個參數的控制碼，如果找不到語義，則 **為 Null** 。 請參閱 [處理 (Direct3D 9) ](handles.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
