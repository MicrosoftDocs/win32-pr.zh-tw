---
description: 取得最上層參數或結構成員參數的控制碼。
ms.assetid: 940f1bfd-ce62-4c86-88cc-787e62cf6a93
title: 'ID3DXBaseEffect：： GetParameter 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameter
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7c96c371b36b8dcfc2e3e64a95798347ca3a6ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035432"
---
# <a name="id3dxbaseeffectgetparameter-method"></a>ID3DXBaseEffect：： GetParameter 方法

取得最上層參數或結構成員參數的控制碼。

## <a name="syntax"></a>語法


```C++
D3DXHANDLE GetParameter(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Index
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hParameter* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

參數的控制碼，或最上層參數的 **Null** 。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*索引* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

參數索引。

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

 

 
