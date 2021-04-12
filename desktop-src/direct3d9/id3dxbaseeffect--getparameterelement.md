---
description: 取得陣列元素參數的控制碼。
ms.assetid: fe8edbc5-dc1d-4386-8149-489541d55bde
title: 'ID3DXBaseEffect：： GetParameterElement 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterElement
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5130ccf57634f9b1a569a1dd70833fe2014e1a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323327"
---
# <a name="id3dxbaseeffectgetparameterelement-method"></a>ID3DXBaseEffect：： GetParameterElement 方法

取得陣列元素參數的控制碼。

## <a name="syntax"></a>語法


```C++
D3DXHANDLE GetParameterElement(
  [in] D3DXHANDLE hParameter,
  [in] UINT       ElementIndex
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hParameter* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

陣列的控制碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*ElementIndex* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

陣列元素索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

傳回指定之參數的控制碼，如果 hParameter 或 ElementIndex 無效，則 **為 Null** 。 請參閱 [處理 (Direct3D 9) ](handles.md)。

## <a name="remarks"></a>備註

這個方法是用來取得屬於陣列之參數的元素。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
