---
description: 藉由查詢名稱來取得技術的控制碼。
ms.assetid: 34871229-ad63-4575-8c60-f27d7f7dddce
title: 'ID3DXBaseEffect：： GetTechniqueByName 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechniqueByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5827527bf5151b121958c3f5803ef8a7e74f8d60
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985915"
---
# <a name="id3dxbaseeffectgettechniquebyname-method"></a>ID3DXBaseEffect：： GetTechniqueByName 方法

藉由查詢名稱來取得技術的控制碼。

## <a name="syntax"></a>語法


```C++
D3DXHANDLE GetTechniqueByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

包含技術名稱的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

傳回具有指定名稱之第一個技術的控制碼，如果找不到名稱，則 **為 Null** 。 請參閱 [處理 (Direct3D 9) ](handles.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Shader。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
