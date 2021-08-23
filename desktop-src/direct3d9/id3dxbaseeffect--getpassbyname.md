---
description: 藉由查詢名稱來取得傳遞的控制碼。
ms.assetid: 24d043a2-5c87-4a59-80d4-0c81bd7a0b3e
title: 'ID3DXBaseEffect：： GetPassByName 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5837d2b69c793f788c4c89f648402e7924bc2f3af9a92bbbe596c133efe10d1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987758"
---
# <a name="id3dxbaseeffectgetpassbyname-method"></a>ID3DXBaseEffect：： GetPassByName 方法

藉由查詢名稱來取得傳遞的控制碼。

## <a name="syntax"></a>語法


```C++
D3DXHANDLE GetPassByName(
  [in] D3DXHANDLE hTechnique,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hTechnique* \[在\]
</dt> <dd>

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

父技術的控制碼。 請參閱 [處理 (Direct3D 9) ](handles.md)。

</dd> <dt>

*pName* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

包含傳遞名稱的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

傳回具有指定名稱之指定技術內第一個傳遞的控制碼，如果找不到名稱，則 **為 Null** 。 請參閱 [處理 (Direct3D 9) ](handles.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Effect。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
